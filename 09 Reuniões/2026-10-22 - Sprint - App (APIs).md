---
tipo: reuniao
data: 2026-10-22
hora: "14:25"
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
  - Felipe Martins Costa Brito
  - Gustavo Pinto
  - Diogo Leite Mesquita
  - Thaiana Lima
  - Talita Ribeiro
  - Yann Naylor Francisco
  - Lucas Farias
  - Alexandre Donnelly Vaz
  - Leonardo de Melo
  - Marcos Benigno
  - ICARO LUIZ ALBAR EDUARDO
  - Bianca Tavares Soares Silva
  - Lucas de Oliveira Mol Silva
projeto: "[[Maria - atendimento automatizado]]"
fonte: Google Meet, anotações do Gemini (revisar)
gravacao: 
tags:
  - reuniao
  - sprint
  - apis
---

# Sprint - App (APIs) (22/10)

> Anotações geradas pelo Gemini no Google Meet; podem conter erros (nomes de sistemas e de pessoas saem trocados em alguns pontos). Duração: 1h56. Transcrição: [[2026-10-22 - Sprint - App (APIs) (transcrição)]].

## Resumo

Reunião de alinhamento com foco na liberação do Gov.BR para homologação e novos fluxos de atendimento.

**Integração e Versões do Aplicativo**
Versão com Gov.BR será liberada para homologação. Correções em verificações de identidade foram implementadas com sucesso.

**Fluxos de Atendimento e APIs**
Novos fluxos de agendamento e status de pré-atendimento foram apresentados. Ajustes estruturais em filtros de assunto foram definidos.

**Planejamento de Sprint e Prazos**
Data de entrega da sprint foi prorrogada para 17 de novembro devido a feriados. Cronograma de implantação de APIs foi alinhado.

## Decisões

**Alinhadas:**

- **Critério de exibição para preferência de WhatsApp** O sistema deve exibir a opção de recebimento de notificações por WhatsApp apenas para usuários que possuem telefone cadastrado.
- **Alteração da data de planejamento** Ficou definido que a próxima reunião de planejamento da sprint será alterada do dia 12 para o dia 17 de novembro.
- **Criação de aba para proposta de deploy** Foi acordado a criação de uma nova aba na planilha de deploy para registrar a proposta de liberação e versionamento.

## Próximas etapas
As tarefas desta reunião ficam em `11 Tarefas`; a lista abaixo vem das anotações do Gemini, ainda sem nota de tarefa. A tabela mostra as que já existirem.

- **Emerson Yamamoto:** Liberar versão GOVBR: Disponibilizar a nova versão do aplicativo com GOVBR no ambiente de testes temporário.
  - [Emerson Yamamoto] Limpar verificações: Realizar uma limpeza geral nos registros antigos de verificação de identidade pendentes.
  - [Gustavo Pinto, Diogo Leite Mesquita] Planejar deploy API: Definir o cronograma e o escopo das próximas subidas de interface de programação de aplicações.
  - [Emerson Yamamoto] Ajustar planilha: Adicionar uma coluna na planilha de controle identificando dependências com outros sistemas.
  - [Thaiana Lima] Consultar requisitos WhatsApp: Entrar em contato com Talita para esclarecer os detalhes e requisitos da funcionalidade de notificações via WhatsApp.
  - [O grupo] Criar tarefas WhatsApp: Elaborar as tarefas para implementar o envio de confirmação de agendamento e notificações gerais via WhatsApp.
  - [Leonardo de Melo] Incluir Observação Órgão: Incluir campo de observação do órgão na integração de dados e realizar o ajuste do texto fixo para órgãos de justiça itinerante.
  - [Felipe Martins Costa Brito, Talita Ribeiro] Desenvolver Fluxo WhatsApp: Desenvolver um fluxo para notificações por WhatsApp de informações de agendamentos.
  - [Lucas Farias, Emerson Yamamoto] Validar Agendamento: Verificar se o tipo de agendamento via atendimento precisa de integração com pré-atendimento.
  - [Talita] Alterar encaminhamento: Alterar o encaminhamento processual para reaproveitar ou criar o caso, solicitando preferência de atendimento apenas se o órgão possuir pauta remota ou contato publicável.
  - [O grupo] Ajustar visualização: Remover do andamento do caso no aplicativo os andamentos de agendamentos que foram marcados como não visíveis por pauta interna.
  - [O grupo] Permitir hífen: Atualizar o cadastro de pessoas para permitir o uso de hífens nos nomes.
  - [O grupo] Validar representante: Alterar o fluxo de atendimento para verificar se o usuário é o próprio réu ou um representante, solicitando o RG do réu caso seja representante.
  - [O grupo] Ajustar consulta: Alterar a consultora de processo para retornar se a pessoa é ré no processo, permitindo que a Tike saiba se deve realizar a pergunta sobre representação.
  - [O grupo] Armazenar RG: Armazenar o RG do réu manualmente informado pelo representante no encaminhamento do processo.
  - [O grupo] Substituir e-mail: Criar um novo modelo de e-mail para casos não respondidos em 30 dias, substituindo o modelo atual que mistura fluxos remotos e presenciais.
  - [Felipe Martins Costa Brito] Validar recesso: Validar o funcionamento do recesso na plataforma Tike durante o próximo feriado.
  - [O grupo] Liberar GOV BR: Liberar uma versão de ambiente de teste do GOV BR no aplicativo e no verde com correções de identidade e outras melhorias.
  - [Emerson Yamamoto] Avaliar deploy: Avaliar as pendências e dependências técnicas das funcionalidades marcadas na planilha de deploy para viabilizar as próximas liberações.

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

**Liberação de Versão com GOVBR no Ambiente Temporário**: Emerson Yamamoto informou que a equipe montará uma versão com integração ao GOVBR para ser disponibilizada no ambiente temp até o dia seguinte ou na segunda-feira, permitindo que as equipes realizem homologação e testes antes da subida para produção, etapa na qual a configuração do broker precisará ser ajustada (00:03:36).


**Correção de Duplicação de Verificações de Identidade no Aplicativo**: Emerson Yamamoto apresentou uma verificação mais rígida para impedir que pessoas usuárias enviem duas ou três verificações de identidade no mesmo segundo, resolvendo uma issue antiga repassada por Bianca (00:05:01). Emerson Yamamoto também mencionou a possibilidade de realizar uma limpeza geral nos registros anteriores a 2026, além das limpezas pontuais já executadas (00:06:08).


**Correção do Bloqueio de Versões Antigas**: Emerson Yamamoto relatou que um problema anterior no bloqueio de versões antigas do aplicativo (relacionado ao push token, que deixava uma tela permanentemente travada e exigia fechar o aplicativo) foi corrigido, permitindo que futuros bloqueios ocorram sem gerar reclamações (00:06:08).


**Planejamento de Onda de Deploy para APIs e Chatbot**: Diogo Leite Mesquita levantou o tema sobre o plano de subida de próximas APIs, apontando mais de 20 issues acumuladas para chatbot e WhatsApp. Emerson Yamamoto solicitou a ajuda de Felipe Martins Costa Brito para analisar uma tabela com issues homologadas (sendo oito issues separadas por Felipe Martins Costa Brito) e verificar dependências com o sistema da Tik, com Gustavo Pinto solicitando o envio da lista escolhida via WhatsApp para avaliação conjunta (00:07:06).


**Abertura da Apresentação e Ausência de Farias**: Emerson Yamamoto iniciou a apresentação da pauta estruturada em issues de aplicativo e de Integra API, comunicando a ausência de Farias devido a instabilidades na conexão de internet (00:11:52).


**Alteração no Fluxo de Primeiro Atendimento com Mapeamento de Assuntos Verde e CNJ**: Marcos Benigno apresentou a issue 10468, que verifica se há um caso processual em andamento associado ao assunto verde e CNJ selecionado, exibindo uma mensagem para direcionar o público para o atendimento processual (00:13:13) (00:20:14). Emerson Yamamoto e Felipe Martins Costa Brito discutiram a checagem de urgência, concordando que a verificação pode ocorrer antes do complemento do assunto (00:21:33).


**Solicitação de Preferência de Recebimento de Agendamento por WhatsApp**: Marcos Benigno apresentou a issue 1493, onde ao finalizar um agendamento é exibido um card e um modal posterior perguntando se a pessoa deseja receber informações pelo WhatsApp (00:23:41). Emerson Yamamoto, Felipe Martins Costa Brito, Thaiana Lima e Gustavo Pinto debateram se o aviso deve ser condicional à existência de telefone cadastrado, decidindo ajustar para exibir a opção apenas para quem possui telefone cadastrado com início nove .


**Destaque em Observações de Endereço e Justiça Itinerante**: Marcos Benigno e Leonardo de Melo apresentaram a issue 10488, que destaca em negrito as observações de endereço e adiciona um texto fixo para órgãos de justiça itinerante (00:39:37) (00:43:44). Felipe Martins Costa Brito e Thaiana Lima esclareceram que o campo de observação pertence ao órgão e não ao imóvel, e alinharam ajustes futuros no texto fixo para evitar redundâncias com as datas (00:43:09) (00:47:24).


**Uso de Órgão Colegiado no Mapeamento EPROC 2G**: Leonardo de Melo apresentou a issue 10513 (e equivalente 10517 na Integra), demonstrando que a consulta de processos de origem EPROC de segunda instância passa a armazenar e utilizar o órgão colegiado em vez do órgão julgador/TJ para o mapeamento correto com os órgãos da Defensoria Pública (DPGE), o que foi confirmado por Felipe Martins Costa Brito (00:49:27).


**Atualização de Status de Pré-Atendimento Vinculado a Agendamento**: Emerson Yamamoto introduziu as issues 10627 e 10628 voltadas para o Farias atendimento, permitindo que profissionais do sistema verde visualizem o status do pré-atendimento (como número de documentos enviados e conclusão), inicializando o status como pendente assim que o link for gerado (00:17:23).


**Alinhamento Adicional sobre Notificações de WhatsApp com Talita Ribeiro**: Talita Ribeiro entrou na reunião para alinhar com Felipe Martins Costa Brito, Thaiana Lima e Emerson Yamamoto sobre o escopo de envio de dados de agendamento e lista de documentos via WhatsApp, decidindo agendar uma reunião específica com a equipe da DGD para desenhar o fluxo definitivo .


**Discussão sobre Fluxo de WhatsApp e Refinamento**: Talita Ribeiro questionou Emerson Yamamoto se um ajuste discutido com Felipe Martins Costa Brito tratava-se de um refinamento ou de um novo fluxo, tendo Emerson Yamamoto esclarecido que não poderia ser considerado refinamento por se tratar de um envio para o WhatsApp, que constitui um fluxo operacional distinto (01:02:25). Talita Ribeiro pontuou que a instrução de serviço original era específica para solicitar a confirmação de agendamento via WhatsApp, enquanto Emerson Yamamoto recordou ter sugerido uma ideia mais genérica sobre informações gerais do agendamento, que acabou sendo bem acolhida (01:03:06).


**Consulta de Casos por Assunto Verde e Assunto CNJ**: Alexandre Donnelly Vaz apresentou a instrução de serviço para alterar a consulta de casos de uma pessoa, permitindo verificar o mapeamento entre o assunto verde e o assunto unificado do Conselho Nacional de Justiça (01:03:06). Alexandre Donnelly Vaz demonstrou a filtragem por um assunto verde associado a assuntos judiciais do Conselho Nacional de Justiça, como abandono de função, confirmando que o sistema retorna apenas os casos correspondentes sem quebrar os filtros de busca direta por assunto verde (01:04:12). Emerson Yamamoto e Alexandre Donnelly Vaz debateram sobre os parâmetros de busca e o comportamento esperado dos filtros para casos associados (01:06:17).


**Reestruturação de Filtros de Assunto por Identificador de Processo**: Emerson Yamamoto explicou que, anteriormente, o tipo de caso definia o valor no identificador de assunto, gerando um campo multivalorado confuso entre o identificador verde e o identificador do Conselho Nacional de Justiça. Para solucionar esse problema, a equipe criou um novo campo dedicado denominado identificador de assunto de processo, garantindo campos definitivos para cada tipo de assunto, enquanto o tipo de caso passa a atuar estritamente como filtro (01:07:22). Emerson Yamamoto observou que a interface de programação de aplicativo pode exigir pequenos ajustes para se adaptar a essa alteração estrutural mais organizada (01:08:23).


**Fluxo de Atendimento Processual e Observações de Órgãos**: Alexandre Donnelly Vaz apresentou a instrução de serviço unificando o fluxo de atendimento processual na busca de órgãos, retornando observações para endereços do tipo justiça itinerante (01:08:23). Emerson Yamamoto apontou que a observação é uma propriedade intrínseca do órgão e não do endereço específico, sugerindo alinhar a estrutura para extraí-la diretamente do órgão, conforme discutido previamente com Felipe Martins Costa Brito. Alexandre Donnelly Vaz ponderou sobre órgãos com múltiplos endereços, e Emerson Yamamoto concordou em mover o campo para fora para manter a consistência textual (01:09:44).


**Visualização de Órgão Colegiado no Atendimento Processual**: Alexandre Donnelly Vaz apresentou a funcionalidade equivalente para aplicativo referente ao órgão colegiado, demonstrando uma consulta que recupera o nome do órgão da Defensoria Pública do Estado a partir do órgão colegiado de um processo (01:10:37). Alexandre Donnelly Vaz evidenciou que a remoção do órgão colegiado do processo resulta em um erro informando que não foi encontrada vara associada devido à validação do mapeamento (01:11:55).


**Novo Ponto de Extremidade para Status de Pré-Atendimento**: Lucas Farias apresentou a instrução de serviço 10627, criando um novo ponto de extremidade para receber status vinculados a um pré-atendimento de agendamento, contemplando o recebimento do identificador de agendamento, identificador de pré-atendimento e quantidade de documentos enviados. Lucas Farias demonstrou as regras de validação implementadas, incluindo a verificação se o agendamento está ativo (pendente ou validado), validação de tipo de evento restrita ao Centro de Relacionamento com o Cidadão para excluir audiências ou bloqueios, e validação de formato de status (01:13:32). Lucas Farias detalhou que a quantidade de documentos enviados é armazenada em um novo log criado especificamente para registrar as alterações de status, e que novos envios atualizam o status anterior (01:16:55). Thaiana Lima questionou sobre a abrangência do tipo Centro de Relacionamento com o Cidadão, e Emerson Yamamoto esclareceu que o tipo engloba todas as origens, como o aplicativo Maria e o site, embora tenham levantado a necessidade de confirmar o tratamento aplicável ao atendimento do núcleo digital (01:19:06).


**Geração de Link e Gestão de Status de Pré-Atendimento**: Lucas Farias apresentou a alteração no ponto de extremidade de geração de link de pré-atendimento, que agora centraliza as sessões e cria o pré-atendimento com status pendente automaticamente ao gerar o link para um agendamento novo (01:22:25). Lucas Farias detalhou que solicitações repetidas para o mesmo link e identificador de pré-atendimento não alteram nem sobrescrevem o status atual caso este seja diferente de pendente, prevenindo perdas de informativos de andamento em produção (01:24:46). Emerson Yamamoto reforçou que essa medida protege contra a sobrescrita indevida de status em passivos existentes, mantendo a integridade até que o ponto de extremidade de atualização seja acionado (01:26:37).


**Planejamento de Requisitos e Escopo da Sprint**: Thaiana Lima apresentou os candidatos do backlog da sprint, totalizando trinta pontos de interface de programação de aplicativo e onze pontos de interface de usuário, priorizando notificações de inativação de endereços de órgãos com agendamento presencial (01:29:07). Thaiana Lima destacou alterações no encaminhamento processual, remoção de andamentos não visíveis no aplicativo por pauta interna, permissão de hífen no cadastro de nomes de pessoas, e o pedido de Felipe Martins Costa Brito para permitir que réus libertos sejam agendados por representantes ou familiares (01:30:51). Thaiana Lima explicou que a consulta de processos será modificada para retornar se a pessoa consultada é ré, permitindo que a tecnologia da informação ajuste o fluxo de perguntas, além da atualização do modelo de e-mail automatizado de trinta dias para encaminhamento presencial (01:32:00).


**Alocação de Equipe e Capacidade para o Aplicativo**: Leonardo de Melo questionou o desequilíbrio na pontuação de interface de programação de aplicativo voltada para o aplicativo, visto que há apenas uma pessoa na equipe correspondente (01:34:13). Emerson Yamamoto pontuou que Lucas de Oliveira Mol Silva está chegando para reforçar a equipe do cidadão, embora precise de adaptação devido à complexidade do sistema, enquanto Leonardo de Melo e Emerson Yamamoto debateram formas de mitigar a entrega e solicitar auxílio de Lucas Farias e Alexandre Donnelly Vaz se necessário (01:35:25).


**Ajuste de Data de Entrega da Sprint por Feriados**: Gustavo Pinto e Emerson Yamamoto analisaram o calendário de feriados de novembro, destacando o feriado de Finados em dois de novembro e a possibilidade de ponto facultativo ou feriadão prolongado no dia trinta (01:37:56). Emerson Yamamoto sugeriu prorrogar a data de entrega da sprint de doze de novembro para dezessete de novembro (terça-feira) para acomodar os feriados e garantir a entrega completa, contando com a concordância de Diogo Leite Mesquita e Yann Naylor Francisco (01:38:45).


**Validação de Recesso e Integrações de Atendimento Telefônico**: Diogo Leite Mesquita alertou sobre a necessidade de verificar o impacto do recesso nas entregas de interface de programação de aplicativo e mensagens, com Gustavo Pinto questionando se a tecnologia da informação testou o esquema de atendimento durante o recesso (01:40:29). Felipe Martins Costa Brito confirmou que realizou testes em feriados anteriores com êxito e planejou novos testes para o feriado de novembro. Felipe Martins Costa Brito, Gustavo Pinto e Emerson Yamamoto discutiram o status da unidade de resposta audível da central de atendimento, tokens de produção e dependências de ajustes pendentes na equipe de Alan (01:41:18).


**Liberação de Versão com Integração de Identidade Gov.BR**: Emerson Yamamoto anunciou que uma versão do Gov.BR para o aplicativo e para o sistema verde será liberada até o dia seguinte para homologação, incluindo correções cruciais de aplicação de verificações de identidade (01:44:14). Yann Naylor Francisco e Gustavo Pinto confirmaram que o Gov.BR já está em produção no sistema Maria, e Yann Naylor Francisco comentou que a lista de itens para homologação está extensa, mas sob controle (01:45:08).


**Alinhamento de Implantação e Pacotes de Atualização de API**: Diogo Leite Mesquita propôs alinhar o cronograma de implantação das próximas interfaces de programação de aplicativo e verificar quais itens estão homologados (01:46:07). Yann Naylor Francisco explicou que precisa de um direcionamento sobre quais pacotes podem ser subidos independentemente do status de homologação (01:47:51). Diogo Leite Mesquita apresentou uma planilha com um recorte por sprints de um a seis, destacando itens prioritários apontados por Felipe Martins Costa Brito e Ícaro Luiz Albar Eduardo (01:48:39). Emerson Yamamoto, Yann Naylor Francisco e Diogo Leite Mesquita debateram dependências externas com outros sistemas e a necessidade de criar uma nova aba na planilha para gerenciar a proposta de implantação com controle de edição compartilhado com Yann Naylor Francisco, Camila e Diogo Leite Mesquita (01:49:47).

## Relacionado
- [[2026-10-22 - Sprint - App (APIs) (transcrição)]]
- [[Maria - atendimento automatizado]]
- [[Tykhe]]
