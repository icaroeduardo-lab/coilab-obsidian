---
tipo: reuniao
data: 2026-10-23
hora: "13:55"
convidados:
  - Diogo Leite Mesquita
  - ICARO LUIZ ALBAR EDUARDO
  - Talita Vieira Ribeiro
  - Gustavo Pinto
  - CAMILA MAURA MOREIRA DA SILVA
  - Filipe Braida do Carmo
  - ANDERSON MARINOVIC
falaram: 
projeto: "[[Maria - atendimento automatizado]]"
fonte: https://docs.google.com/document/d/1LkZID_zz_mz4cbZINXdIt1fwl-BpSVBmArw2BIZnQls/edit
gravacao: 
origem: anotações automáticas do Gemini (Google Meet)
tags:
  - reuniao
  - maria
---

# Pré-atendimento - Fase Varas (23/10)

> Ata gerada automaticamente pelo Gemini no Google Meet; pode conter erros de nomes e termos. A transcrição completa ficou só no Google Docs (aba "Transcrição" do documento da fonte).

## Resumo

Reunião de alinhamento com definição da regra de trinta dias e ajustes de integração de documentos.  
  
**Regra de trinta dias**  
Definida a regra temporal de trinta dias para disparo de mensagens de solicitação de documentos.  
  
**Integração e exclusão**  
Alinhada a exclusão automática de documentos associados a agendamentos cancelados.  
  
**Atualizações do sistema**  
Demonstrada nova interface com declarações de residência e validações de assinatura.

  
  

## Decisões

### Alinhada

  - **Restrição temporal de trinta dias para envio de links** O envio do link para o assistido enviar documentos no pré-atendimento passará a ocorrer automaticamente apenas para agendamentos com até trinta dias de antecedência.
  - **Exclusão de documentos após cancelamento de agendamento** Os documentos associados a um pré-atendimento devem ser excluídos do sistema Maria caso o agendamento correspondente seja cancelado.
  - **Manutenção do envio automático sem curadoria prévia** O fluxo de documentos manterá o envio automático sem exigir uma etapa de curadoria prévia pelos operadores, permitindo edições posteriores quando necessário.
  - **Janela temporal de trinta dias** O envio de links de pré-atendimento aos assistidos foi restrito a agendamentos ocorridos em uma janela de até trinta dias.
  - **Sincronização integral de dados passivos** Ficou determinado que todo o passivo de documentos anterior à nova regra temporal será sincronizado integralmente.
  - **Diretrizes para cancelamentos e reagendamentos** O cancelamento de agendamentos exige a exclusão dos documentos no Verde e no Maria, enquanto o reagendamento requer o reapontamento do pré-atendimento.
  - **Migração da tela de solicitação documental** A construção da tela de solicitação de documentos foi deslocada do Verde para o Maria por meio de redirecionamento no prontuário.
  - **Priorização do pré-atendimento das varas** O fluxo de pré-atendimento para as varas foi estabelecido como prioridade imediata de entrega em relação às demandas de divórcio.
  - **Adoção da reutilização de documentos no Maria** Ficou acordado implementar a reutilização de documentos que ainda estão no sistema Maria para novos pré-atendimentos.
  - **Adiamento da sincronização total de dados** Ficou acordado aguardar a mudança da regra de 30 dias para realizar a sincronização completa dos dados.
  - **Inclusão de motivo de encerramento de atendimento** Ficou acordado adicionar a opção de falta de resposta do assistido entre os motivos de encerramento de atendimento.

  

### Arquivada

  - **Rejeição de opção de bloqueio no Maria** A proposta de criar uma opção de bloqueio de acesso exclusiva no Maria sem passar pelo Verde foi descartada pelo grupo.

## Próximas etapas (sugeridas pelo Gemini)
Ainda não viraram notas em `11 Tarefas`; criar uma nota por tarefa (Modelo - Tarefa) com `origem` apontando para esta reunião.


  - \[Gustavo Pinto\] Atualizar fluxo produção: Priorizar a entrada em produção das alterações no fluxo de exibição de status dos documentos.
  - \[Gustavo Pinto\] Ajustar envio link: Implementar regra de envio de link para envio de documentos apenas para agendamentos com intervalo de 30 dias.
  - \[Gustavo Pinto\] Excluir documentos cancelados: Configurar a exclusão automática dos documentos armazenados no sistema Maria e no prontuário Verde quando um agendamento for cancelado.
  - \[Talita Ribeiro\] Ajustar ícone agenda: Alterar a cor ou o design do ícone de pre-atendimento na tela da pauta para que nao pareça desativado.
  - \[Gustavo Pinto\] Automatizar Envio Documentos: Coordenar com Talita, Camila e Braida a transição do fluxo de envio de documentos para o modo automático definitivo.
  - \[Talita Ribeiro\] Adicionar Atalho Documentos: Avaliar e implementar uma aba ou link de acesso rápido para documentos vinculados a casos e pré-atendimentos.
  - \[Talita Ribeiro\] Criar API documentos: Desenvolver interface de programação para consulta de documentos no sistema Verde.
  - \[Filipe Braida do Carmo\] Adicionar botão sincronização: Incluir funcionalidade de sincronizar tudo para permitir a atualização de múltiplos arquivos simultaneamente.
  - \[Talita Ribeiro\] Ajustar interface edição: Alterar o sistema Verde para explicitar a possibilidade de edição de documentos no Maria.
  - \[Talita Ribeiro\] Atualizar envio links: Ajustar o fluxo de envio para disparar links apenas quando o agendamento estiver no período de 30 dias.
  - \[O grupo\] Vincular documentos prontuário: Organizar e realizar a vinculação dos documentos ao prontuário do assistido e aos respectivos casos no sistema.
  - \[Filipe Braida do Carmo\] Sincronizar passivo: Sincronizar todos os documentos do passivo conforme a regra estabelecida.
  - \[Talita Ribeiro\] Confirmar assunto: Verificar a obrigatoriedade da indicação de assunto no pré-atendimento.
  - \[Talita Ribeiro\] Validar reagendamento: Confirmar com Taiana o comportamento do sistema em casos de mudança de pauta ou assunto durante reagendamentos.
  - \[Talita Ribeiro\] Criar APIs: Desenvolver as APIs necessárias no sistema Verde para listagem de documentos.
  - \[Filipe Braida do Carmo\] Implementar documentos: Implementar a funcionalidade de listagem e reutilização de documentos do assistido no sistema Maria.
  - \[Talita Ribeiro\] Atualizar backlog: Incluir na lista de tarefas a deleção de documentos em cancelamentos e o reapontamento em reagendamentos.
  - \[Talita Ribeiro\] Confirmar casos: Verificar a disponibilidade da lista de todos os casos no sistema.
  - \[CAMILA MAURA MOREIRA DA SILVA\] Ajustar regra: Conversar com Felipe sobre a regra de 30 dias de antecedência para sincronização.
  - \[Talita Ribeiro\] Compartilhar materiais: Enviar o documento de trabalho e a lista de documentos da Dra. Suian no grupo de gestão.
  - \[Gustavo Pinto\] Resolver IDs: Auxiliar Filipe na obtenção dos IDs dos documentos necessários para a integração.
  - \[CAMILA MAURA MOREIRA DA SILVA\] Enviar texto de declaração: Enviar o texto utilizado pelo Nad para a declaração de residência para que Filipe possa atualizar o modelo no sistema.
  - \[Filipe Braida do Carmo\] Adicionar motivo de encerramento: Adicionar a opção falta de resposta do assistido na lista de motivos de encerramento de atendimentos.
  - \[Filipe Braida do Carmo\] Verificar matrícula de defensores: Verificar com Gustavo a possibilidade de buscar os dados de matrícula dos defensores diretamente do Verde.
  - \[Filipe Braida do Carmo\] Implementar calculadora: Implementar a calculadora de despesas para recalcular o total automaticamente no sumário.
  - \[Filipe Braida do Carmo\] Subir para homologação: Subir as novas alterações para o ambiente de homologação na segunda-feira para testes.
  - \[CAMILA MAURA MOREIRA DA SILVA\] Reunião de resultados: Agendar uma reunião para apresentar os resultados da ação na Campo para o Filipe.
  - \[Filipe Braida do Carmo\] Consultar Luna: Discutir com a Luna os problemas relacionados aos identificadores do pomar no Tike para resolver inconsistências de monitoramento.
  - \[Filipe Braida do Carmo\] Atualizar monitoramento: Realizar a verificação pendente sobre a origem das mensagens e atualizar o sistema para garantir o monitoramento de todos os chats via Maria.
  - \[Filipe Braida do Carmo\] Ajustar lista: Fazer uma revisão detalhada na lista da Bahia que foi encaminhada ao Gustavo.
  - \[Filipe Braida do Carmo\] Solicitar número: Solicitar à Luna a liberação do número para testes de funcionamento do motor de conversa.

## Relacionado
- [[Maria - atendimento automatizado]]
