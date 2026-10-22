---
tipo: sistema
status: ativo
dono_sistema: Tykhe
contato: 
uso_no_coilab: Chatbot de atendimento ao cidadão (WhatsApp e web); consumidor da API da Maria
documentacao: https://api-flow.tykhe.dev/rest/v1/docs/
acesso_documentacao: exige login no TykheFlow (flow.tykhe.dev)
autenticacao: Bearer JWT ou header access-token
projetos:
  - "[[Maria - atendimento automatizado]]"
atualizado_em: 2026-10-22
tags:
  - sistema
---

# Tykhe

> Nunca registrar token, senha ou chave aqui: só o mecanismo e onde se obtém.

## O que é
- Plataforma de atendimento (**TykheFlow**) que conversa com o cidadão por WhatsApp e web: chats, filas por setor, agentes humanos, campanhas de mensagens ativas e relatórios. A API se apresenta como "Taike API 1.0.0".
- Na Defensoria, é a porta de entrada do cidadão. A **Maria** atende por trás dela os fluxos de pessoa presa e violência doméstica.

## Como integramos
- **Tykhe → Maria**: a Tykhe é o único consumidor previsto da API da Maria, servidor a servidor, com Bearer token fixo (`API_KEY`). Rotas: `GET /fluxos`, `POST /atendimentos`, `POST /atendimentos/respostas`, `GET /atendimentos/:chatId` e `POST /atendimentos/orquestrador`. Contrato: [docs/contrato-tykhe.md](https://github.com/dgd-dprj/maria-langgraph-pp/blob/develop/docs/contrato-tykhe.md).
- **Maria → Tykhe**: hoje nenhuma chamada. A API da Tykhe abaixo é a da plataforma deles e **não** descreve como eles chamam a Maria.

## API da Tykhe (base `/rest/v1`)
Fonte: [[anexos/tykhe-swagger.json|tykhe-swagger.json]] (OpenAPI 3.0, exportado em 2026-10-14).

| Grupo | Endpoints | Para quê |
|---|---|---|
| Saúde | `GET /health` | Verificação de disponibilidade |
| Chats | `GET /chats`, `GET /chats/{id}`, `POST /chats/finish`, `POST /chats/{id}/finish`, `POST /chats/{id}/reopen`, `GET`/`POST /chats/{id}/tags` | Listar (filtros: status, contato, agente, setor, período, protocolo; paginação por cursor `after`/`before`/`first`/`last`), finalizar (inclusive em lote), reabrir, etiquetas |
| Mensagens | `GET /messages`, `POST /messages`, `GET /messages/{id}` | Ler e enviar mensagens de um chat |
| Contatos | `GET`/`POST /customers`, `GET`/`PUT`/`DELETE /customers/{id}` | Cadastro do cidadão (contato) |
| Campanhas | `GET`/`POST /activeMessageLists`, `GET /activeMessageLists/{id}` | Mensagens ativas: template, botões, recorrência, canal/SMS/e-mail |
| Relatórios | `GET`/`POST /reports`, `GET`/`DELETE /reports/{id}` | Gerar e baixar relatórios |
| Webhooks | `GET`/`POST /projectWebhooks`, `GET`/`PUT`/`DELETE /projectWebhooks/{id}` | Configurar webhooks (evento `messageReceived`, por setor ou todos) |
| Webhook de saída | `POST /webhooks/customer-service-messages` (documentação, não rota) | Formato que a Tykhe **envia** para a URL configurada |

### Webhook de saída (mensagens de atendimento)
- Mensagens agrupadas em **lotes com até 30 s** de intervalo.
- Campos: `projectId`, `chatId`, `customerId`, `reopenedFromChatId` (conversa anterior, quando reaberta), `messages[]` (`messageId`, `text`, `fileId`/`fileName`, `whoSent`, horários), `timestamp`.

## Autenticação
- `bearerAuth`: HTTP Bearer (JWT).
- `accessToken`: header `access-token`, obtido na página de integrações do TykheFlow.

## Pontos de atenção
- A documentação exige login. O anexo é uma cópia de 2026-10-14; em 2026-10-22 a página foi salva de novo (HTML de cerca de 550 KB) e conferida por texto: mesmos grupos de rotas, sem rota nova. A comparação foi aproximada.
- Esta documentação é a da **API REST da plataforma**. Ela **não** descreve os nós do construtor de fluxos (Chamada API, Variável, Troca de fluxo, Condição). O que sabemos deles vem do comportamento observado: ver "Construtor de fluxos" abaixo.
- Mensagens e contatos carregam dado pessoal do cidadão. Nada disso vai para log nem para esta nota (LGPD).
- `reopenedFromChatId` indica que uma conversa retomada ganha **chat novo**. Isso é coerente com a medição da issue #217 (nenhuma confirmação de TTL em produção): quem volta provavelmente chega à Maria com outro `chatId`.
- `Chat.category` é o **setor** da fila na Tykhe. Pode ser o mapeamento natural do `tipoCaso` proposto na issue #225 (redirecionar para a Tykhe).

## Como testar o fluxo "como se fosse o WhatsApp"
- **A API REST não simula a pessoa.** `POST /messages` cria uma mensagem **passiva** (resposta ao cliente) com `whoSent` `agent`, `manager` ou `bot`: ela escreve **para** o cidadão, não **como** o cidadão. Não há rota para injetar uma mensagem recebida do cliente. `POST /customers` só cadastra o contato.
- **Mensagem ativa** (`/activeMessageLists`, com `flowId`) dispara template para contatos de verdade pelo canal. Não usar para teste sem um número de teste do laboratório.
- Caminhos de teste que não dependem dessa API:
  1. **Maria**: chamar a API dela como a Tykhe chamaria (`/atendimentos/orquestrador`, `/atendimentos/respostas`), com `chatId` de teste e CPF fictício. Cobre o lado da Maria, não o comportamento dos nós.
  2. **Tykhe**: executar o fluxo no próprio TykheFlow (teste do editor ou canal web). **Não verificado**: não temos a documentação desse recurso.
- Ao testar pela Tykhe, observar: variável que sobra de uma conversa para outra (`clearEmptyVariable`), botões Sim/Não indo como `"true"`/`"false"`, resposta com aspas ou quebra de linha dentro do corpo JSON e `chatId` novo a cada conversa.

## Construtor de fluxos (observado, não documentado)
- Nó de **Chamada API**: opção `clearEmptyVariable`. Ligada, a variável ligada a um campo ausente na resposta é limpa; desligada, mantém o valor anterior (inferência pelo comportamento; confirmar com a Tykhe).
- Nó de **variável**, operação `add`: se substitui ou concatena o valor ainda não foi confirmado.
- Nó de **troca de fluxo** (subfluxo): se as variáveis passam entre os fluxos funciona no desenho atual, mas não está documentado.
- Corpo JSON da Chamada API: o texto digitado entra no corpo por variável (`"{{Variável}}"`); aspas e quebras de linha podem quebrar o JSON. O CPF precisa ir entre aspas (`"{{CPF}}"`): sem aspas, a Maria aceita, mas ignora o valor (teste no release, 2026-10-22).

## Perguntas em aberto
- [ ] Nas perguntas sim/não da Maria, a Tykhe manda sempre `"true"`/`"false"` dos botões, ou pode repassar texto digitado? (issue #227). A Maria aceita "sim"/"não" digitados segundo o `docs/contrato-tykhe.md`; falta testar na Tykhe.
- [ ] Onde estão as páginas dos nós do construtor de fluxos (o erro da API citou `docs.vendiz.com/api`)?
- [ ] A Tykhe gera `chatId` novo a cada conversa do mesmo contato, mesmo após `concluido`/`handoff_humano`? (issue #228; a Maria responde 409 se o `chatId` encerrado receber mais respostas)
- [ ] Contrato do status novo `redirecionado` + `tipoCaso` (issue #225): slug ou id de setor (`category`) da Tykhe?
- [ ] Contato técnico do lado da Tykhe.

## Relacionado
- [[Maria - atendimento automatizado]]
- [[Maria]] (inventário de IA)
- Issues: [#225](https://github.com/dgd-dprj/maria-langgraph-pp/issues/225), [#227](https://github.com/dgd-dprj/maria-langgraph-pp/issues/227), [#217](https://github.com/dgd-dprj/maria-langgraph-pp/issues/217)
