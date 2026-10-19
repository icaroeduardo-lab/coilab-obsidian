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
atualizado_em: 2026-10-14
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
- A documentação exige login. O anexo é uma cópia de 2026-10-14; conferir se mudou antes de usar como contrato.
- Mensagens e contatos carregam dado pessoal do cidadão. Nada disso vai para log nem para esta nota (LGPD).
- `reopenedFromChatId` indica que uma conversa retomada ganha **chat novo**. Isso é coerente com a medição da issue #217 (nenhuma confirmação de TTL em produção): quem volta provavelmente chega à Maria com outro `chatId`.
- `Chat.category` é o **setor** da fila na Tykhe. Pode ser o mapeamento natural do `tipoCaso` proposto na issue #225 (redirecionar para a Tykhe).

## Perguntas em aberto
- [ ] Nas perguntas sim/não da Maria, a Tykhe manda sempre `"true"`/`"false"` dos botões, ou pode repassar texto digitado? (issue #227)
- [ ] Contrato do status novo `redirecionado` + `tipoCaso` (issue #225): slug ou id de setor (`category`) da Tykhe?
- [ ] Contato técnico do lado da Tykhe.

## Relacionado
- [[Maria - atendimento automatizado]]
- [[Maria]] (inventário de IA)
- Issues: [#225](https://github.com/dgd-dprj/maria-langgraph-pp/issues/225), [#227](https://github.com/dgd-dprj/maria-langgraph-pp/issues/227), [#217](https://github.com/dgd-dprj/maria-langgraph-pp/issues/217)
