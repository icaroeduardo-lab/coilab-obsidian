---
tipo: reuniao
data: 2026-11-17
hora: "14:29"
convidados:
  - Felipe Martins Costa Brito
  - Rodrigo Stwart Da Silva Marcal
  - CAMILA MAURA MOREIRA DA SILVA
  - Diogo Leite Mesquita
  - Bianca Tavares Soares Silva
  - Yann Naylor Francisco
  - JHONY DE PAULA BOTELHO
  - ANDERSON MARINOVIC
  - Guilherme De Araujo Silva
  - ICARO LUIZ ALBAR EDUARDO
  - Gustavo Pinto
  - MAURO LUIZ DE OLIVEIRA JUNIOR
falaram:
  - Emerson Yamamoto
  - Yann Naylor Francisco
  - Bianca Tavares Soares Silva
  - Leonardo de Melo
  - Felipe Martins Costa Brito
  - Gabriel Távora
  - Lucas de Oliveira Mol Silva
  - Thaiana Lima
  - ICARO LUIZ ALBAR EDUARDO
  - Alexandre Donnelly Vaz
  - Lucas Farias
projeto: "[[Maria - atendimento automatizado]]"
fonte: Google Meet, anotações do Gemini (revisar)
gravacao: 
tags:
  - reuniao
  - sprint
  - apis
---

# Sprint - App (APIs) (17/11)

> Anotações geradas pelo Gemini no Google Meet; podem conter erros (nomes de sistemas e de pessoas saem trocados em alguns pontos). Duração: 2h18. Transcrição: [[2026-11-17 - Sprint - App (APIs) (transcrição)]].

## Resumo

Reunião de alinhamento cobriu validação de sprints, com ajustes de fluxo e definição de prioridades.

**Validação e Planejamento Inicial**
O sistema atingiu a marca de 1567 pessoas validadas com GOV, reduzindo a demanda da CRC. A sprint atual priorizou funcionalidades voltadas para o aplicativo antes das integrações.

**Ajustes no Fluxo e API**
Equipe discutiu melhorias no fluxo de réu liberto, padronizando o salvamento do RG. Lucas Farias apresentou atualizações na Integra API para verificação de tipos de partes.

**Definição de Novas Tarefas**
Thaiana Lima detalhou as tarefas priorizadas para a próxima sprint, totalizando entre 30 e 40 pontos. Ficou acordado remarcar a próxima reunião para o dia 9 de dezembro.

## Decisões

**Precisa de mais conversa:**

- **Verificação da regra para plantão e recesso** A necessidade de verificação e adaptação da regra de preferência de atendimento para os casos de plantão e recesso ficou pendente de análise e confirmação posterior.

**Alinhadas:**

- **Reordenação do fluxo de preferência de atendimento** O grupo alinhou a alteração para mover a seleção de preferência de atendimento para após a escolha do órgão, assumindo a perda de compatibilidade com versões antigas do aplicativo.
- **Padronização do salvamento de RG** O sistema deve sempre salvar o RG do réu liberto no campo novo e na observação, independentemente de o usuário ser representante ou não.
- **Remoção de andamento de criação automática** Ficou decidido remover a criação do andamento que indica que o caso foi gerado automaticamente pelo aplicativo.
- **Tratamento para assistido fora do processo** O sistema deve prosseguir com o encaminhamento sem exibir mensagem de erro ou criar o caso quando o assistido não for parte do processo.
- **Ajuste no mapeamento de órgãos** O mapeamento de órgãos de execuções penais deve ser alterado para remover o final 6 da quinta DP.
- **Definição do escopo de issues priorizadas** O grupo alinhou a seleção de issues apresentada por Thaiana, totalizando entre 35 e 40 pontos, para atender às demandas priorizadas e liberar o sistema Verde.

## Próximas etapas
As tarefas desta reunião ficam em `11 Tarefas`; a lista abaixo vem das anotações do Gemini, ainda sem nota de tarefa. A tabela mostra as que já existirem.

- [Emerson Yamamoto] Investigar a falha de exibição de endereço: no fluxo de primeiro atendimento para o órgão da DPU para identificar o motivo de o campo ter ficado em branco.
- [Emerson Yamamoto] Incluir apenas o RG do réu na observação: para os casos de representante no fluxo do encaminhamento.
- [Emerson Yamamoto] Remover a criação do andamento: de caso criado automaticamente pelo aplicativo para evitar registros desnecessários.
- [Emerson Yamamoto] Remover o dígito 6: da regra de mapeamento da quinta DP para corrigir o direcionamento de atendimento dos assistidos.
- [Emerson Yamamoto] Encaminhar a lista de alterações: da Integra para o pessoal da Defensoria e para Felipe a fim de revisar os impactos e modificações necessárias no fluxo da TI.
- [Emerson Yamamoto] Enviar a seleção de issues da Integra API: para Yann Naylor Francisco e Felipe Martins Costa Brito contendo a organização dos impactos identificados.
- [Gabriel Távora] Ajustar o fluxo de preferência de atendimento: para os fluxos de violência doméstica, atendimento prisional e ré liberto, movendo a seleção de atendimento remoto ou presencial para após a escolha do órgão conforme alinhado.
- [Leonardo de Melo] Investigar a falha de recuperação de partes: no processo para resolver o problema de carregamento inconsistente relatado durante a demonstração.
- [Leonardo de Melo] Salvar o RG e o registro de Real Liberto: no campo específico, independentemente de a pessoa ser representante ou não, mantendo também o registro na observação.
- [Unassigned] Verificar o fluxo de primeiro atendimento: em períodos de plantão e recesso para validar as decisões e alterações na API.
- [Thaiana Lima] Incluir a questão na lista da CRC: para a sprint futura referente à remoção da seção de pessoa presa em casos de réu em liberdade.
- [Thaiana Lima] Disponibilizar o refinamento para teste: referente à verificação e ao reaproveitamento de casos processuais.

```base
filters:
  and:
    - 'tipo == "tarefa"'
    - file.hasLink(this.file)
formulas:
  situacao: 'if(status == "feita", "feita", if(prazo < today(), "atrasada", status))'
views:
  - type: table
    name: Tarefas desta reunião
    order:
      - file.name
      - responsavel
      - prazo
      - formula.situacao
    sort:
      - property: note.prazo
        direction: ASC
```

## Detalhes

**Atualização dos números de validação e diretrizes iniciais**: Emerson Yamamoto informou que o sistema atingiu a marca de 1567 pessoas validadas com GOV, registrando um acréscimo de 500 validações em relação ao meio-dia do dia anterior. Yann Naylor Francisco destacou que esse volume representa menos 1500 pessoas para validação por parte da CRC (00:04:49). Adicionalmente, Yann Naylor Francisco repassou a orientação de Camila para que o foco na abertura seja direcionado ao pré-atendimento para varas (00:00:22).

**Visão geral da sprint e planejamento de itens**: Emerson Yamamoto apresentou a distribuição da sprint atual, composta por nove eixos, priorizando inicialmente as funcionalidades voltadas para o app antes de prosseguir para as integrações de API. Entre as tarefas descritas estão a alteração de encaminhamentos, a permissão de caracteres especiais em cadastros e a melhoria em consultas de órgãos para réus libertos (00:07:48) (00:10:30). Também foram detalhadas tarefas de API voltadas para rotinas automatizadas de envio de e-mails de notificação por falta de resposta (00:15:14).

**Ajustes no fluxo de preferência de atendimento do aplicativo**: Gabriel Távora demonstrou a tarefa de alterar o encaminhamento para solicitar preferência de atendimento apenas quando houver pauta remota ou contato publicável do órgão (00:16:20). Após demonstrações nos fluxos de primeiro atendimento, violência doméstica, atendimento prisional e réu liberto, Felipe Martins Costa Brito avaliou que a pergunta de preferência deve ser movida para um momento posterior à seleção do órgão (00:17:42) (00:20:51). Emerson Yamamoto apontou que essa alteração impactará a compatibilidade com versões antigas do app e exigirá validações adicionais para os casos de plantão e recesso (00:24:01) (00:30:23).

**Ocultação de andamentos de agendamento de pauta interna**: Lucas de Oliveira Mol Silva apresentou a tarefa de alterar a visualização do caso para ocultar andamentos de agendamentos de pauta interna configurados como não visíveis no app (00:32:32). Através de um exemplo prático com dois agendamentos com datas distintas, Lucas de Oliveira Mol Silva demonstrou que o sistema exibe corretamente apenas o agendamento marcado como visível, mantendo o outro oculto na consulta ao caso (00:35:08). Felipe Martins Costa Brito acompanhou a demonstração, confirmando o funcionamento esperado da regra (00:36:32).

**Inclusão de suporte a hífen no cadastro de usuários**: Lucas de Oliveira Mol Silva exibiu a implementação da melhoria que permite o uso de hífen e apóstrofo em nomes e sobrenomes durante o cadastro no app (00:36:32). Durante os testes realizados por Lucas de Oliveira Mol Silva, o sistema aceitou nomes contendo hífen, mas continuou bloqueando o uso de acentos agudos e crases conforme as restrições vigentes (00:39:11). Emerson Yamamoto recordou que a restrição a acentos foi mantida para evitar problemas em outras partes do sistema (00:38:03).

**Validação do fluxo de réu liberto e tratamento de registros gerais**: Leonardo de Melo apresentou a tarefa de alterar o fluxo de réu liberto verificando se o assistido é o próprio réu ou um representante (00:41:52). Durante a simulação, identificou-se um problema crítico apontado por Emerson Yamamoto e Icaro Luiz Albar Eduardo onde a seleção incorreta do RG de uma pessoa presa pode gerar divergências graves entre o nome do assistido e os dados exibidos nos detalhes do encaminhamento (00:49:39) (00:57:35). Thaiana Lima esclareceu que o campo de RG avulso deve ser preenchido especificamente quando houver um representante, enquanto Emerson Yamamoto pontuou que o fluxo precisa de refinamentos para evitar inconsistências nos dados salvos (00:48:35) (00:50:33).

**Fluxo de Representante e Tratamento de RG**: Leonardo de Melo apresentou o fluxo para representantes e réus em liberdade, gerando dúvidas com Emerson Yamamoto, Thaiana Lima, Yann Naylor Francisco e Felipe Martins Costa Brito sobre a exibição de campos de pessoa presa (00:59:21). Yann Naylor Francisco apontou comportamentos de agendamento em ISOs anteriores, enquanto Emerson Yamamoto esclareceu que pessoas presas seguem para o fluxo do Nospen, diferenciando-se de pessoas em liberdade (01:00:13). Leonardo de Melo demonstrou a exibição de órgãos com base no penúltimo dígito do RG, conforme validado na quinta DP e terceira DP (01:02:46). Thaiana Lima explicou que a mudança no fluxo para réus libertos exige capturar o RG para mapeamento, levando Emerson Yamamoto a sugerir a remoção da seção de pessoa presa em casos de réus libertos para reduzir complexidade (01:04:01). Felipe Martins Costa Brito questionou a exibição de dados de pessoas presas para assistidos em liberdade, e Leonardo de Melo constatou que o sistema utiliza o assistido logado sem validação adequada, exigindo revisão do fluxo (01:04:57).

**Ajustes no Fluxo de Perguntas e Observações**: Leonardo de Melo e Thaiana Lima discutiram a ordem das perguntas sobre o réu estar preso ou em liberdade antes de solicitar o número do RG (01:07:44). Emerson Yamamoto confirmou que o campo do RG do réu liberto deve ser salvo nas situações corretas, mantendo o registro na observação apenas com o RG do réu quando houver atuação de representante (01:09:12). Leonardo de Melo confirmou que, nos casos sem representante, o novo campo de RG não era preenchido anteriormente, gerando discussões sobre padronização (01:10:16) (01:12:27). Felipe Martins Costa Brito e Emerson Yamamoto concordaram em padronizar o salvamento do RG no novo campo em todas as situações de réu liberto, além de manter a exibição na observação para visualização dos órgãos na pauta do dia (01:13:23).

**Reaproveitamento de Casos Processuais**: Leonardo de Melo demonstrou o funcionamento da busca de processos e o reaproveitamento de casos existentes com base no número do processo e na origem MNI (01:15:11) (01:17:51). Thaiana Lima apontou que a ISO da CRC exige verificar a possibilidade de reaproveitamento após finalizar o encaminhamento, regra que Leonardo de Melo detalhou em fluxos de atendimento remoto e presencial (01:16:25) (01:19:16). Emerson Yamamoto questionou o redirecionamento automático para a tela do caso após a conclusão, e Leonardo de Melo esclareceu que o comportamento atual direciona diretamente para a mensagem devido ao formato de atendimento (01:23:01). Após demonstrar o encerramento de um caso para testar a criação de um novo processo, Leonardo de Melo apresentou o andamento gerado automaticamente (01:24:20).

**Remoção de Andamentos de Criação Automática**: Felipe Martins Costa Brito questionou a relevância do título gerado automaticamente com a descrição de caso criado pelo aplicativo, argumentando que a informação gera títulos inadequados e desnecessários. Emerson Yamamoto ponderou que a intenção era indicar a origem automatizada, mas concordou com Felipe Martins Costa Brito sobre a remoção do andamento (01:26:13). Emerson Yamamoto anotou a diretriz de não criar o andamento de criação automática de caso, visto que a origem pelo app já fica registrada (01:27:39).

**Cadastro de Personagens e Tratamento de Polos do TJ**: Leonardo de Melo explicou a regra de cadastrar todas as pessoas do processo judicial como personagens utilizando uma flag de cadastro de pessoa na consulta ao processo (01:29:06) (01:32:37). Emerson Yamamoto expressou preocupação quanto à duplicação de cadastros e poluição do sistema com nomes de empresas ou dados incompletos, mas Thaiana Lima confirmou que o verde já realiza esse procedimento automaticamente durante a consulta de processos (01:30:31). Leonardo de Melo destacou que apenas registros com dados de pessoa física válidos são cadastrados, e tipos de polo do TJ sem correspondência no verde são tratados como terceiros (01:29:06) (01:33:26).

**Validação de Processos e Intimações no Fluxo de Recepção**: Leonardo de Melo apresentou o fluxo de recebimento de intimação, demonstrando o reaproveitamento de casos e a criação automática quando o caso anterior é encerrado (01:35:32). Emerson Yamamoto sugeriu testar cenários ambíguos, como processos com a mesma pessoa em polos invertidos (autor versus réu), para garantir que o sistema não reaproveite incorretamente, o que Leonardo de Melo validou com sucesso em teste prático (01:38:21). Leonardo de Melo apresentou um modal implementado para casos em que o assistido não faz parte do processo, exibindo mensagem de erro orientando contato pelo 129 (01:39:27). Após ponderação de Thaiana Lima e Felipe Martins Costa Brito de que o encaminhamento possui as informações corretas e deve prosseguir, ficou decidido remover a mensagem de erro restritiva e apenas suprimir a criação do caso (01:41:34).

**Consulta de Órgão com Parâmetro de RG**: Alexandre Donnelly Vaz apresentou a alteração na consulta de órgãos para réus libertos, incorporando o parâmetro direto de RG em substituição ao identificador IDCAP (01:43:45). Alexandre Donnelly Vaz demonstrou o mapeamento baseado no penúltimo dígito do RG para direcionamento à terceira DP de execuções penais ou primeira DP de execuções penais (01:45:21) (01:49:43). Emerson Yamamoto apontou uma inconsistência no dígito 6 que gerava empate e ausência de retorno de órgãos, levando Felipe Martins Costa Brito e Thaiana Lima a confirmarem a atualização recente no mapeamento da execução penal que excluiu o dígito 6 da quinta DP, mantendo o dígito apenas na terceira DP (01:46:51) (01:51:00).

**Armazenamento de RG no Fluxo Prisional e Alinhamentos de Integração**: Alexandre Donnelly Vaz demonstrou o parâmetro opcional de RG no fluxo de encaminhamento prisional, registrando a informação diretamente no encaminhamento e na observação (01:49:43) (01:52:41). Emerson Yamamoto e Alexandre Donnelly Vaz alinharam que o salvamento do RG no campo novo deve ser padronizado para todas as situações de réu liberto, independentemente de haver representação (01:54:30). Thaiana Lima e Emerson Yamamoto debateram os impactos da atualização na API e nos fluxos do chatbot, combinando alinhamentos futuros com a equipe de tecnologia para garantir que as alterações sejam comunicadas e implementadas antes da subida da nova versão da Integra (01:56:37).

**Atualização na Consulta de Processos da Integra API**: Lucas Farias apresentou a alteração implementada no end point de processo da Integra API para verificar o tipo da parte com base em um novo campo de ID de pessoa. Quando o ID não é informado, o tipo da parte não é retornado (01:58:27) (02:02:48). Caso o ID fornecido não pertença a uma parte do processo, o sistema retorna o valor não encontrado, ou utiliza a designação outros quando se trata de uma parte com tipo diferente de autor ou réu, a exemplo de testemunhas e vítimas (01:59:58) (02:02:48). Em cenários em que o processo não é consultado com sucesso, optou-se por retornar um erro de consulta em vez de não encontrado para evitar ambiguidades, preservando as informações já existentes no banco de dados (02:01:27).

**Modificações nos E-mails da Cidadão API**: Lucas Farias demonstrou as alterações realizadas nos e-mails gerados pela Cidadão API, o que incluiu a remoção do modelo anterior e a criação de um novo texto padrão. O sistema passou a contemplar regras de horário de atendimento, exibindo o horário comum do órgão quando disponível, ou recorrendo aos horários de urgência na ausência do primeiro. Quando o órgão não possui endereço cadastrado, o texto é modificado para instruir o contato com a CRC por meio do número 129 (02:04:02) (02:06:18). Adicionalmente, verificou-se que os encaminhamentos já são criados nativamente com o tipo de atendimento presencial (02:07:45).

**Seleção e Priorização de Tarefas para a Próxima Sprint**: Thaiana Lima detalhou a seleção de tarefas priorizadas para a sprint, totalizando entre 30 e 40 pontos, com foco em pré-atendimento para atender às demandas de Braida. Foram destacadas três notificações críticas (e-mail, aplicativo e WhatsApp) e a exibição do link do Google Meet no agendamento interno, itens que bloqueiam alterações no Verde API devido aos riscos de notificação sem aviso prévio (02:11:30). Como itens adicionais, incluiu-se a correção de encaminhamento para a Corregedoria na Integra API e Cidadão API como bônus, enquanto a demanda de envio de aplicativo para o WhatsApp da CRC foi mantida para atendimento posterior (02:12:47). Yann Naylor Francisco e os demais participantes confirmaram o alinhamento com base na planilha compartilhada no chat (02:14:00).

**Definição da Data e Alinhamentos Finais da Próxima Reunião**: A data inicial para a próxima apresentação, prevista para 8 de dezembro, foi questionada por Felipe Martins Costa Brito devido à possibilidade de não haver expediente oficial em decorrência do dia da justiça (02:14:40). Após a ponderação, ficou acordado remarcar o encontro para o dia 9 de dezembro, no período da tarde. Lucas de Oliveira Mol Silva pontuou que estará de férias no período, mas a equipe estruturou o suporte com Leobardo e a colaboração de Gabriel e Marcos para a apresentação das respectivas demandas (02:15:40). Por fim, Emerson Yamamoto encerrou a reunião indicando que organizará e enviará aos colegas a seleção de issues da Integra API afetadas (02:16:24).

## Relacionado
- [[2026-11-17 - Sprint - App (APIs) (transcrição)]]
- [[2026-10-22 - Sprint - App (APIs)]]
- [[Maria - atendimento automatizado]]
- [[Tykhe]]
