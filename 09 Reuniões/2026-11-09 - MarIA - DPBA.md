---
tipo: reuniao
data: 2026-11-09
hora: "16:01"
convidados:
  - ICARO LUIZ ALBAR EDUARDO
  - Filipe Braida do Carmo
  - Gustavo Pinto
  - CAMILA MAURA MOREIRA DA SILVA
  - IRAN TEIXEIRA DE OLIVEIRA
falaram:
  - IRAN TEIXEIRA DE OLIVEIRA
  - CAMILA MAURA MOREIRA DA SILVA
  - Filipe Braida do Carmo
  - Gustavo Pinto
  - ICARO LUIZ ALBAR EDUARDO
projeto: "[[Compartilhamento da MarIA com a Bahia]]"
fonte: https://docs.google.com/document/d/1cgpKEshcT5D7sN6A3HRqAT6-vfRmTFCnpTKSlBjCXyo/edit
gravacao: 
origem: anotações automáticas do Gemini (Google Meet)
tags:
  - reuniao
  - maria
---

# MarIA - DPBA (09/11)

> Ata gerada automaticamente pelo Gemini no Google Meet; pode conter erros de nomes e termos. Transcrição completa em [[2026-11-09 - MarIA - DPBA (transcrição)]].

## Resumo

Reunião analisou melhorias no MarIA com foco na auditoria e expansão para outras defensorias.  
  
**Ajustes Operacionais e Auditoria**  
A equipe corrigiu falhas no cancelamento indevido de agendamentos e atualizou a biblioteca de auditoria sob licença MIT. Decidiu-se implementar uma verificação passiva de cancelamentos para evitar retrabalho.  
  
**Integração e Desacoplamento**  
Discutiu-se a alta dependência do sistema Verde e a flexibilização do GovBR para facilitar a adoção do MarIA por outras defensorias. A criação de uma interface genérica de broker foi descartada por inviabilidade.  
  
**Planejamento e Expansão**  
Alinhou-se a priorização das APIs de pré-atendimento para a próxima sprint e a estratégia de cessão do sistema para a Defensoria da Bahia. O motor de respostas terá um teste gradual de 1 porcento em produção.

## Decisões

### Alinhada

  - **Subida do aplicativo para produção** Ficou definido que a nova versão do aplicativo será subida diretamente para produção, mantendo o envio de fotos como método alternativo em caso de falhas.
  - **Proibição de criação de casos fora do MarIA** Ficou proibido criar casos pessoais ou paralelos manualmente para o Naddia fora da plataforma MarIA a partir de agora.
  - **Verificação passiva de cancelamentos de agendamento** Decidiu-se adotar uma verificação passiva no MarIA, checando a validade do agendamento sempre que o analista entrar na tela de atendimento, descartando rotinas ativas automatizadas.
  - **Priorização das APIs do Braida na sprint** Ficou acordado priorizar 100% das tarefas de IntegraAPI do Braida na equipe do Emerson para a sprint do dia 17.
  - **Abordagem de transição assistida para a Bahia** A diretriz de repasse total de código sem suporte foi descartada em favor de fornecer um conjunto mínimo de alterações estruturais para viabilizar a adoção pela Defensoria da Bahia.
  - **Implementação do recurso Gov.BR desativável** Ficou acordado implementar o recurso de tornar o Gov.BR desativável no sistema para facilitar a expansão para outras defensorias.
  - **Abandono da generalização prévia de brokers** A equipe decidiu não investir esforço na criação de uma camada de abstração genérica para troca de brokers, deixando essa adaptação por conta da empresa contratada.
  - **Desacoplamento do sistema Maria em relação ao Verde** Ficou acordado que o sistema Maria será adaptado para funcionar de ponta a ponta sem a dependência direta do Verde e com a remoção de partes do GolBR.
  - **Lançamento antecipado da tela de distribuição** A equipe definiu liberar a funcionalidade de distribuição separadamente do acordo extrajudicial para resolver problemas imediatos na homologação.
  - **Implementação gradual do motor de automação** Ficou estabelecido que o motor de automação será colocado no ar para o fluxo de alimentos com testes A/B em pequena escala antes de avançar para o recurso de múltiplos chats.

## Próximas etapas (sugeridas pelo Gemini)

- [Filipe Braida do Carmo] Atualizar o ID do caso no banco de dados: para o caso antigo criado por Rut, após receber a identificação correspondente para permitir que a usuária prossiga normalmente.
  - [Filipe Braida do Carmo] Verificar com o Emerson a priorização das tarefas de pré-atendimento: para alinhar os ajustes necessários e a liberação das chamadas de API antes do final da sprint.
  - [Filipe Braida do Carmo] Incorporar o aviso de pré-atendimento: para o estado verde e a inclusão no prontuário sobre a conclusão ou envio do atendimento.
  - [Filipe Braida do Carmo] Enviar mensagem para Emerson: em chat privado para conversar sobre o alinhamento das tarefas.
  - [Filipe Braida do Carmo] Implementar o atendimento da Maria sem o Verde: de ponta a ponta e remover os elementos do GOV.BR do sistema para garantir o funcionamento adequado conforme alinhado na reunião.
  - [Filipe Braida do Carmo] Conversar com Gustavo e Talita: para alinhar a implementação do acordo na Maria e esclarecer pontos específicos sobre o funcionamento.
  - [Filipe Braida do Carmo] Preparar a Maria: para realizar um novo teste no motor de atendimento com o fluxo de alimentos utilizando uma porcentagem inicial reduzida.
  - [Filipe Braida do Carmo] Atualizar a documentação de deploy: e a parte técnica do sistema para esclarecer o funcionamento interno por trás dos panos.
  - [Filipe Braida do Carmo] Fazer o motor funcionar: reduzindo o escopo de trabalho para garantir que os fluxos passem corretamente pelo sistema.
  - [Camila Maura Moreira da Silva] Identificar o atendente da CRC responsável pelo cancelamento: e conversar com Filipe sobre o ocorrido para apurar a falha no agendamento do NAD.
  - [Gustavo Pinto] Solicitar a inclusão da verificação de cancelamento na API: para garantir que o sistema retorne o status atualizado e exiba a informação corretamente na tela de atendimento.
  - [Unassigned] Priorizar as demandas do Braida: nas tarefas atribuídas a Emerson para a sprint da próxima terça-feira com foco nas entregas de fim de ano.
  - [CAMILA MAURA MOREIRA DA SILVA] Enviar mensagem de apoio a Ricardo: para alinhar as expectativas e garantir que eles não sejam pegos de surpresa.

## Detalhes

**Problema de Cancelamento Indevido de Agendamento pela CRC**: Foi apontado por Camila Maura Moreira da Silva e Filipe Braida do Carmo que um atendente da CRC cancelou indevidamente o agendamento de uma assistida no NAD sem consultar a equipe, o que resultou na exclusão automática do caso não processual correspondente no sistema Verde (00:02:20) (00:09:44). O problema gerou retrabalho para a analista Rut, que havia preparado todo o dossiê da petição, mas perdeu o vínculo com o caso (00:03:29) (00:09:44).

**Avaliação dos Testes em Homologação e Produção**: Discutiu-se que o aplicativo enfrentava falhas no ambiente de homologação, mas Camila Maura Moreira da Silva ressaltou que o sistema já operava sem registros de problemas em produção e que a equipe não ficaria testando indefinidamente em homologação (00:03:29). Iran Teixeira de Oliveira observou que mais de 60 testes já haviam sido gerados, indicando uma validação robusta (00:04:20).

**Desenvolvimento e Licenciamento da Biblioteca de Auditoria**: Filipe Braida do Carmo explicou que projetou uma biblioteca própria para facilitar a rastreabilidade e a geração de logs auditáveis. Como a biblioteca original de um autor francês utilizava a licença GPL e geraria contaminação legal, Filipe Braida do Carmo realizou um *fork*, atualizou o *framework* e disponibilizou o código sob a licença MIT (00:05:52).

**Mecanismos de Rastreabilidade e Auditoria de Ações**: Filipe Braida do Carmo e Camila Maura Moreira da Silva destacaram que a tela de auditoria permite rastrear ações detalhadas com precisão, identificando o uso de aparelhos e horários específicos (como operações em dispositivos Android em Nova Iguaçu), o que já auxiliou na apuração de responsabilidades internas (00:04:57) (00:08:02).

**Tratamento e Correção de Casos Criados Manualmente**: Diante da situação em que a analista Rut criou um caso manualmente devido ao cancelamento do agendamento pela CRC, Gustavo Pinto e Filipe Braida do Carmo alinharam uma solução técnica (00:10:32) (00:12:41). Ficou acordado que Filipe Braida do Carmo fará a alteração direta do identificador no banco de dados para reutilizar o caso criado, e Camila Maura Moreira da Silva reforçou a proibição de criação de casos por fora do MarIA (00:12:41) (00:23:01).

**Decisão sobre a Verificação Passiva de Cancelamentos no Sistema Verde**: O grupo debateu se o MarIA deveria ser notificado ativamente ou passivamente sobre cancelamentos de agendamentos na CRC (00:14:24) (00:17:46). Gustavo Pinto e Filipe Braida do Carmo avaliaram as opções, e decidiu-se implementar uma verificação passiva no MarIA toda vez que a analista acessar a tela de atendimento, exibindo um alerta caso o agendamento tenha sido cancelado, medida considerada suficiente devido à baixa frequência do problema (cerca de uma a duas ocorrências mensais) (00:17:46) (00:19:04).

**Priorização das APIs de Pré-Atendimento para a Próxima Sprint**: Camila Maura Moreira da Silva cobrou o alinhamento com a equipe de Emerson para garantir que as APIs de pré-atendimento solicitadas por Filipe Braida do Carmo recebam prioridade de cem por cento na próxima *sprint* programada para a terça-feira da semana seguinte, dia 17 (00:23:54) (00:31:31).

**Alinhamento do Calendário de Entregas e Prazos para Dezembro**: Discutiu-se a necessidade de concluir as entregas do projeto ainda em dezembro, antes do início do recesso de fim de ano, para atender às expectativas da Defensoria Pública do Estado do Rio de Janeiro (DPG) (00:32:18) (00:34:35). Gustavo Pinto pontuou as datas das aberturas de *sprint* anteriores para contextualizar o fluxo de demandas (00:27:13) (00:29:40).

**Definição sobre o Canal de Envio de E-mails**: Filipe Braida do Carmo apresentou alternativas para o envio de e-mails, sugerindo que o MarIA realize os disparos diretamente ou passe as requisições pelo sistema Verde. Gustavo Pinto manifestou preferência por delegar o envio diretamente ao MarIA para evitar centralizações desnecessárias no Verde, embora a passagem pelo Verde permitisse auditoria centralizada (00:32:57).

**Estratégia de Expansão e Cessão do MarIA para a Defensoria da Bahia**: Camila Maura Moreira da Silva relatou que a Defensoria da Bahia demonstrou interesse na ferramenta e aguarda retornos sobre códigos e integrações com o GovBR (00:35:35). Gustavo Pinto e a equipe concluíram que a abordagem de simplesmente entregar o código sem preparação resultaria em fracasso, sendo indispensável fornecer um conjunto mínimo de ajustes estruturais e firmar termos formais de cooperação e cessão (00:36:30) (00:38:12).

**Definição dos Critérios Mínimos para o Desacoplamento do Sistema**: Filipe Braida do Carmo apresentou uma lista de critérios focada nos elementos bloqueadores para permitir que outras defensorias utilizem o MarIA sem depender de toda a infraestrutura do Rio de Janeiro (00:40:55) (00:43:19). Icaro Luiz Albar Eduardo concordou que o MarIA deve buscar independência máxima de ferramentas externas para facilitar futuras adoções (00:46:15).

**Avaliação da Utilidade dos Assuntos Internos no Pré-Atendimento**: Filipe Braida do Carmo questionou a relevância de manter a modalidade de assuntos internos no pré-atendimento (solicitada anteriormente pela Doutora Suha), argumentando que o mecanismo de assuntos personalizados já supre essa demanda (00:47:56). Camila Maura Moreira da Silva e Filipe Braida do Carmo concordaram que a funcionalidade pode ser descartada para simplificar o sistema (00:49:19).

**Desacoplamento e Flexibilização do Uso do GovBR**: Filipe Braida do Carmo propôs tornar a integração com o GovBR desativável no MarIA para atender a defensorias que não utilizem o serviço. Icaro Luiz Albar Eduardo e Iran Teixeira de Oliveira pontuaram que o esforço de implementação é pequeno e que os links e botões associados simplesmente desaparecerão da interface caso o GovBR não esteja ativo (00:50:43) (00:54:42).

**Complexidade do Acoplamento Funcional com o Sistema Verde**: Filipe Braida do Carmo destacou que, ao contrário do GovBR, desligar o sistema Verde afeta profundamente a lógica de negócios e o fluxo operacional do MarIA, exigindo regras condicionais complexas para avançar etapas processuais sem um caso verde vinculado (00:52:23) (00:55:28).

**Desafios na Padronização de Provedores de Mensagens Externos**: Icaro Luiz Albar Eduardo e Filipe Braida do Carmo debateram os problemas relacionados à falta de padronização nas APIs e provedores de mensagens de terceiros (como os da Meta), apontando que tal cenário representa um desafio de integração tão relevante quanto o acoplamento com o sistema Verde (00:55:28).

**Proposta de Camada de Abstração para Brokers**: Filipe Braida do Carmo sugeriu criar uma interface e uma camada acima dos brokers para dar flexibilidade caso novas empresas forneçam soluções diferentes. Camila Maura Moreira da Silva ponderou que a contratação de uma nova empresa está em andamento para o próximo ano (00:57:31) (00:59:03). Gustavo Pinto argumentou que a empresa fornecedora pode não cumprir o padrão estabelecido, tornando a customização imprevisível (00:59:03). A decisão final foi de que a criação de uma interface genérica de broker não compensa o esforço diante da baixa frequência de troca de ferramentas (01:02:57).

**Desafios na Migração e Troca de Brokers**: Filipe Braida do Carmo e ICARO LUIZ ALBAR EDUARDO apontaram que migrar de broker envolve problemas complexos, como divergências de IDs de mensagens e adaptações implementadas para a Tatic (00:59:42). Camila Maura Moreira da Silva informou que a contratação da nova empresa está na fase de Estudo Técnico Preliminar e Termo de Referência, com conclusão prevista para meados do próximo ano (01:01:07). A conclusão foi de que a administração pública não troca de broker frequentemente, tornando inviável o esforço de generalização (01:02:57).

**Suporte Técnico e Stack de Desenvolvimento da Nova Empresa**: ICARO LUIZ ALBAR EDUARDO e Filipe Braida do Carmo debateram se a nova empresa contratada receberia suporte para integrar sua aplicação ao sistema Maria. Filipe Braida do Carmo esclareceu que o suporte fornecido abrangerá apenas a interface de programação de aplicações (API) e o webhook, sem orientar a implementação de regras de negócio na aplicação externa (01:03:51) (01:05:05). Camila Maura Moreira da Silva ressaltou que ainda não houve reuniões com a equipe externa para compreender o stack tecnológico e a composição da equipe (01:03:51).

**Dependências do Pré-Atendimento e Assuntos**: Filipe Braida do Carmo levantou problemas operacionais do pré-atendimento, que exige assuntos cadastrados originados do Solar e do Verde (01:05:45). Camila Maura Moreira da Silva comentou que a defensoria externa provavelmente desejará utilizar todos os fluxos de pré-atendimento, embora ainda não haja clareza se implementarão o Maria para todos os processos ou apenas para ações específicas, como pensão de alimentos ou divórcio (01:06:36).

**Acoplamento do Sistema Maria com o Verde**: Filipe Braida do Carmo explicou que o Maria possui forte acoplamento com o sistema Verde para gerenciamento de organização, lotação e identificadores de órgãos (01:08:27). Gustavo Pinto acrescentou que a autenticação recupera todas as informações de lotação diretamente das regras do Verde (01:10:06). Camila Maura Moreira da Silva avaliou que a desacoplagem exigirá esforço, mas trará benefícios para futuras defensorias públicas que desejem utilizar o sistema (01:18:52).

**Configuração de Fuso Horário nas Consultas**: Filipe Braida do Carmo explicou que o sistema utiliza carimbo de data/hora (timestamp) em tempo universal coordenado (UTC) no banco de dados, com conversão fixa para o fuso horário de América/São Paulo nas consultas. ICARO LUIZ ALBAR EDUARDO alertou sobre possíveis divergências caso os servidores fiquem localizados na Virgínia (01:11:37). Filipe Braida do Carmo concordou que a conversão poderá ser migrada para uma variável de ambiente no futuro (01:12:17).

**Independência do Sistema Maria em Relação ao Verde**: Filipe Braida do Carmo detalhou que funcionalidades como petições, agendamentos e personagens dependem diretamente de abas do Verde (01:16:49). IRAN TEIXEIRA DE OLIVEIRA confirmou que os fluxos, conversas, mudanças de status e criação de petições possuem forte integração crítica com o Verde (01:15:02). A equipe discutiu que remover essas dependências e permitir fluxos de ponta a ponta sem o Verde é viável, facilitando a adoção por outras instituições (01:17:53).

**Encaminhamentos e Ajustes Mínimos para a Defensoria da Bahia**: Gustavo Pinto e Camila Maura Moreira da Silva alinharam que o pré-atendimento tem prioridade superior a ajustes genéricos para outras defensorias (01:21:22). Filipe Braida do Carmo comprometeu-se a executar ajustes nas duas semanas seguintes, desligando o Verde para permitir um fluxo de ponta a ponta e removendo a dependência do GolBR (01:22:57).

**Implementação da Distribuição e Acordos Extrajudiciais**: Filipe Braida do Carmo relatou que a funcionalidade de distribuição está pronta e aguardando a data de implantação em produção junto com o Verde. Sobre o acordo extrajudicial, Filipe Braida do Carmo conversou com Ciano e planejou alinhar os detalhes com Gustavo Pinto e Talita, mantendo a distribuição pronta para ser liberada (01:24:52) (01:27:13).

**Plano de Implantação Gradual do Motor de Respostas**: Filipe Braida do Carmo propôs colocar o motor de respostas em produção para o fluxo de alimentos, realizando um teste A/B com uma parcela inicial pequena (como 1%) dos atendimentos e aumentando gradativamente. Camila Maura Moreira da Silva concordou que testar o motor antecipadamente ajuda a identificar e resolver problemas antes da liberação do fluxo de divórcio (01:28:06) (01:33:04).

**Suporte a Múltiplos Chats por Atendimento**: Filipe Braida do Carmo propôs uma melhoria estrutural para permitir múltiplos contatos e telefones associados a um único atendimento, criando abas de chat (01:28:55). Camila Maura Moreira da Silva e Gustavo Pinto destacaram que essa funcionalidade resolverá os problemas recorrentes de assistidas que mudam de número e facilitará o contato com a parte contrária nos núcleos de atuação (NAD e PAR) (01:30:38).

**Interrupção Inesperada pela Gestão da Defensoria**: Durante a reunião, Camila Maura Moreira da Silva relatou a chegada imprevista da defensoria pública geral e da equipe de gestão para uma visita técnica, abordando planos de lançamento do portal em dezembro (01:34:15) (01:35:49).

**Alinhamento de Expectativas e Entrega de Código para a Bahia**: Gustavo Pinto, Camila Maura Moreira da Silva e Filipe Braida do Carmo expressaram preocupação com o prazo de dezembro almejado pela liderança da Bahia, visto que a integração com o broker e o Solar envolve alta complexidade técnica (01:39:06) (01:40:28). A equipe decidiu fornecer documentação e código, alinhar expectativas com a liderança para evitar gargalos e programar treinamentos, confirmando que a sessão de treinamento de sexta-feira será conduzida por Jane, com o apoio de Filipe Braida do Carmo e ICARO LUIZ ALBAR EDUARDO (01:38:07) (01:41:58).

## Relacionado
- [[Compartilhamento da MarIA com a Bahia]]
- [[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]]
- [[Maria - atendimento automatizado]]
- [[2026-11-09 - MarIA - DPBA (transcrição)]]
- [[2026-10-16 - Compartilhamento MarIA]]
