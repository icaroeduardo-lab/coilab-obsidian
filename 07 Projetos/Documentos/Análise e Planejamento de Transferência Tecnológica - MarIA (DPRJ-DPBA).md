---
tipo: documento
autor: IRAN TEIXEIRA DE OLIVEIRA
data: 2026-10-15
atualizado_em: 2026-10-16
projeto: "[[Compartilhamento da MarIA com a Bahia]]"
fonte: https://docs.google.com/document/d/1a9Uhd9q4433EqQkZUcb0aarwehYJ23PrTLt0reFCztg/edit
tags:
  - documento
  - maria
---

# Análise e Planejamento de Transferência Tecnológica: Sistema MarIA (DPRJ ➔ DPBA)

> Cópia do documento do Iran no Google Drive, de 16/10/2026. O original continua sendo a versão de trabalho; os comentários abertos estão no fim desta nota. Segundo o Iran, a parte a partir da seção 4 é sugestão do Gemini, e a Camila observou que o documento é praticamente um ACT.

## 1. Objetivo
Estabelecer as diretrizes, requisitos, responsabilidades e o estudo de impacto para a transferência de conhecimento, implantação e co-desenvolvimento do sistema de atendimento digital **MarIA** da Defensoria Pública do Rio de Janeiro (DPRJ) para a Defensoria Pública do Estado da Bahia (DPBA).

## 2. Aspectos Institucionais e Estruturais (Negócio)
A arquitetura de atendimento da DPRJ pressupõe a existência de órgãos específicos para o fluxo digital. A DPBA precisará espelhar ou adaptar essa estrutura.

- **Núcleo de Atendimento Digital (NAD):** No Rio, o MarIA finaliza o fluxo (Ex: Alimentos, Divórcio), monta o sumário e disponibiliza ao NAD, onde o servidor valida o sumário, gera uma petição e envia para criação de Caso no Verde.
    - *Ação DPBA:* Levantar se existe um órgão correspondente com essa atribuição. Caso não, será necessário criar o órgão no sistema (Solar) e designar servidores (lotação) para recepcionar essas demandas.
- **Polo de Mediação (POMAR):** Casos com potencial de conciliação são direcionados para o POMAR.
    - *Ação DPBA:* Mapear o fluxo de mediação baiano e definir para qual núcleo ou fila sistêmica esses casos serão direcionados.
- **Transbordo Humano (CRC):** Fluxos que não podem ser resolvidos pelo bot são transbordados para atendimento humano na Central de Relacionamento ao Cidadão (CRC).
    - *Ação DPBA:* Estruturar e informar se possuem uma central de teleatendimento/chat humano para receber esse transbordo, definindo regras de horário de atendimento e dimensionamento de equipe.
- **Suporte ao MarIA:** Ter uma equipe para prestar atendimento aos usuários do MarIA internamente (Suporte N1);

## 3. Aspectos Técnicos e de Integração (TI)
A implantação na Bahia exigirá a substituição de diversos componentes periféricos que hoje são acoplados à realidade do Rio de Janeiro.

- **Substituição do Broker de Mensageria:**
    - *Cenário Atual:* A DPRJ utiliza a Tythe (WhatsApp/Webchat) com fluxos de triagem, agendamento e consulta ao Verde.
    - *Desafio:* A DPBA possui outra empresa fornecedora.
    - *Ação Necessária:* A DPBA e sua fornecedora deverão recriar os fluxos de primeiro atendimento no novo broker e integrar via API com o MarIA. O desenvolvimento dessa integração será de inteira responsabilidade da equipe/fornecedor da DPBA.
- **Integração de Sistemas Core (Verde ➔ SOLAR):**
    - *Ação Necessária:* A DPBA precisará desenvolver a camada de integração (APIs) do SOLAR para consumir e enviar dados ao MarIA (criação de casos, agendamentos, consultas de processos).
- **Servidor de Nuvem para hospedar o MarIA:**
    - *Ação Necessária:* A DPBA precisará dispor de um servidor web para hospedar o sistema MarIA ou contratar um (ex.: AWS, Azure, Google Cloud, etc).
- **Modelos de Petição:**
    - As petições geradas pelo MarIA não são feitas por IA generativa, mas sim por modelos parametrizados (templates). A DPBA precisará mapear seus próprios modelos jurídicos e adaptá-los dentro da lógica do sistema, seguindo os padrões do judiciário baiano.
- **Infraestrutura e Contratação de IA (LLMs):**
    - Embora a petição seja modelo pronto, o MarIA utiliza modelos de linguagem (LLMs) para sumarização e outras funcionalidades internas.
    - *Requisito:* A DPBA deverá providenciar **contratação própria** de infraestrutura de nuvem e de chaves de API de IA (ex: OpenAI, Azure, AWS). O código deverá aceitar as chaves da DPBA como variáveis de ambiente, sem onerar os custos da DPRJ.

## 4. Governança de Código e Co-Desenvolvimento (Boas Práticas Node.js/Git)
Para garantir que as alterações da Bahia (ex: integração Solar) não quebrem o sistema do Rio (Verde), e vice-versa, enquanto compartilham inovações do núcleo (core) do MarIA:

- **Desacoplamento por Interfaces (Design Patterns):**
    - Orientação técnica: O código em Node.js deve adotar o padrão de *Adapter/Ports and Adapters*. O *Core* do MarIA não deve saber o que é "Verde" ou "Solar". Ele deve chamar uma interface ISistemaDefensoria. Existirá um módulo adapter-verde (mantido pela DPRJ) e um módulo adapter-solar (mantido pela DPBA).
- **Repositório e Versionamento (Git):**
    - Manter um repositório centralizado sob gestão da DPRJ.
    - A DPBA fará contribuições através de **Pull Requests (PRs)**.
    - **Regras para PR:** Nenhum código sobe para a branch main sem (1) aprovação de no mínimo um desenvolvedor sênior da DPRJ/COPPE, (2) passar em testes automatizados, (3) não alterar regras de negócio exclusivas da DPRJ.
- **Modularização:** Módulos de interesse comum (melhorias na IA, nova feature de UX, refatoração de sumário) são incorporados ao *Core*. Módulos específicos (integração do broker X, sistema Y) viram plugins.
- Com alterações realizadas pela DPBA como fica a manutenção da COPPE, ou seja, se o código "quebrar" a COPPE pode fazer a correção ou se negar a fazer por não ser a responsável pelo bug? *Nota: Se quebrar tem responsabilidade para quem autorizou o merge.*

## 5. Questões Contratuais e Empresa Desenvolvedora (COPPE)
- A propriedade intelectual do código é da DPRJ, permitindo a cessão de uso à DPBA.
- **Blindagem do Contrato:** O contrato atual da DPRJ com a COPPE é dimensionado para as demandas do Rio de Janeiro.
- **Diretriz:** O escopo do contrato da COPPE **não** poderá ser utilizado para desenvolver integrações exclusivas para a Bahia (ex: integrar com o SOLAR ou com o novo Broker).
- *Solução sugerida:* A DPBA deve alocar desenvolvedores próprios, contratar uma fábrica de software própria, ou celebrar um convênio/contrato direto (com a COPPE ou outra) para realizar as adaptações, ficando a cargo da DPRJ apenas a revisão do código (PR) e homologação técnica.

## 6. Transferência de Conhecimento (Business & Lógica)
A DPRJ se compromete a compartilhar sua expertise, mas de forma estruturada para não prejudicar sua rotina:

- Repasse das metodologias de **Linguagem Simples** e Design Legal utilizadas nos fluxos.
- Treinamento sobre a lógica de árvore de decisão e fluxos de atendimento (Alimentos e Divórcio).
- Workshops agendados e limitados a uma carga horária máxima (ex: 20 horas no total), cobrindo o manual arquitetural, fluxo do usuário e governança.

## 7. Estudo de Impacto Operacional na DPRJ (Alerta)
Este é o ponto de maior sensibilidade. A equipe de suporte interno, TI e inovação da DPRJ é enxuta e já atua no limite de sua capacidade com as demandas estaduais.

- **Impacto no Suporte Interno:** O desvio de servidores da DPRJ para reuniões de alinhamento, explicação de fluxos, e suporte "Nível 3" para a DPBA atrasará o cronograma de desenvolvimento interno de novas features (ex: fluxos criminais, de saúde, etc.).
- **Impacto na TI / Code Review:** A revisão técnica de Pull Requests gerados pela equipe da Bahia (ou terceiros deles) exigirá horas de engenheiros de software da DPRJ/COPPE para garantir a integridade do repositório.
- **Mitigação (O que precisamos exigir):**
    1. **Autonomia da DPBA:** A DPBA deve nomear um "Product Owner" e um "Tech Lead" próprios que irão absorver o conhecimento e ser os replicadores na Bahia. A DPRJ não fará suporte direto aos usuários ou desenvolvedores júnior da Bahia.
    2. **SLA de Atendimento:** Estabelecer que a DPRJ responderá dúvidas técnicas em um prazo estendido (ex: até 5 dias úteis), para não interromper sprints de desenvolvimento do Rio.
    3. **Documentação Mútua:** Toda nova feature desenvolvida pela Bahia e acoplada ao repositório deverá vir acompanhada de documentação técnica robusta, reduzindo o custo de manutenção futura pela DPRJ.

### Próximos Passos (Checklist Interno DPRJ)
1. Agendar reunião de alinhamento (Kick-off) com a DPBA apresentando as premissas deste documento.
2. Exigir que a DPBA apresente o organograma deles (quem será o PO, o Tech Lead e a equipe/empresa de desenvolvimento que atuará do lado deles).
3. Criar o documento de "Acordo de Cooperação Técnica (ACT)" constando expressamente as limitações de uso do contrato da COPPE e as regras de governança de código.

## Comentários abertos no documento
| Trecho | Comentário do Iran | Para quem |
|---|---|---|
| Servidor de nuvem | Verificar com Braida se a arquitetura precisa ser AWS ou se há flexibilidade. Perguntar sobre S3, Redis, LLM e requisitos de máquina. | Braida |
| Petições não são feitas por IA generativa | Verificar com o Braida. | Braida |
| Contratação própria de nuvem e chaves de IA | Validar. | |
| Ports and Adapters | Verificar se essa parte já funciona dessa maneira. | |
| Modularização em Core e plugins | Ver com o Icaro se isso é comum e funciona bem em Node.js. | Icaro |
| Seção 5 (contrato com a COPPE) | Essa situação temos que dar uma pensada. | Diogo, Frederico |
| Seção 7 (impacto e mitigação) | Vamos pensar e pesquisar como podemos organizar isso. | Icaro |
| Próximos passos | Daqui pra frente é sugestão do Gemini. Camila: "Esse doc é praticamente um ACT". | Camila |

## Relacionado
- [[Compartilhamento da MarIA com a Bahia]]
- [[2026-10-15 - Compartilhamento MarIA - Melhores práticas]]
- [[2026-10-16 - Compartilhamento MarIA]]
