---
tipo: documento
data: 2026-10-21
projeto: "[[Compartilhamento da MarIA com a Bahia]]"
status: rascunho
tags:
  - documento
  - maria
  - governanca
---

# Governança open source da MarIA (esboço para a reunião de 21/10)

> Rascunho para discussão (reunião de 21/10). Base: documento do Iran ([[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]]), atas de 15 e 16/10 e a [[Resolução DPRJ - Política de IA]]. Nada aqui foi combinado com a Bahia nem com a COPPE.

## Ideia central
Tratar a MarIA como um produto com **núcleo (core) mantido pela DPRJ** e **plugins/adapters mantidos por cada defensoria**. Outras defensorias usam o núcleo, contribuem por pull request e ficam responsáveis pelo que é específico delas (broker, sistema de casos, nuvem, chaves de IA). Isso junta o que o Iran propôs (Ports and Adapters, PR com regras, mitigação de impacto) com o modelo "híbrido inspirado em comunidades de código" que o Braida sugeriu em 16/10.

## 1. Papéis e decisões
| Papel | Quem (proposta) | Decide |
|---|---|---|
| Mantenedor do núcleo | DPRJ (COILAB, com Braida/COPPE na revisão técnica) | O que entra no core, releases, roadmap |
| Comitê de governança | COILAB + representantes de cada defensoria participante | Prioridades gerais, regras do projeto, entrada de novos membros |
| Ponto focal de cada defensoria | PO e Tech Lead nomeados por ela | Pedidos e PRs da sua defensoria |
| Mantenedor de adapter | Cada defensoria (ex.: Solar = DPBA, Verde = DPRJ) | Código do seu adapter |
| Segurança e dados | DPRJ (CGSI/EPD, conforme a Política de IA) | Veto em PR que afete dados pessoais ou segurança |

Regra simples de decisão: mudança no core = aprovação do mantenedor; mudança em adapter = aprovação do dono do adapter, com checagem automática do core.

## 2. Contribuição e revisão de features
Fluxo proposto: **issue → proposta curta (o quê, por quê, impacto) → PR → esteira automática → revisão humana → merge → release.**
- Qualquer feature nova começa por issue no repositório central (canal único e registrado, não WhatsApp).
- Só PR "verde" entra na revisão humana: testes, lint, checagem de dependências/segredos.
- Exigências do PR (do doc do Iran): ao menos 1 revisor sênior DPRJ/COPPE; testes passando; não alterar regras de negócio exclusivas da DPRJ; **documentação técnica obrigatória**.
- Teto de PRs em revisão por sprint e sem sprint paralela (proposta do Braida).
- Quem autorizou o merge responde pelo efeito (nota do Iran): por isso o merge no core fica só com o mantenedor.

## 3. Núcleo x plugin (Ports and Adapters)
- O core define interfaces (ex.: sistema de casos, broker de mensagens); Verde, Solar, Tykhe e o broker da Bahia são adapters escolhidos por configuração.
- O core nunca importa código de plugin; o contrato das interfaces é versionado e muda pouco.
- Fluxos, sumários e modelos de petição específicos ficam no banco/configuração (o novo motor da MarIA permite fluxo próprio sem tocar no núcleo), não em fork.
- **Pré-requisito**: confirmar no código o quanto o desacoplamento já existe (IDs fixos de NAD/POMAR, GovBR obrigatório, logos). Isso é a lista de generalização do Braida e deve vir antes de abrir para outras defensorias.

## 4. Versionamento e releases
- Versionamento semântico do core e das interfaces; changelog por release.
- Releases em cadência fixa (sugestão: mensal), com notas de migração.
- Cada defensoria decide quando atualizar a sua instância, com versão mínima suportada (ex.: as duas últimas).
- Homologação própria: cada defensoria testa no seu ambiente (a DPRJ pode oferecer o bot de Telegram em homologação como porta de entrada).

## 5. Critérios para aceitar melhorias de outras defensorias
Aceitar no core quando a melhoria: (1) serve a mais de uma defensoria ou é neutra; (2) não depende de um sistema ou fornecedor específico; (3) tem testes e documentação; (4) respeita a Política de IA (risco, supervisão humana, aviso ao usuário) e a LGPD; (5) tem dono para manutenção. Caso contrário, vira plugin mantido por quem propôs.

## 6. Segurança e dados pessoais
- Nenhum dado de assistido, segredo ou chave no repositório; chaves de IA e nuvem sempre por variável de ambiente, **contas próprias de cada defensoria**.
- Cada defensoria opera a própria instância e é controladora dos próprios dados; o código compartilhado não leva dado de cidadão.
- Dependências e segredos verificados na esteira; vulnerabilidade reportada por canal privado.
- Cada instância precisa cumprir a Política de IA do seu órgão (inventário, classificação de risco, EPD); o cadastro da MarIA na DPRJ ainda está com risco "a confirmar".

## 7. Licença e propriedade
- Propriedade intelectual da DPRJ (premissa do doc do Iran) com **cessão/licença de uso** às demais defensorias.
- Opções para decidir com o jurídico: (a) código aberto público com licença permissiva (MIT/Apache-2.0) ou copyleft (AGPL-3.0, que obriga devolver melhorias de quem hospeda); (b) repositório fechado ao consórcio de defensorias, sob ACT. A Política de IA prefere código aberto quando viável, mas o contrato com a COPPE pode limitar.
- Contribuições recebem declaração de que o contribuinte tem direito de ceder o código (CLA simples ou DCO).

## 8. Relação com a COPPE
- O contrato atual (5.700 PF e 16.200 USTs; base de 1.350 USTs/mês) foi dimensionado para o Rio: **não paga integração exclusiva de outra defensoria** (Solar, novo broker).
- Papel da COPPE no core: manutenção e evolução do que serve ao Rio e à generalização aprovada; revisão de PR de terceiros precisa estar prevista (horas ou UST) ou fica limitada por teto.
- Trabalho específico da Bahia: equipe própria, fábrica própria ou convênio direto.
- Pergunta do Iran ainda aberta: se um PR de terceiro quebrar algo, a COPPE corrige? Proposta: corrige o que o core quebrou; adapter quebrado é do dono do adapter.

## 9. Proteção da equipe (mitigação do Iran)
Ondas com teto de horas (1º mês com até 5 encontros e 2 treinamentos, sugestão do Diogo); ponto focal único; SLA de 5 dias úteis para dúvidas técnicas e assuntos síncronos na reunião semanal; esteira automática antes da revisão humana; documentação obrigatória; registro mensal das horas gastas para recalibrar o teto. Detalhe nas respostas propostas aos comentários do Iran.

## 10. Administração técnica do repositório (foco do Icaro)
Proposta inicial; premissas a confirmar com o Braida estão marcadas.

### Estrutura
- **Repositório central do core** na organização da DPRJ (hoje a MarIA está em `dgd-dprj/maria-langgraph-pp`), sob gestão do COILAB. Visibilidade (pública ou privada) depende da decisão de licença.
- **Adapters** como pacotes separados (workspaces do npm) dentro do mesmo repositório enquanto houver poucos (Verde, Tykhe), ou em repositórios próprios de cada defensoria quando ela quiser autonomia (ex.: `adapter-solar` da DPBA). O core publica as interfaces; o adapter externo depende delas por versão.
- Arquivos de governança na raiz: `GOVERNANCE.md` (papéis e decisões), `CONTRIBUTING.md` (fluxo de PR), `SECURITY.md` (canal privado de vulnerabilidade), `CODEOWNERS` e uma pasta de decisões de arquitetura (ADRs).

### Acesso (menor privilégio)
| Perfil | Permissão |
|---|---|
| Defensorias parceiras | Fork + PR; leitura do core |
| Ponto focal de cada defensoria | Triagem de issues; escrita só no repositório do próprio adapter |
| Mantenedores (COILAB, Braida/COPPE) | Escrita e merge no core |
| Administradores | 2 pessoas da DPRJ, com autenticação em dois fatores obrigatória |

### Regras da branch `main` (proteção)
- Merge só por PR; sem push direto nem force push.
- Ao menos 1 aprovação de mantenedor e aprovação do dono do código via `CODEOWNERS` (ex.: `adapters/solar/` é da DPBA; `core/` e fluxos da DPRJ são dos mantenedores).
- Checagens obrigatórias verdes e branch atualizada antes do merge.
- Histórico linear (squash), commits no padrão convencional para gerar o changelog.

### Esteira (CI) antes da revisão humana
1. Lint, tipos e testes unitários.
2. **Testes de contrato das interfaces**: todo adapter (Verde, Solar, broker) precisa passar na mesma suíte; assim PR de adapter não quebra o core e vice-versa.
3. Verificação de segredos e de dependências (vulnerabilidades e licenças).
4. Build da imagem Docker e teste de subida (Node.js, PostgreSQL, Redis).
5. Checagem de migrações de banco: versionadas, reversíveis e compatíveis com a versão anterior.
6. Exigência de documentação: PR que muda comportamento sem atualizar `docs/` falha na checagem (ou revisor marca o item no template do PR).

### Versionamento e release
- Semver para o core e para as interfaces; mudança incompatível de interface só em versão maior, com aviso prévio.
- Tags assinadas, changelog automático e imagem Docker publicada por release; ramos `release/x.y` para correções das versões ainda suportadas.
- Configuração por variáveis de ambiente e por banco (fluxos, sumários, petições, chaves de IA), de modo que cada defensoria não precise de fork do core.
- Instâncias de cada defensoria só atualizam por release, nunca pela `main`.

### Fluxo de issues e SLA
- Modelos de issue (bug, proposta de feature, dúvida) e rótulos por defensoria e por área (core, adapter, fluxo, infra).
- Triagem semanal (reunião de quarta) e resposta em até 5 dias úteis; o que for síncrono vai para a reunião.
- Teto de PRs de terceiros em revisão por sprint.

### Respostas diretas (modelo recomendado: fork + upstream, adapters como plugin)
- **Branch separada por defensoria?** Não no repositório central. Branch longa por defensoria vira divergência permanente e cada atualização do core vira merge manual. Cada defensoria trabalha no **próprio fork** e traz o que é reutilizável por PR; o que é só dela fica no plugin/adapter e na configuração (fluxos, petições e sumários no banco), sem tocar no core.
- **Como o código muda se outra defensoria adaptar?** O core só muda se a adaptação exigir um novo ponto de extensão (interface). Nesse caso a defensoria propõe a interface por issue/PR; o resto é plugin no repositório dela. O Verde passa a ser só mais um adapter, mantido pela DPRJ.
- **Como avaliar as modificações?** Em duas camadas: (1) esteira automática, incluindo os testes de contrato das interfaces; (2) revisão humana do mantenedor, com os critérios da seção 5 (serve a mais de uma defensoria, sem dependência de sistema específico, testes, documentação, Política de IA e LGPD).
- **Feature reutilizável criada por outra defensoria?** Ela abre issue com a proposta, depois PR do fork para o core. Se passar nos critérios, entra com squash na `main` e sai na próxima release; todas as defensorias recebem ao atualizar. Se for específica, fica como plugin dela. A DPRJ também pode adotar o plugin de outra como "plugin da comunidade" mantido por quem o criou.
- **GitHub ou GitLab?** Recomendação: **GitHub**, porque a MarIA já está na organização `dgd-dprj`, o fluxo de fork e PR é o mais conhecido por quem contribui de fora, e proteção de branch, `CODEOWNERS`, Actions e Dependabot cobrem a esteira. GitLab (de preferência instalado em infraestrutura própria) só faz sentido se houver exigência de soberania dos dados do código ou norma interna. O modelo acima funciona igual nos dois.

### Pontos técnicos a confirmar
- O Ports and Adapters já existe no código ou há acoplamento ao Verde/Tykhe? (levantamento do Braida)
- Monorepo com workspaces ou repositórios separados por adapter?
- O repositório atual contém algo que impeça abrir para terceiros (dados, segredos no histórico, credenciais)? Antes de qualquer abertura, rodar varredura de segredos no histórico inteiro.
- Quem administra a organização no GitHub e quem fica com a segunda chave de administração?

## Perguntas em aberto para a reunião das 14h
1. Open source **público** ou aberto só entre defensorias (consórcio)? Quem decide a licença (jurídico/Diogo)?
2. Modelo técnico: centralizado, segregado ou híbrido (fork controlado)? Minha inclinação: híbrido, com core central e adapters nos repositórios de cada defensoria.
3. Quem é o mantenedor oficial do core: COILAB, COPPE ou os dois? Quantas horas por mês a COPPE pode dedicar a revisão de PR de terceiros dentro do contrato?
4. Como formalizar: ACT por defensoria ou um termo de adesão único a este modelo, já que DF, RS e ES também têm interesse?
5. Que cadência de releases e que versão mínima suportada são viáveis para a equipe atual?
6. O desacoplamento (Ports and Adapters) já existe no código? Braida confirma antes de abrir o repositório.
7. Comitê de governança: quem participa e com que periodicidade (sugestão: assunto semanal na reunião de quarta)?
8. Quem avalia segurança e privacidade dos PRs externos (CGSI/EPD) e qual o prazo?
9. O que a DPRJ oferece sem custo (documentação, homologação) e o que é contrapartida das demais defensorias?
10. Repositório: monorepo com adapters em pacotes ou um repositório por adapter? O histórico atual está limpo de segredos?

## Relacionado
- [[Compartilhamento da MarIA com a Bahia]]
- [[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]]
- [[Maria]] (inventário de IA)
- [[Resolução DPRJ - Política de IA]]
