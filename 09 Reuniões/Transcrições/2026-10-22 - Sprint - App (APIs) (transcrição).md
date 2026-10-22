---
tipo: transcricao
data: 2026-10-22
reuniao: "[[2026-10-22 - Sprint - App (APIs)]]"
tags:
  - transcricao
  - sprint
---

# Sprint - App (APIs): transcrição (22/10)

> Transcrição automática do Google Meet; pode conter erros. Ata: [[2026-10-22 - Sprint - App (APIs)]]. Encerrada após 01:56:41.

### 00:03:36

**Emerson Yamamoto:** Boa tarde, pessoal. Eh, enquanto o pessoal vai entrando, adiantando um assunto aí com Felipe Diogão, eh, eu não entrou ainda, né? A gente tá para montar uma versão com GOVBR no aplicativo para liberar num ambiente para fazer tanto uma homologação por parte de vocês quanto o nosso teste antes de subir. Eh, a gente deve liberar no ambiente temp, que é um ambiente onde a gente estava testando um login único. E e isso vai incluir tanto a parte da verificação no aplicativo quanto a visualização dessa verificação diferenciada no verde. Então vai ter meio que o ciclo completo aplicativo e verde. Eh, aí a gente deve fazer isso até amanhã, talvez, talvez segunda-feira mais ou menos já deve tá disponível para vocês testarem. E aí, tando tudo aprovado, vocês homologando e a gente testando e aprovando, a gente já poderia subir. Só teria que ver de antes de subir tem que ajustar ajustar o broker de vocês para apontar pra produção, enfim, configurar ele paraa produção. Não sei se vocês já t porque eu acho que já tá no via, né, uma coisa assim.

### 00:05:01

**Emerson Yamamoto:** Então, só avisando aí sobre esse assunto do GOV. Yeah. E aí tem uma outra notícia também boa, Felipe, que é junto com essa versão, a gente vai subir algumas correções do aplicativo e uma delas é com relação à niplicação de verificações de identidade, porque parece que a tentativa que a gente teve a primeira vez não resolveu. Então, até hoje as pessoas estão conseguindo enviar duas, três verificações no mesmo segundo ali, só que dessa vez a gente fez uma uma verificação bem mais rígida, então deve subir junto com essa versão do gov essa questão de não gerar várias verificações,

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** é, é o problema que a gente reportou ontem,

**Emerson Yamamoto:** Eu não sei,

**Felipe Martins Costa Brito:** né?

**Emerson Yamamoto:** mas essa porque essa Issueé antiga já e ela nunca fechou,

**Felipe Martins Costa Brito:** Não tem Bianca não tá aqui conosco não, né? Ainda não, né? Eh,

**Emerson Yamamoto:** mas ela me passou sim, Felipe.

**Felipe Martins Costa Brito:** como passou?

**Emerson Yamamoto:** Eh,

**Felipe Martins Costa Brito:** Ah, então beleza.

### 00:06:08

**Emerson Yamamoto:** isso,

**Felipe Martins Costa Brito:** Fou.

**Emerson Yamamoto:** ela me passou um caso inicial que era de 2024 e agora acho que ela me passou casos mais recentes.

**Felipe Martins Costa Brito:** E um dia recente, né?

**Emerson Yamamoto:** Então,

**Felipe Martins Costa Brito:** É.

**Emerson Yamamoto:** de 2026 para trás, realmente a gente não mexeu. Então, assim, não teve limpeza. Quando a gente fez a limpeza, a gente fez 2026. Eu posso até organizar de fazer a limpeza geral. São vão ser muitos registros, mas dá para fazer. E eu tô fazendo essas pontuais também. Então, qualquer coisa eu vejo de fazer uma limpeza geral e depois a gente sobe essa versão, a gente tem fé que vai resolver.

**Felipe Martins Costa Brito:** Так.

**Emerson Yamamoto:** E vai corrigir também a questão do bloqueio da versão antiga, porque você tinha pedido para para bloquear as versões antigas do app quando a gente subiu essa alteração do push

**Felipe Martins Costa Brito:** Угу.

**Emerson Yamamoto:** do push token. Só que eu identifiquei, a gente até bloqueou em produção, mas quando eu fui testar no meu celular, eu identifiquei que uma das telas ela ficava sempre bloqueada, aí você tinha que fechar o app, enfim, era era uma burocracia que provavelmente ia dar muita reclamação.

### 00:07:06

**Emerson Yamamoto:** E aí a gente corrigiu isso também. Então, a próxima vez que subir um app que precisar bloquear, a gente já vai conseguir também.

**Felipe Martins Costa Brito:** Show. Ô Diogo, tu não quer aproveitar ainda que a gente tá nas introduções tocar no assunto que eu falei contigo não

**Diogo Leite Mesquita:** Sim, pode ser. Eu acho que tem a ver inclusive com o que o Emerson falou aí ou Emerson. Eh, a questão das APIs hoje imagino que vocês vão mostrar algumas coisas de API, que eu não sei se a gente tem já algum plano, plano de deploy de próximas subidas de API. Deixa eu até aproveitando que o Gustavo entrou aí também.

**Emerson Yamamoto:** É, na verdade, isso é uma coisa que eu tenho falado com o Gustavo há algum tempo já. Eu até passei pro Felipe a tabela também para ele dar uma olhada, porque a minha ideia fazendo isso e é a gente decidir qual vai ser a próxima subida de integra, porque chatbot, por exemplo, tudo que é site WhatsApp já tem mais de 20 Issues,assim, tá muito acumulado e tem muita coisa que acho que seria bom subir, que que realmente ia agregar valor pro fluxo.

### 00:08:12

**Emerson Yamamoto:** Então eu pedi ajuda do Felipe, ele dar uma olhada também para ver o que que seria legal. Assim, nem tudo tá homologado, tem algumas que estão homologadas. Mas também se for o caso da gente fechar um pacote, a gente pode, vocês podem, né, se for possível, fazer um esforço de homologação só para as pontuais que que precisam subir.

**Felipe Martins Costa Brito:** Eh, não, eu separei oito Issuesque já estão homologadas.

**Emerson Yamamoto:** Ah, sim, que são importantes

**Felipe Martins Costa Brito:** Diogo. É, pelo menos essas oito podia e umas outras eu já passei pro Ian para ver se o Ian consegue

**Emerson Yamamoto:** homologar,

**Felipe Martins Costa Brito:** dar.

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** Ja.

**Emerson Yamamoto:** É, a única sprint que não tá em homologação é a Sprint 11, que é a última. Tem poucas fichas dela. Se não for da Sprint 11, é tranquilo. Se for, a gente até consegue, né, subir, mas como é sprint anterior, a gente ainda tava refinando, ainda não disponibilizamos. De qualquer forma, eu botei lá só pra gente ter esse controle.

### 00:09:11

**Diogo Leite Mesquita:** É, não sei se a gente vai conseguir chegar nesse acordo aí. Talvez, Gustavo,

**Emerson Yamamoto:** Sim.

**Diogo Leite Mesquita:** a gente pode pensar, né, nessa próxima onda e a gente fazer um corte. A Camila falou que atrasar um pouquinho o Ian também, eu preciso deles, mas a gente tentar chegar a um acordo no que dá para subir, entendeu? De fazer um corte aí de se essas que o Felipe precisa de prioritárias estão homologadas.

**Emerson Yamamoto:** Угу.

**Diogo Leite Mesquita:** Eu não sei qual é sprint dessas is que ele falou, a gente tentar fazer essa aí, né? Não sei se são furafila ou não, de outras sprints, mas fazer um corte até sprint se a gente tentar fazer um esforço para até semana

**Emerson Yamamoto:** Sim.

**Diogo Leite Mesquita:** que vem algum dia e a gente conseguir subir, entendeu? Tentar fazer um uma primeira onda.

**Emerson Yamamoto:** O único ponto, Diogo, é que assim, quando eu falo subir até sprint 6, pode ser que eu esteja incluindo coisas que o Felipe não escolheu. E aí o único problema eh é que tem coisas que a Tike precisa se adaptar,

### 00:10:00

**Diogo Leite Mesquita:** Exato.

**Emerson Yamamoto:** que não são só mudanças de API, às vezes muda um comportamento que a Tik precisa ajustar. Então a gente vai ter que olhar direitinho depois qual foi a seleção que a gente fez.

**Diogo Leite Mesquita:** Mas aí seria aquela coluna do tipo, depende de outro sistema. Sim. Não,

**Emerson Yamamoto:** Não, isso é nosso assim,

**Diogo Leite Mesquita:** não, né?

**Emerson Yamamoto:** a dependência é nossa, tipo, depende subverde, depende. Se se depende de a tai que alterar algo, eu não tô colocando ali, entendeu?

**Diogo Leite Mesquita:** A gente teria que evoluir aquela planilha para ter uma depende de T ainda,

**Emerson Yamamoto:** aqui.

**Diogo Leite Mesquita:** né?

**Emerson Yamamoto:** É, pode ser porque mas é fácil de ver isso. Assim, basicamente lendo a isto dá para ter uma ideia se vai alterar o fluxo atual ou não. Mas eu posso tentar criar uma coluna lá que identifique se afeta o fluxo da T ou não,

**Diogo Leite Mesquita:** Ja.

**Emerson Yamamoto:** porque tem coisas até que são campos novos que não alteram fluxo, por exemplo, lá, tá, vai retornar uma informação nova, tanto faz.

### 00:10:57

**Emerson Yamamoto:** Claro, talvez se a Tik tiver que recuperar esse campo para alguma coisa altera, mas tem coisas que realmente não tem pago.

**Diogo Leite Mesquita:** Beleza. Vamos tentar fazer um recorte aí do se não vai conseguir resolver isso agora. Olha aí, Gustavo.

**Gustavo Pinto:** Eh, se o Filipe Martins puder compartilhar com a gente qual é a lista de issuesque ele já selecionou, eh, seria bom pra gente já até tentar pegar essa situação de o que que tem provável envolvimento com a Tik,

**Felipe Martins Costa Brito:** Eu tô tô mandando teu WhatsApp agora,

**Gustavo Pinto:** né?

**Felipe Martins Costa Brito:** Gustavo.

**Gustavo Pinto:** Ah, beleza. E aí a gente consegue pelo menos pegar essas e já dar uma olhada, né?

**Felipe Martins Costa Brito:** Eu acho que essa tem, acho que só tem uma ou duas que depende, tá?

**Gustavo Pinto:** tá?

**Emerson Yamamoto:** É,

**Gustavo Pinto:** que aí teria Так.

**Emerson Yamamoto:** aí dependendo do que depende vai ser mais complicado. Por exemplo, se for prioridade não tem como. Se for data inválida, até dá, mas é um pacote bem grande data inválida.

### 00:11:52

**Emerson Yamamoto:** Então tem que ver que dependência é essa. Se for dependência só de subir a mesma versão, é mais tranquilo. Mas aí a gente vê lá quando você mandar a lista. Bom, tá todo mundo aí, exceto Farias, a gente teve uma surpresa em 2:20 ele falou que a internet dele lá

**Gustavo Pinto:** О.

**Emerson Yamamoto:** tava oscilando e ele não tá conseguindo conectar e eu deixei ele por

**Gustavo Pinto:** Ja.

**Emerson Yamamoto:** acaso na ordem, ele tá por último. Então eu vou torcer aqui para até chegar a vez dele ele conseguir entrar. Ele até passou um roteiro aqui, mas como foi muito em cima da hora, foi tipo faltando 10 minutos, nem deu pra gente preparar nenhuma substituição. Eu posso até tentar aqui lendo as instruções que ele tá colocando aqui, mas não vai ser uma apresentação tão fluída como geralmente é. Então vou começar com os outros meninos e a gente torce para até a hora de chegar a parte dele, ele tá presente. Beleza? Show. Vamos começar pelo app, então. Vou apresentar as issuesde app, vou compartilhar a tela aqui, mas para adiantar, a gente vai começar com as IS do app e depois a gente passa paraa API, beleza?

### 00:13:13

**Emerson Yamamoto:** Compartilhar aqui para mostrar para vocês o que a gente vai apresentar hoje. Beleza? Então, a gente tá com essas nove IFs aqui, eh, acho que são cinco de app, quatro, na verdade, e cinco de integra, eu coloquei na ordem aqui de apresentação. Beleza? A primeira de 10468, alterar fluxo de primeiro atendimento para verificar a associação entre assunto verde e CNJ. Essa é uma Ixa que já foi feita no verde também. Enfim, ela vai ser feita também eh, se eu não me engano, paraa integra aqui. Ela ela só não é no mesmo fluxo, mas na consulta de casos. Então, essa e essa estão relacionadas, que é basicamente quando a gente buscar por um assunto verde, a gente vai usar aquele mapeamento entre assunto verde e assunto CNJ para saber se tem ali um caso processual, direcionar para um atendimento eh processual, tá? Isso é uma isso que a gente apresentou no verde na última sprint. Então a gente tá trazendo aqui tanto pro app quanto paraa Integra também. Beleza? A 1493, alterar conclusão de agendamento para solicitar preferência de recebimento de informações sobre o agendamento pelo WhatsApp.

### 00:14:33

**Emerson Yamamoto:** Essa daqui é uma bem legal que ao finalizar o agendamento a gente vai mostrar uma janelinha que pergunta se você desejaria receber notificações desse agendamento por WhatsApp. E aí a gente marca isso no próprio agendamento, no próprio evento. É uma configuração individual do evento. É, depois eu até vou abordar que tem alguns pontos aqui que eu achei eh que poderiam melhorar, mas no geral é isso. Depois a gente tem a 1048, que é o alterar encaminhamento presencial para destacar a observação do endereço dos órgãos. Essa é uma que eh principalmente paraa justiça itinerante, se eu não me engano, tem ali uma configuração específica para itinerante. Eh, essa ficou um pouco confusa porque olhando no banco de produção, eh, parece que a observação não é sempre preenchida. Na verdade, de itinerante nenhuma tem observação, por exemplo, mas tem, por exemplo, complemento na praça do não sei o quê. Então, tem algumas eh alguns comentários sobre essa também, mas é basicamente isso, é dar um destaque, um negrito ali nesses campos, na parte do endereço dos órgãos. Depois a gente tem a 10513, que é alterar encaminhamento processual utilizando o órgão colegiado para mapeamento de atendimento no EPROC 2G, que é uma issueque também já foi desenvolvida pelo verde, que é parar de usar o órgão TJ e passar a usar o órgão colegiado nos processos que são EPROC 2G, porque é nesse campo que a gente tem o depar correto, né?

### 00:16:10

**Emerson Yamamoto:** O o órgão TJ é sempre um desembargador e aí o órgão correto vem nessa parte de órgão colegiado. A mesma ISO na integra é a 10517, que é logo a próxima. E aí vai na continuidade e na transição entre e integra PI. Então a gente tem a mesma questão. Quando a gente for consultar o órgão ali, a gente vai consultar considerando esse órgão colegiado. A 10464 eu já comentei também que é aquela questão do mapeamento entre assunto verde CNJ na consulta de casos. Então essa consulta de casos, a gente precisou alterar um pouco a forma como ela funcionava para se a se adequar, né, se adaptar a essa essa nova questão. Então a gente vai explicar como é que ficou agora a nova consulta. Depois a gente tem a 10489 já no na barreira da Integra PI, que é alterar consulta de órgãos de atendimento processual para retornar trecho para justiça itinerante, que é específico ali paraa parte de justiça itinerante. Eh, algumas informações. Depois a gente tem a 10627, que é o receber status de pré-atendimento vinculado a agendamento.

### 00:17:23

**Emerson Yamamoto:** que a gente entra nas listas do Farias, eh, que aqui é basicamente a o Fariasatendimento poder alterar o status desse pré-atendimento aqui no verde, porque hoje a gente cadastra um pré-atendimento, mas ele fica lá só como cadastrado, associado ao agendamento, mas a gente não sabe se a pessoa já enviou documentos, se ela já finalizou, enfim, não tem esse status. Então o defensor ou o usuário do verde não consegue saber em que pé está esse pré-atendimento. Então, a gente vai disponibilizar esse end point para que própria possa atualizar esse status, então saber quantos documentos ele enviou, se ele já inicializou, se ele já finalizou. E o 10628 é nessa mesma linha, mas alterando o serviço de recebimento do link para inicializar esse status como pendente, porque como a gente não tinha status ainda, quando a gente gerava um link de pré-atendimento, a gente só fazia o vínculo com o agendamento e nada mais. E agora, como a gente vai ter de fato eh um status desse pré-atendimento, a gente já vai dar o start assim que gerar o link com esse status pendente.

### 00:18:36

**Emerson Yamamoto:** Beleza? Então essas duas aqui relativas ao Fariasatendimento. Show. É isso que a gente tem para apresentar hoje. Eh, a gente vai começar com Marcos, juntamente com Leonardo de Melo, vão apresentar essas três do e logo depois o o Leonardo vai apresentar a última e aí a gente vira a chave paraa integra. Beleza? Aí, Felipe, não sei, mas talvez, talvez app, com certeza integra, não sei, porque é bem parecido com o resto, então talvez daqui depois do app você já possa se liberar.

**Felipe Martins Costa Brito:** M.

**Emerson Yamamoto:** Beleza? Então, vou passar aí pro Marcos e pro Leonardo de Melo, e eles vão fazer essa apresentação.

**Marcos Benigno:** Só pessoal, vou apresentar minha tela aqui. Tá? Eh, a primeira iso que eu vou apresentar é a 10 e assento 468. Eh, tem o título Alterar fluxo de primeiro atendimento para verificar mapeamento entre assunto verde e CNJ. Eh, nessa ISO, eh, basicamente descreve uma funcionalidade que ao você iniciar um primeiro atendimento, eh, ao selecionar o assunto, eh, é pesquisado se você tem um CP em andamento, eh, de acordo com aquele assunto, eh, para aquele usuário que tá consultando.

### 00:20:14

**Marcos Benigno:** É, e se tiver, aparece uma mensagem, é, perguntando se aquele usuário quer falar sobre aquele processo e eh se ele marcar que afirmativo, ele é redirecionado pro atendimento, eh, pro encaminhamento, de acordo como se tivesse, eh, pesquisado a aquele processo que, eh, foi identificado. Eh, caso negativo, eh, o fluxo eh percorre normalmente o fluxo de primeiro atendimento. Bom, eh, vou mostrar para vocês como tá funcionando no aplicativo. Fazer um novo caso aqui. Uso capião imóvel. OK. Eh, nessa tela aqui, eh, que é onde ocorre a seleção do assunto. Clicando no próximo, ele vai pesquisar e aparece aqui a a indicação a eh atendimento em andamento. Você já possui um atendimento em andamento para o processo número sobre o assunto? gostaria de falar sobre o assunto desse processo. Eh, então, se o usuário clicar sim, ele vai ser redirecionado lá pro para continuar eh para fazer um encaminhamento de acordo nos moldes do fluxo do processo. E eh se ele clicar não, ele continua eh criando o primeiro atendimento no fluxo normal.

### 00:21:33

**Marcos Benigno:** Vou clicar aqui sim para não ser redirecionado. OK. foi direcionado fluxo de buscar processo já na na busca do atendimento. E nós temos aqui fizemos o encaminhamento. E é basicamente isso para essa

**Emerson Yamamoto:** Só uma questão, Marcos, que foi uma questão que a gente abordou na interna nossa e talvez Felipe e Taiana possam ajudar, que é a questão em relação à urgência. A gente ficou com dúvida, Felipe, porque tem alguns assuntos que baseados no complemento geram urgência, por exemplo, corte de luz. Não sei se em produção tá assim ainda, né? Mas em geral sempre fez isso. E aí a gente ficou em dúvida se a gente eh se para urgência também deveria fazer isso, ou seja, eu posso fazer isso antes mesmo do complemento ou se de fato eu preciso esperar que a pessoa coloque o complemento para saber se tem urgência e só se não tiver eu mostrar essa questão do processo.

**Felipe Martins Costa Brito:** Eh, complicou um pouco para mim, porque assim, em tese, assunto CNJ não vai ter essa conferência de urgência, porque a conferência, essa conferência de urgência que você tá mencionando é assunto verde.

### 00:22:53

**Emerson Yamamoto:** é do assunto.

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** Isso é porque o que eu tô falando é eu preciso primeiro escolher o assunto verde para depois bater o assunto CNJ para depois ver se ele tem um caso.

**Felipe Martins Costa Brito:** sim.

**Emerson Yamamoto:** Então, o que eu quero dizer é, eu, por exemplo, corte de luz, eu poderia fazer essa verificação antes mesmo de saber se isso vai gerar uma urgência ou não, entendeu?

**Felipe Martins Costa Brito:** Ah, entendi. Entendi. Sim. É, não. Sim, sim.

**Emerson Yamamoto:** Posso fazer antes,

**Felipe Martins Costa Brito:** Vai fazer.

**Emerson Yamamoto:** então, né?

**Felipe Martins Costa Brito:** Pode, pode.

**Emerson Yamamoto:** Tá? Essa era a nossa dúvida, porque realmente a gente colocou antes do do complemento. Então aqui, por exemplo, se fosse um assunto com complemento, eu ia primeiro ver isso e só se eu continuasse, provavelmente ele ia cair no complemento, certo? Marcos, depois que ele vai pro complemento, né?

**Marcos Benigno:** Sim.

**Emerson Yamamoto:** Exato. Aí eu fiquei preocupado porque em geral a urgência tem um comportamento diferente.

### 00:23:41

**Emerson Yamamoto:** Mas beleza. Então, então tá feito direitinho. Eh, pode seguir então, Marcos.

**Marcos Benigno:** Show. Vou vou partir paraa próxima então que é a 7493 o título alterar conclusão do agendamento para solicitar preferência de recebimento Yeah. informações sobre o agendamento pelo WhatsApp. Eh, basicamente, eh, essa ISO eh descreve a funcionalidade de que ao finalizar um o um atendimento, eh, na tela de sucesso aparece uma janelinha perguntando pro usuário se eh ele quer receber mais informações sobre aquele agendamento realizado pelo WhatsApp. Eh,

**Emerson Yamamoto:** M.

**Marcos Benigno:** vou mostrar para vocês como ficou. Eh, fazer um aqui. OK. Eh, aparece esse card aqui, eh, em cada agendamento ou ou reagendamento, eh, que é com essas informações. Se o usuário quer receber informações pelo WhatsApp, eh, o texto é além do aplicativo, você pode receber pelo WhatsApp as informações sobre este agendamento. Então, o usuário pode clicar no sim e é enviado, aparece uma mensagem de pronto, você também receberá eh pelo WhatsApp as informações sobre esse agendamento ou não. que tudo bem falando pro usuário que ele não vai receber e é isto.

### 00:25:31

**Emerson Yamamoto:** Aí, só uma coisa aí, né? Marcos, que a gente não mostrou que é o seguinte,

**Marcos Benigno:** Uhum.

**Emerson Yamamoto:** se você não interagir com isso aí e apenas clicar em OK,

**Marcos Benigno:** Sim.

**Emerson Yamamoto:** ele vai te ele vai confirmar ainda, ele vai abrir um pop-up um pouco mais invasivo, perguntando você vai gostaria de receber sim ou não? E você vai responder. Se você interagir ali como o Marcos fez agora, dá para ver que não aconteceu nada.

**Marcos Benigno:** Sim, vou mostrar para vocês o tático.

**Emerson Yamamoto:** Deixar o Marcos mostrar.

**Marcos Benigno:** Show. Não vou interagir com o cardzinho de receber informações. Aí se o usuário clicar no chequezinho aqui, aparece esse modal.

**Emerson Yamamoto:** Isso aí, exatamente isso. Então, ainda assim a gente pergunta para ter certeza que ele vai responder. Beleza? Tranquilo isso, Felipe.

**Felipe Martins Costa Brito:** Tranquilo. M.

**Emerson Yamamoto:** Aí uma dúvida que a gente ficou também, Felipe, na interna, eh, é o seguinte. Vai, faz sentido eu mostrar isso, ainda que o usuário não tenha telefone com WhatsApp?

### 00:26:52

**Emerson Yamamoto:** Porque eu fiquei pensando que talvez não possa fazer muito sentido assim o cara falar: "Pô, mas eu nem tenho telefone no WhatsApp, eu nem cadastrei telefone Sei lá,

**Felipe Martins Costa Brito:** É, mas a minha pergunta é essa. Se ele não tiver o telefone cadastrado, isso aparecer.

**Emerson Yamamoto:** não muda nada, porque essa configuração é uma configuração que a gente vai colocar no evento.

**Felipe Martins Costa Brito:** Sim, mas aí,

**Emerson Yamamoto:** Então não,

**Felipe Martins Costa Brito:** mas a gente vai pedir para ele informar o telefone.

**Emerson Yamamoto:** não vai acontecer nada.

**Felipe Martins Costa Brito:** Verificamos que você não tem telefone cadastrado, que enviabiliza o envio,

**Emerson Yamamoto:** Não, não, não faz isso. A iso

**Felipe Martins Costa Brito:** porque nessa hora a gente tá olhando pro pro cadastro dele no verde, não no cadastro dele do app, né? Eu sei que são não,

**Emerson Yamamoto:** é o mesmo cadastro.

**Felipe Martins Costa Brito:** eu sei que são mesmo, mas digo assim, no se ele já informou, ele não informou no app, mas tem no no banco do verde, a gente vai mandar pro telefone do que tá no carta, né?

### 00:27:34

**Emerson Yamamoto:** Então eu eu não tem como porque se ele tem no verde,

**Felipe Martins Costa Brito:** Não

**Emerson Yamamoto:** ele tem no app.

**Marcos Benigno:** Всё.

**Emerson Yamamoto:** É a mesma cadastro de pessoa, entendeu? Não, não é, não são coisas diferentes,

**Felipe Martins Costa Brito:** entendi. E eu sei o mesmo banco,

**Emerson Yamamoto:** é o mesmo banco.

**Felipe Martins Costa Brito:** mas assim, a minha minha questão era se ele não tivesse inserido, não ia ficar amarrado nisso. Basta ter no banco do vente que vai disparar, né?

**Emerson Yamamoto:** Se você quiser que seja condicional.

**Felipe Martins Costa Brito:** É isso.

**Emerson Yamamoto:** Não entendi.

**Felipe Martins Costa Brito:** Não é pelo ao contrário, não é condicional a ele informar.

**Emerson Yamamoto:** Sim,

**Felipe Martins Costa Brito:** Se você já tiver no verde,

**Emerson Yamamoto:** isso vai disparar.

**Felipe Martins Costa Brito:** vai disparar do mesmo jeito.

**Emerson Yamamoto:** Exatamente. Se tiver, vai disparar. Se não tiver, não vai acontecer nada porque não tem telefone com WhatsApp. Entendeu?

**Felipe Martins Costa Brito:** Entendi.

**Emerson Yamamoto:** Porque isso, como eu falei, isso é uma configuração que fica no agendamento.

### 00:28:13

**Emerson Yamamoto:** Então o agendamento vai ter lá, eh, deseja notificar o WhatsApp, sim ou não? Quando a gente for fazer qualquer ação que deve enviar um WhatsApp, a gente vai olhar esse agendamento aqui, ele botou que quer receber? Sim, então tenta enviar. Não tem telefone, então não vou enviar. Tem telefone, então vou enviar. Disse que não, então não vou enviar.

**Felipe Martins Costa Brito:** Mas aí a gente também não vai dar nenhum retorno para ele,

**Emerson Yamamoto:** Entendeu?

**Felipe Martins Costa Brito:** né? Olha, não foi possível enviar nada disso.

**Emerson Yamamoto:** Como? Porque isso aí vai acontecer provavelmente depois, entendeu? Porque as informações do agendamento vão ser, sei lá, se foi desmarcado ou sei lá, alguma coisa que é posterior ao agendamento, né? Tipo, não é aí que ele vai receber a notificação, é mais pra frente. Aí como é que a gente avisa ele se ele não tem WhatsApp?

**Felipe Martins Costa Brito:** Não é, acho que não tem jeito. Acho que isso vai.

**Emerson Yamamoto:** Entendeu? Eu só tô falando porque ele pode, por exemplo, nem ter telefone cadastrado e isso vai aparecer.

### 00:29:06

**Emerson Yamamoto:** Eh,

**Felipe Martins Costa Brito:** Sim.

**Emerson Yamamoto:** então não afeta nada, ele só não vai receber mesmo.

**Felipe Martins Costa Brito:** É, se a gente pudesse, talvez ele não na hipótese ele não tem telefone cadastrado, a gente pedir para ele informar, olha, não localizamos nenhum telefone, por favor, informe.

**Emerson Yamamoto:** Então, eu acho que é possível eh quando a gente colocar o sim, a API poderia retornar se ele tem ou não telefone, porque não precisa ser no não, por exemplo, porque o não, ele já disse que não.

**Felipe Martins Costa Brito:** Não é exatamente só no Sim.

**Emerson Yamamoto:** Então, botei sim, a API retornou uma mensagem específica, eu posso dar uma mensagem e direcionar ele paraos meus dados para ele cadastrar um telefone com WhatsApp. É possível fazer isso?

**Felipe Martins Costa Brito:** E aí depois que ele informar e dispararia.

**Emerson Yamamoto:** Pode ser não. Aí depois que ele informar vai ficar salvo. Quando disparar é porque o que eu tô entendendo é disparar é quando tiver algo para notificar, entendeu? Quando tiver algo para notificar. ficar sobre esse agendamento. Sim, ele vai receber porque eu tenho telefone lá.

### 00:30:01

**Felipe Martins Costa Brito:** Não, não, não, não. Então,

**Emerson Yamamoto:** Ah,

**Felipe Martins Costa Brito:** a gente tá falando de de diferente.

**Emerson Yamamoto:** sim.

**Felipe Martins Costa Brito:** O que a minha expectativa era? Você quer saber informações sobre esse agendamento? São os dados de sucesso do agendamento.

**Emerson Yamamoto:** Ah, é ess mesmos dados aí?

**Felipe Martins Costa Brito:** Sabe o e-mail que a gente é exatamente?

**Emerson Yamamoto:** É porque hoje ele não tá enviando. Essa aqui é a questão. Isso aí, essa isso aqui foi só para colocar esse aviso, entendeu? Pode falar, tá?

**Thaiana Lima:** Hum. Gente, eu não tô sabendo de nada dessa iso, tá?

**Felipe Martins Costa Brito:** Ah,

**Thaiana Lima:** Eh, eu pergunto,

**Felipe Martins Costa Brito:** não foi contigo.

**Emerson Yamamoto:** Ah, é da Talita,

**Thaiana Lima:** não, pergunta catalista.

**Emerson Yamamoto:** é verdade.

**Thaiana Lima:** É, mas o jeito que tá escrito ali, ela realmente tá só guardando a preferência.

**Emerson Yamamoto:** A informação. Exatamente.

**Felipe Martins Costa Brito:** Então é assim,

**Thaiana Lima:** Eh,

**Felipe Martins Costa Brito:** a a minha expectativa da ISO era fazer com que ele recebisse a lista de documentos e os dados de confirmação do agendamento no WhatsApp, assim como ele recebe por

### 00:30:46

**Thaiana Lima:** que eu pergunta ali é se no sim, além de verificar se ele não tem telefone para cadastrar, verificar se ele tem um telefone que tá sem WhatsApp, porque se ele tem, de repente ele só falar: "Esse telefone aqui, eu recebo WhatsApp".

**Felipe Martins Costa Brito:** Ah, tudo bem. Mas aí como é que a gente faz? Porque assim, só isso não resolve,

**Emerson Yamamoto:** Não deve ter outra iso talvez, né, para para enviar de fato,

**Felipe Martins Costa Brito:** cara.

**Emerson Yamamoto:** porque aqui é para guardar.

**Felipe Martins Costa Brito:** Não sei,

**Emerson Yamamoto:** Será que não é?

**Felipe Martins Costa Brito:** não sei. Tá, tá aí, ó, na live.

**Thaiana Lima:** Não, não sei também.

**Emerson Yamamoto:** Porque a ISO tá bem claro dizendo para solicitar preferência de recebimento. Não tem nada de sobre enviar, entendeu?

**Thaiana Lima:** É,

**Emerson Yamamoto:** Até porque o enviar é muito mais complicado,

**Thaiana Lima:** talvez ela tenha entendido o que era em outros momentos,

**Emerson Yamamoto:** né? Fala aí.

**Felipe Martins Costa Brito:** Mas

**Thaiana Lima:** no verde, no chat do site.

### 00:31:26

**Emerson Yamamoto:** É, eu também entendi exatamente assim que eu tinha entendido. Não entendi que era essa tela aqui, não, tá, Felipe?

**Felipe Martins Costa Brito:** é,

**Emerson Yamamoto:** Entendi que era tipo,

**Felipe Martins Costa Brito:** mas era mas era essa a tela com a lista de documentos

**Emerson Yamamoto:** é, eu não tinha entendido isso também não, mas assim, também não falei com a Talita. Talvez a Talita tenha outra percepção.

**Felipe Martins Costa Brito:** e et a gente fazer o quê então?

**Thaiana Lima:** Eu acho que essa questão do sim verificar se tem telefone dá fazer com refinamento, talvez, néon? E e o envio tem que percutar ali.

**Emerson Yamamoto:** Fala aí, Gustavo.

**Gustavo Pinto:** Eh, eu me lembro um pouco sobre essa essa conversa, mas eu tava entendendo que primeiro a gente ia capturar a intenção da pessoa sobre dar continuidade pelo pelo WhatsApp e depois isso entraria numa outra num outro direcionamento, né? Não,

**Felipe Martins Costa Brito:** Mas eu não eu não tô conseguindo eu não tô conseguindo entender qual é a vantagem de apenas

**Gustavo Pinto:** a confirmar.

**Felipe Martins Costa Brito:** guardar.

**Emerson Yamamoto:** É porque a gente consegue eh é porque é isso, né, Felipe?

### 00:32:28

**Emerson Yamamoto:** guardar é importante se o aviso não é agora, se o aviso é para outras coisas sobre esse agendamento,

**Gustavo Pinto:** É,

**Felipe Martins Costa Brito:** Mas mas aí,

**Emerson Yamamoto:** porque então qualquer coisa que

**Felipe Martins Costa Brito:** mas quem é que vai conduzir esse disparo depois?

**Gustavo Pinto:** não tinha,

**Felipe Martins Costa Brito:** Eh,

**Marcos Benigno:** Eh

**Felipe Martins Costa Brito:** eh.

**Gustavo Pinto:** então não.

**Emerson Yamamoto:** aconteça, por exemplo, cancelei o agendamento,

**Gustavo Pinto:** Ô,

**Emerson Yamamoto:** aviso por WhatsApp, sei lá, o agendamento foi reagendado, eu consigo avisar pelo WhatsApp,

**Gustavo Pinto:** ô,

**Emerson Yamamoto:** qualquer ação.

**Gustavo Pinto:** Felipe, não era aquela questão também de quando fosse eh a Tai consultasse, a gente teria que a os que não quer por WhatsApp, a gente iria mudar. Yeah. também aquela confirmação de agendamento e tudo mais.

**Felipe Martins Costa Brito:** Não sei, Gustavo.

**Gustavo Pinto:** Acho que eu acho que tinha uma história sim, mas assim, confesso que a a é a Talita que pode eh complementar,

**Felipe Martins Costa Brito:** É, esclareceram.

**Gustavo Pinto:** entendeu? Esclarecer, mas eu me lembro um pouco da quando a gente tava discutindo aquela questão de se e vai mandar de novo a confirmação pro cara, como é que a gente vai saber se é para mandar para ele ou não é para mandar para ele mais?

### 00:33:24

**Gustavo Pinto:** Eu acho que isso tá tá um pouco naquele conjunto de discussões que a Talita tava fazendo naquele dia que a gente

**Felipe Martins Costa Brito:** É,

**Gustavo Pinto:** tava conversando com a Ti, entendeu? Com a Luna.

**Felipe Martins Costa Brito:** entendi. Mas o meu objetivo quando eu pedi isso era era isso,

**Gustavo Pinto:** Uhum.

**Felipe Martins Costa Brito:** ele receber por WhatsApp a lista de documentos e os dados do agendamento.

**Gustavo Pinto:** Entendi. Tá.

**Felipe Martins Costa Brito:** Então, se for o caso, t depois esclarece com ela e aí vai ter que fazer uma iso para complementar essa. F.

**Thaiana Lima:** Tá, vou perguntar para ela se já tem. De repente ela colocou meio separado. Não sei.

**Gustavo Pinto:** É, pode ser que ela tenha feito isso em dois passos, né,

**Thaiana Lima:** Eu vou ach, eu acho meio um pouco estranho não que isso invalide.

**Emerson Yamamoto:** É, para mim é estranho porque não precisaria guardar, né,

**Thaiana Lima:** É,

**Emerson Yamamoto:** Thaiana?

**Thaiana Lima:** assim, poderia aguardar para essa questão de reagendamento, cancelamento e em outros meios, mas enviar na hora e iria tá aqui de qualquer forma, né?

### 00:34:15

**Thaiana Lima:** Então, talvez ela não tenha entendido.

**Felipe Martins Costa Brito:** Porque o que vocês estão entendendo que seria a ao invés de notificar a pessoa pelo aplicativo de eventuais reagendamentos, chegou mensagem, iria notificar a pessoa pelo WhatsApp. É, é essa a leitura que eles estão fazendo?

**Gustavo Pinto:** Eu tinha entendido que iria ser uma marcação, ô Felipe, sobre se a pessoa quer ser atendida no futuro pelo WhatsApp e ser receber mais interações pelo WhatsApp ou não, entendeu?

**Felipe Martins Costa Brito:** Não. Sim, mas assim, eh ele respond,

**Gustavo Pinto:** Угу.

**Felipe Martins Costa Brito:** vamos supor, subir em produção hoje, ele respondendo sim, ele não vai receber mais nada para WhatsApp, na prática não vai receber mais nada.

**Emerson Yamamoto:** Não,

**Felipe Martins Costa Brito:** se não vai subir.

**Emerson Yamamoto:** só se reagendar, desmarcar, né?

**Felipe Martins Costa Brito:** Então aí a ideia é que venha substituindo,

**Gustavo Pinto:** Eu

**Felipe Martins Costa Brito:** que ele seja tudo que ele seria notificado pro no app, ele passa ser notificado também pro WhatsApp.

**Emerson Yamamoto:** Por Push e receba também pro WhatsApp. Exatamente.

**Felipe Martins Costa Brito:** É essa a leitura que vocês estão fazendo.

### 00:35:12

**Emerson Yamamoto:** Não, isso é a leitura que eu fiz lendo aí só,

**Gustavo Pinto:** tô entendendo que seria é Ja.

**Emerson Yamamoto:** tá, Felipe? Não participei da discussão.

**Felipe Martins Costa Brito:** Eu tenho certeza que não tem isso dessa parte de notificação.

**Emerson Yamamoto:** Entendi. Que é só essa daqui mesmo.

**Felipe Martins Costa Brito:** Uhum.

**Thaiana Lima:** É, mas a gente consegue colocar o envio aqui,

**Felipe Martins Costa Brito:** Eu

**Thaiana Lima:** que é o envio que já existe hoje, né, de confirmação, eh, que a T já chama a gente para fazer esse envio, né?

**Emerson Yamamoto:** Acho que dá. Só que não dá para fazer isso como refinamento, porque isso é muito mais complicado, entendeu? Tipo, fazer como refinamento não,

**Gustavo Pinto:** Acho melhor conversar com a Talita.

**Emerson Yamamoto:** não tá na inrito,

**Gustavo Pinto:** Eu acho melhor conversar com a Talita.

**Emerson Yamamoto:** é complicado. É.

**Gustavo Pinto:** É, até mesmo para saber se isso tem alguma coisa que foi.

**Felipe Martins Costa Brito:** até eu eu até gostei da ideia

**Gustavo Pinto:** Pode falar, Felip.

**Felipe Martins Costa Brito:** de notificar, mas eu não tinha tinha tido essa ideia antes,

### 00:35:56

**Gustavo Pinto:** Uhum.

**Felipe Martins Costa Brito:** então, certamente não tem iso disso.

**Thaiana Lima:** Tá,

**Felipe Martins Costa Brito:** E a gente é aí,

**Thaiana Lima:** já mandei até mensagem para ela, As.

**Felipe Martins Costa Brito:** eu acho que a gente pode fazer duas, então, uma para que a pessoa receba o o sucesso do agendamento do encaminhamento por WhatsApp e uma outra de que toda notificação que ele receberia no no app, ele também passa a receber WhatsApp, entendeu?

**Emerson Yamamoto:** Eh É porque assim também tem outra coisa, Felipe, como a gente vai verificar se ele tem telefone e ainda que ele tenha telefone cadastrado, mas não tem indicação do WhatsApp, a gente vai pedir para ele informar um telefone. Eh, se for para enviar aqui, vai ser muito mais complicado se a gente for pra tela de meus dados para depois voltar, vai ficar ruim esse fluxo. Então, o que eu sugiro, talvez é até mostrar só um campo de telefone, se ele não tiver cadastrado, eh, e ele preencher qual o telefone que ele quer receber notificação pro WhatsApp e automaticamente a gente salvar

**Felipe Martins Costa Brito:** Ô, Emerson,

### 00:36:54

**Emerson Yamamoto:** também no cadastro.

**Felipe Martins Costa Brito:** se for mais fácil, a gente só exibe isso para quem tiver telefone cadastrado.

**Emerson Yamamoto:** É, é, é, com certeza é mais fácil,

**Felipe Martins Costa Brito:** Faz assim.

**Emerson Yamamoto:** porque aí com certeza ele tem telefone cadastrado. Ou pode até ser assim aquela regra de começando com nove ou que tem indicação do WhatsApp, os dois é melhor, porque para fazer do outro jeito vai ser bem mais complicado porque entende que eu preciso salvar e depois enviar. Tipo assim, esse fluxo vai ficar meio complicado se eu tiver que ir lá para meus dados ou então vou ter que trazer para cá. Enfim,

**Felipe Martins Costa Brito:** a gente parte do do pressuposto que a pessoa que se cadastrou no web e não informou o telefone é porque não quer. Então a gente não vai perguntar isso para ela e quem informou a gente pode olha a gente tem também essa ferramenta de e manda

**Emerson Yamamoto:** tá? Então beleza. Então assim fica mais fácil. Mas ainda assim assim, eu acho complicado fazer isso como refinamento, porque o envio pro WhatsApp é outra outra lógica assim, é outro fluxo, tem questão de template, tem outras questões que são mais complicadas, tá?

### 00:37:57

**Emerson Yamamoto:** Al entrou. Ah, não, eu tinha ouvido uma voz, foi mal. Eh, bom, deixa eu anotar isso aqui. Eh, mostrar as paradas.

**Gustavo Pinto:** A gente tenta conversar com Talita hoje ainda no final do mais final do dia pra gente entender melhor o que que tava por trás disso e depois a gente atualiza vocês, tá?

**Felipe Martins Costa Brito:** Mas da sorte, Taiana, já anota aí essas duas necessidades.

**Thaiana Lima:** Tá anotado. Так. Yeah.

**Felipe Martins Costa Brito:** Show. Obrigado.

**Emerson Yamamoto:** Show. Então, beleza, anotei aqui pra gente exibir esse aviso apenas para quem tenha telefone cadastrado com WhatsApp ou telefones celular, né, que comecem com nove. A gente vai deixar mais, mais flexível nesse ponto. Show. Então vamos lá, Marcos. Acho que falta mais uma, né?

**Marcos Benigno:** Isso. OK. Agora eu vou apresentar iso eh 10488, que tem título Alterar encaminhamento presencial para destacar a observação de endereço dos órgãos. Eh, basicamente, eh, ao realizar um encaminhamento, eh, se o endereço tiver uma uma observação, eh, essa observação tem que tá em destaque com estilo diferente.

### 00:39:37

**Emerson Yamamoto:** Так.

**Marcos Benigno:** Eh, nós optamos pelo negrito, conforme foi indicado aqui na na ISO, e também eh caso o órgão seja eh de justiça itinerante, deve ser eh adicionado também mais essa mensagem antes da da observa dessa observação do endereço, que é atenção ônibus da justiça itinerante estará no endereço nas seguintes datas e depois vem a observação. Bom, eh vou mostrar aqui para vocês. OK.

**Emerson Yamamoto:** Так.

**Marcos Benigno:** buscar o atendimento presencial. E aqui logo abaixo do endereço aparece a observação. Eh, nesse caso aqui, nós já colocamos a a indicação do órgão de justiça itinerante para mostrar e logo abaixo vem essa observação do imóvel, teste observação imóvel, que seria a observação do imóvel. E ficaria mais ou menos assim negrito e com a fonte um pouquinho maior

**Felipe Martins Costa Brito:** Ô Marcos, essa informação, essa frase, ela vem da onde?

**Emerson Yamamoto:** Então, Felipe,

**Marcos Benigno:** Kom.

**Emerson Yamamoto:** deixa eu só explicar aqui. Tem tem uma tem essa questão que é o seguinte. Eu até peguei em produção aqui os os exemplos de de órgãos de justiça itinerante, como é que eles estão.

### 00:41:09

**Emerson Yamamoto:** Eh, por exemplo, tem aqui eh DP junto à justiça itinerante de Nova Cepetiba, o aí tá a praça do skate. Mas isso tá no complemento e não na observação. A mesma coisa itinerante de Rio das Pedras.

**Felipe Martins Costa Brito:** Na observação do SI as datas.

**Emerson Yamamoto:** Aí aparece então na observação aqui, nossa, não tem nada, tá nulo.

**Felipe Martins Costa Brito:** Qual é a observação? É, você não tá

**Emerson Yamamoto:** É porque sabe, tem outro campo também que é o informação complementar, que é esse observação para solicitar o agendamento no seu atendimento presencial, distribuição de 20 senhas. Isso é em cada horário,

**Felipe Martins Costa Brito:** sem horário. Não,

**Emerson Yamamoto:** só que geralmente isso pode,

**Felipe Martins Costa Brito:** não. Deixa eu te mostrar. Eu posso mostrar?

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** Mas aí eu vou te mostrar na mesmo,

**Emerson Yamamoto:** Não é isso aí, não tem problema não.

**Felipe Martins Costa Brito:** tá?

**Emerson Yamamoto:** Uhum.

**Felipe Martins Costa Brito:** Deixa só logar aqui Qual é esse

### 00:41:58

**Emerson Yamamoto:** Porque essa Foi uma dúvida que surgiu assim,

**Felipe Martins Costa Brito:** itinerante aí que você mencionou? CPIBA.

**Emerson Yamamoto:** eh, Nova CPA,

**Felipe Martins Costa Brito:** Você viu? Nova CPetiba.

**Emerson Yamamoto:** DP junto à justiça itinerante de Nova CPiba.

**Felipe Martins Costa Brito:** Perí.

**Emerson Yamamoto:** Exatamente. Se quiser pode compartilhar aí.

**Felipe Martins Costa Brito:** Ah, deixa eu só logar aqui que é isso.

**Emerson Yamamoto:** Uhum. He.

**Felipe Martins Costa Brito:** Achei e teria essa observação aqui, ó. Observações de atendimento.

**Emerson Yamamoto:** Não tem isso não, cara.

**Felipe Martins Costa Brito:** Isso. Sabe onde é que isso tem?

**Emerson Yamamoto:** Oi.

**Felipe Martins Costa Brito:** No verde, né?

**Emerson Yamamoto:** Ahã.

**Felipe Martins Costa Brito:** Ela eh, pô, deixa eu logar no verde aqui. Pera aí.

**Emerson Yamamoto:** É, vê no verde aí se isso tem, porque eu olhei,

**Felipe Martins Costa Brito:** Tem no verde tem. fica em cima do do órgão.

**Emerson Yamamoto:** eu olhei em produção e não achei.

**Felipe Martins Costa Brito:** Pera aí, deixa eu ver se eu consigo.

### 00:43:09

**Felipe Martins Costa Brito:** Vou tentar chegar em nova septiva também aqui. Pera aí.

**Thaiana Lima:** A gente tem um campo de observação do órgão.

**Felipe Martins Costa Brito:** É,

**Thaiana Lima:** É fora de endereço.

**Felipe Martins Costa Brito:** é esse,

**Emerson Yamamoto:** Ah, do órgão. Mas aí não é do imóvel,

**Felipe Martins Costa Brito:** é esse,

**Thaiana Lima:** Ah, deve ser isso.

**Emerson Yamamoto:** é do

**Thaiana Lima:** É, eu escrevi do endereço no na ISO mesmo,

**Felipe Martins Costa Brito:** é isso.

**Thaiana Lima:** mas na hora que ele que ele mostrou aqui, eu acho que é do imóvel ou do órgão,

**Emerson Yamamoto:** Ah, então é isso.

**Thaiana Lima:** desculpa, do órgão.

**Felipe Martins Costa Brito:** Óg.

**Emerson Yamamoto:** Óg pode crer.

**Thaiana Lima:** Do órgão.

**Felipe Martins Costa Brito:** Ah, achei, ó.

**Emerson Yamamoto:** Isso é do órgão mesmo.

**Felipe Martins Costa Brito:** Aqui. Opa. Foi, foi aqui, ó.

**Emerson Yamamoto:** Isso aí.

**Thaiana Lima:** Dogo. Isso nem é exibido hoje no app,

**Emerson Yamamoto:** Oi. Nem é exibido hoje.

**Thaiana Lima:** né?

**Emerson Yamamoto:** Exatamente,

**Thaiana Lima:** É,

### 00:43:44

**Emerson Yamamoto:** Felipe.

**Thaiana Lima:** é verdade.

**Emerson Yamamoto:** A gente nem traz isso. Mas isso é para trazer só se foi itinerante ou para qualquer.

**Felipe Martins Costa Brito:** Não, só para itinerante.

**Emerson Yamamoto:** Entendi. Eh, aí a gente não tava com esse conhecimento aqui na IS, não. A gente vai ter que fazer um, posso tentar botar isso como refinamento de trazer esse campo, mas não sei o quão complicado vai ser, que é o campo do órgão, não do endereço, né? E é só se for itinerante. Inclusive tem que ver como é que isso aí vai ficar no app. É muita coisa, né? Um texto bem bem longo. Vai ser meio chatinho de de exibir isso aí. Bonito. Fala de

**Leonardo de Melo:** Eh, acho que é possível sim. até ver aqui qual campanha é possível colocar,

**Emerson Yamamoto:** Uhum.

**Leonardo de Melo:** mas onde fiquei com dúvida é se não for justiça itinerantes, eh tem o critério, o primeiro critério, né, que diz que é para a observação do endereço deve receber destaque.

### 00:44:39

**Leonardo de Melo:** Eh, então isso vale só quando a justiça itinerante mesmo ou tem uma outra observação para receber esse destaque?

**Felipe Martins Costa Brito:** Onde tá esse destaque?

**Emerson Yamamoto:** É aquele atenção ânimo da justiça itinerante, teste observação imóvel. É porque ali tá manual.

**Felipe Martins Costa Brito:** Ah, então é só mesmo.

**Leonardo de Melo:** Ah,

**Emerson Yamamoto:** Então, se for órgão normal,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** não precisa de destaque negrito.

**Felipe Martins Costa Brito:** não.

**Leonardo de Melo:** Beleza.

**Felipe Martins Costa Brito:** O que está chamando de destaque é essa frase, né? Atenção,

**Emerson Yamamoto:** Não, não,

**Felipe Martins Costa Brito:** o ônibus,

**Emerson Yamamoto:** não, não é o negrito. É porque, por exemplo,

**Felipe Martins Costa Brito:** o negrito.

**Emerson Yamamoto:** o T,

**Felipe Martins Costa Brito:** Ah, tá, tá. Não, beleza.

**Emerson Yamamoto:** entendeu?

**Felipe Martins Costa Brito:** Pode manter só no justiç itinerante que essa frase só vai aparecer na justiça itinerante.

**Emerson Yamamoto:** Então,

**Thaiana Lima:** Espera aí,

**Emerson Yamamoto:** mas é porque é fala aí, Tana.

**Thaiana Lima:** desculpa. Eh, essa frase, atenção, a gente colocou só pr justiça itinerante, mas o negrito ele vale o próprio texto da observação do endereço.

### 00:45:24

**Thaiana Lima:** E a observação do endereço tem vários órgãos.

**Felipe Martins Costa Brito:** Mas a observação do endereço na Sci,

**Emerson Yamamoto:** Boa pergunta, porque pelo menos no nos de itinerantes que eu vi aqui, nenhum deles tem preenchido a observação.

**Felipe Martins Costa Brito:** exatamente que eu não preencho. Se se for essa aqui que eu tô Ah, desculpa. Deixa eu mostrar aqui rapidinho de novo. Se for essa esse campo aqui, ele vai tá vazio em todos.

**Emerson Yamamoto:** É esse aí. É isso aí.

**Felipe Martins Costa Brito:** Tá vazio em todos.

**Emerson Yamamoto:** Por isso que eu tô falando, eu olhei no banco também e quase nenhum preenche isso. Até tem uns que tm preenchido. Posso até buscar aqui depois.

**Felipe Martins Costa Brito:** Não, mas mas deve ser assim desativado que que aí não é não é para finalidade de atendimento.

**Emerson Yamamoto:** Uhum.

**Felipe Martins Costa Brito:** Então esse campo de observação a gente não usa para para fing de atendimento.

**Thaiana Lima:** A gente sempre exibe, né, no app e na e na CRC.

### 00:46:17

**Thaiana Lima:** Exibe assim, existe o campo, ele vai tá vazio, tudo bem, mas era era padrão sempre ficava na tela.

**Emerson Yamamoto:** Pior que eu acho que nem exibita porque o o principal é a observação do horário, né, que é sempre a mesma, mas geralmente tem informações mais relevantes. Eu nem exibe, mas não tem nada, né? Nunca aparece. Acho que é isso que eu quero dizer. Fala, Léo.

**Leonardo de Melo:** Eh, eu mudei aqui via banco e essa observação imóvel para um outro de justiça itinerante que tem aqui no banco. Aí se puder fazer a busca novamente, mano, só pra gente ver como é que vai ficar,

**Marcos Benigno:** Sì.

**Leonardo de Melo:** que eu acho que vai ficar bem bem grande mesmo.

**Emerson Yamamoto:** Vai, vai ficar muito grande, vai ficar estranho. É muito, muito longo esse texto. É, até que não, hein. Até que até que eu achei que ia ficar pior, sinceramente.

**Felipe Martins Costa Brito:** Tá ruim não, hein? Yeah.

**Emerson Yamamoto:** É, achei que ia ficar pior também. Tá bom.

### 00:47:24

**Emerson Yamamoto:** Se for assim. Agora,

**Leonardo de Melo:** Eh

**Emerson Yamamoto:** engraçado que tem o atende apenas nos dias e ali tem nas seguintes datas, né? Mas tá bom. Ficou, ficou redundante, mas não sei se tem como resolver isso.

**Felipe Martins Costa Brito:** Cadê na que datas? Onde é que tá datas? Que eu não tô achando apenas no

**Emerson Yamamoto:** É as datas de baixo que estão ali, atende apenas nos dias, tal, tal, tal, tal.

**Felipe Martins Costa Brito:** gestal. Onde é que você viu a outra data?

**Emerson Yamamoto:** Em cima, atenção, o ônibus da justiça itinerante estará nos endereços nas seguintes datas. Dois pontos. Atende apenas nos dias.

**Felipe Martins Costa Brito:** Ah, mas aí atende apenas nos dias eu tiro,

**Emerson Yamamoto:** Dois pontos. É, entendi.

**Felipe Martins Costa Brito:** aí eu removo do SI,

**Emerson Yamamoto:** Pode ser.

**Felipe Martins Costa Brito:** porque vai ter isso.

**Emerson Yamamoto:** É,

**Felipe Martins Costa Brito:** Se bem que eu não posso tirar desse porque essa frase vai exatamente então eh vai ficar

### 00:48:02

**Emerson Yamamoto:** mas vai ter isso no app. Exatamente. No CRC não, né?

**Felipe Martins Costa Brito:** então vai ficar quanto mais informação melhor.

**Emerson Yamamoto:** Depois a gente pode pensar numa frase que não fique tão redundante assim. Sei lá, o ônibus itinerante estará no endereço apenas em dias específicos. Atende apenas nos dias, tal, tal, tal, tal. que aí pelo menos não tem dois dois pontos, né? Fica estranho.

**Felipe Martins Costa Brito:** Beleza. Так.

**Emerson Yamamoto:** Pode botar pelo menos para não ficar tão redundante assim, porque parece erro. Mas beleza, a gente faz esse ajuste. Eh, botei aqui então, Leonardo,incluir observação do órgão. Se o órgão for de justiça itinerante, eu botar aqui ajustar texto fixo. Beleza? Então, para órgão, eu vou até anotar aqui que para órgãos que não são de justiça itinerante não destaque. Aí até a gente vai comentar na IS, porque o item um dá a entender que precisaria, né? A observação do endereço do órgão deverá receber destaque e aí só o item dois que fala de itinerante, tá?

### 00:49:27

**Emerson Yamamoto:** Beleza? Acho que acho que é isso. Acho que a gente fechou, né, Marcos?

**Marcos Benigno:** pessoal. É isso. Obrigado,

**Emerson Yamamoto:** Obrigado, Marcos. Vamos passar agora pro Leonardo. Leonardo de Melo vai apresentar a parte aí do órgão colegiado.

**Felipe Martins Costa Brito:** É, é, é, é minha ainda ou tá liberado?

**Emerson Yamamoto:** Eh, eu acho que não, né, Felipe? É do app, né? É questão de encaminhamento processual.

**Felipe Martins Costa Brito:** Ah, então tá. Então,

**Emerson Yamamoto:** Acho que acho que vale a pena,

**Felipe Martins Costa Brito:** beleza,

**Emerson Yamamoto:** sim.

**Diogo Leite Mesquita:** Todas suas Felipe.

**Felipe Martins Costa Brito:** muito obrigado, seu Diogo.

**Leonardo de Melo:** Eh, boa tarde. apresentar aqui agora. Só colocar aqui. Não aparece seu tch. Eh, acho que eu peguei é essa de alterar encaminhamento processual utilizando o órgão colegiado para mapeamento de atendimento no PROEC 2G. Eh, então a consulta de processo de origem PROC de segunda instância tem que armazenar o nome e o código enviado do como órgão colegiado nos encaminhamentos processuais.

### 00:50:35

**Leonardo de Melo:** dessa desse tipo de origem deve obter o órgão a partir do órgão colegiado em vez do órgão julgador e a exibição do dos dados

**Emerson Yamamoto:** Ja.

**Leonardo de Melo:** tem que ir de acordo, né? Então a gente pega os órgãos DPGE a partir do órgão TJ, que é esse órgão colegiado aqui. Então eu tô aqui com esse assistido aqui, o Anísio. Eh, tem esse caso aqui que tá com esse processo de PROC 2G de segunda instância. Vou mostrar aqui primeiro. No caso, o caso tá aqui com primeira DP são período da aldeia. E se a gente for vir aqui no ver aqui pelo banco qual órgão TJ, eh aqui a gente tem esse campo aqui, FK, órgão colegiado TJ, que tá aqui com esse órgão aqui, o terceira câmara de direito público, que é exatamente esse daqui, o órgão colegiado desse processo. E aí esse órgão TJ, ele tem como eh órgão DPG associado esse órgão aqui, 10 DP de defesa da criança e do adolescente e esse outro que é o que tá aqui no caso, primeiro EDP de São Pedro da Aldeia, tá?

### 00:51:55

**Leonardo de Melo:** Daí o que eu vou fazer aqui, eu vou tirar esse campo aqui como preenchido, colocar aqui ele como no pra gente poder ver que quando eu buscar esse processo, ele vai ser preenchido novamente com o órgão que estava anteriormente, tá? Então vou fazer aqui no app a busca por esse processo. A gente vai poder ver esse campo sendo preenchido. Aqui ele fez a fez a busca, apareceu aqui o órgão responsável primeira DP de São Pedro da Aldeia. E se a gente for atualizar aqui a busca, a gente pode ver que ele atualizou de acordo, né? Então, terceira câmara de direito público e ele tá seguindo o mapeamento, né? Então, como esse órgão DJ tá ligado com o órgão DPG, primeira DP são pror da aldeia, ele pegou aqui corretamente. Como a gente tem esse caso associado, eh, se a gente tirar esse esse órgão do mapeamento, então vou tirar essa linha aqui, o que ele vai fazer agora é que ele vai pegar um outro órgão associado a esse caso.

### 00:53:12

**Leonardo de Melo:** Então aqui é o núcleo de Caxias. Se a gente fizer essa busca novamente, ele vai aparecer esse órgão em vez do da primeira DP. N aqui núcleo de primeiro atendimento cível de núcleo de Caxias. Vou até prosseguir aqui com o atendimento. A gente vai ver que aparece corretamente. Não deveria. Aqui também ele atualiza o núcleo de primeiro atendimento cível de Caxias, tá? Então acredito que seja isso nessa ISO. Se tiver alguma dúvida ou fluxo para testar.

**Felipe Martins Costa Brito:** Não, não tenho não. Só queria saber o seguinte,

**Emerson Yamamoto:** Show

**Felipe Martins Costa Brito:** a gente já previu isso paraas outras frentes também.

**Thaiana Lima:** Desculpa, o uso do colegiado já tá tá relacionado embaixo,

**Felipe Martins Costa Brito:** Essa mesmo.

**Emerson Yamamoto:** no verde já

**Thaiana Lima:** ó, na integra e no verde.

**Felipe Martins Costa Brito:** Perfeito. Não, beleza. Beleza. Era só para confirmar isso. Valeu,

### 00:54:20

**Thaiana Lima:** Sim. No.

**Leonardo de Melo:** Beleza? Então é isso. Essas foram as do app.

**Emerson Yamamoto:** Boa. Eh, bom, Felipe, agora deixa eu ver o que tem aqui.

**Felipe Martins Costa Brito:** Não tem que ver se o Diogo me deixa sair.

**Emerson Yamamoto:** Tem a questão do da Integra, tem a questão de consulta de órgão de atendimento processual, considerando órgão colegiado.

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** Essa mesma é

**Felipe Martins Costa Brito:** mas que aí vocês mostram lá naquela telinha de API. Só fico aqui olhando.

**Emerson Yamamoto:** sim. Aí, Diogão, que tá com a palavra aí, Diogão, tá liberado.

**Felipe Martins Costa Brito:** É,

**Diogo Leite Mesquita:** Eu acho que sim. Qualquer coisa a gente chama novo.

**Felipe Martins Costa Brito:** então você tão você você é tão gentil. Tá bom,

**Emerson Yamamoto:** Tem que ver paraa abertura,

**Felipe Martins Costa Brito:** então.

**Emerson Yamamoto:** né, Felipe? Se você vai voltar,

**Felipe Martins Costa Brito:** Ah, qualquer coisa o Diogo me chama. Ah,

**Emerson Yamamoto:** tá?

### 00:55:05

**Felipe Martins Costa Brito:** Tita tá aí.

**Talita Ribeiro:** Oi, entrei aqui, tava falando com Taiana, aí ela comentou sobre aquela questão lá do da do atendimento, né, do agendamento, poder receber as informações também pelo WhatsApp, né?

**Felipe Martins Costa Brito:** Iso.

**Talita Ribeiro:** Aí, Felipe, a a minha ideia, na verdade, a minha ideia inicial era fazer isso via rotina, mas aí eu conversando aqui com Taiana, acabei achando. E aí você me diz o que que fica melhor, porque assim, o que que a minha ideia inicial era era a gente varrer esses esses agendamentos que têm necessidade de informação também via WhatsApp, identificar aqueles que querem ser receber os dados do do WhatsApp, a gente pegar o pré-atendimento referente a ele e mandar pelo WhatsApp via que eu

**Felipe Martins Costa Brito:** Então, a gente tá falando a mesma coisa.

**Talita Ribeiro:** tô nesse Ah,

**Felipe Martins Costa Brito:** Por quê? Porque na na na mensagem de sucesso do agendamento já vai o link do

**Talita Ribeiro:** tá. Acho. É, só quer que eu vou apresentar porque vai ser um dia que eu vou tomar.

### 00:55:57

**Felipe Martins Costa Brito:** pré-atendimento.

**Talita Ribeiro:** Tô no pré-atendimento aí. Aí, aqui já tá indo no app.

**Felipe Martins Costa Brito:** Uhum.

**Emerson Yamamoto:** Não, não, no app não. M.

**Felipe Martins Costa Brito:** Não, não é não,

**Talita Ribeiro:** Não,

**Felipe Martins Costa Brito:** mas é para ir, entendeu?

**Talita Ribeiro:** aqui, aqui você quer também que já tenhaum.

**Felipe Martins Costa Brito:** Já que hoje, por exemplo, se a pessoa se hoje no WhatsApp, se a pessoa se agenda pelo WhatsApp, ela recebe mensagem de confirmação e vem o link do do pré-atendimento.

**Talita Ribeiro:** É.

**Felipe Martins Costa Brito:** É pra gente replicar aí também aí no app e também no verde pro agendamento do 29.

**Talita Ribeiro:** É, mas assim, eu lembro da gente ter conversado sobre isso e não vai ficar, você não acha que vai ficar estranho a gente aqui no no sucesso dela pedir para ela inserir os documentos em outro lugar, sendo que ela vai receber uma notificação para subir os documentos aqui também referente à aquele agendamento?

**Felipe Martins Costa Brito:** Mas aí a gente não ia tomar a decisão de de manter num só canal.

### 00:56:52

**Talita Ribeiro:** Então a gente vai ter que conversar então sobre isso, porque na minha concepção a gente, eu lembro que a gente t não vamos pedir dos dois, mas não ao mesmo não no mesmo momento, não no mesmo contexto, né? Na minha cabeça, a nossa decisão foi o seguinte: a gente não vai mantendo o mesmo contexto para não confundir. E aí se a gente vê que a pessoa tá inserindo pelos dois caminhos, a gente tira de um dos lados.

**Felipe Martins Costa Brito:** que eu achei que os dois caminhos eles iam num determinado momento.

**Talita Ribeiro:** Mas eles estão convergindo pra mesma tela,

**Felipe Martins Costa Brito:** É.

**Talita Ribeiro:** mas aí a gente vai acabar tendo que fazer eh a gente não desconectou nada. Então assim, imagina que a pessoa vai ser ped solicitada para enviar documentos pelos dois caminhos. Será que faz sentido?

**Felipe Martins Costa Brito:** Não, me dera desabilitar um, né?

**Talita Ribeiro:** E qual seria? Porque um ela ela pode um ela pode utilizar os dados.

**Felipe Martins Costa Brito:** E por onde ela começou? Se ela começou pelo app, não vamos no chamar no WhatsApp.

### 00:57:46

**Felipe Martins Costa Brito:** Se ela começou no WhatsApp, não vamos chamar no app.

**Talita Ribeiro:** Hum. Mas aí então não,

**Felipe Martins Costa Brito:** Não,

**Talita Ribeiro:** mas nesses casos aqui ela fez no WhatsApp, ela fez no app, então não seria nem pra gente mandar nada no WhatsApp,

**Felipe Martins Costa Brito:** mas a questão do WhatsApp é é para ele receber. Vamos tira um pouco o link do pretendimento.

**Talita Ribeiro:** tá?

**Felipe Martins Costa Brito:** O que eu tinha pensado era ele rece por quê? Porque eles alegam que a maioria das pessoas que faltam ao agendamento alegam que esqueceram a data. Então era ele ter essa data no WhatsApp dele.

**Talita Ribeiro:** Ah\!

**Felipe Martins Costa Brito:** Então ele teria ali a data e a maioria das pessoas alega que não consultou a lista de documentos, ele teria lista de documentos no WhatsApp dele.

**Talita Ribeiro:** Então, a gente vai criar um outro fluxo para esses casos.

**Felipe Martins Costa Brito:** Isso, isso seria esse esse caso. Outra questão que surgiu na reunião, eu não sei, se você tinha pensado nisso, era que toda notificação que a gente fizesse pelo pelo por exemplo, chegou uma mensagem para você e notificá-lo também por WhatsApp.

### 00:58:42

**Felipe Martins Costa Brito:** Você tinha pensado nisso?

**Talita Ribeiro:** Sim. Tanto é que, na verdade, quem a gente tinha pensado junto com o próprio Emerson que falou assim, ao invés da gente deixar isso e específico para falar só sobre a confirmação de agendamentos e sobre o

**Felipe Martins Costa Brito:** Hum.

**Talita Ribeiro:** envio de a gente falava assim: "Não, eu quero receber informações genéricas sobre esse agendamento".

**Felipe Martins Costa Brito:** Beleza.

**Talita Ribeiro:** E aí a gente pode usar para para como,

**Felipe Martins Costa Brito:** Então é um outro.

**Talita Ribeiro:** mas eu acho que vale a pena a gente sentar e eu tenho até que falar sobre outras coisas contigo.

**Felipe Martins Costa Brito:** Tá.

**Talita Ribeiro:** A gente pode marcar uma reunião talvez amanhã pra gente desenhar esse fluxo, como a gente quer usar essa informação,

**Felipe Martins Costa Brito:** Tá bom. Beleza.

**Talita Ribeiro:** porque eu tô entendendo então que não é nem não é nem como a gente tinha pensado que é pedindo documento dos dois lados,

**Felipe Martins Costa Brito:** Aquela aquela primeira reunião que a gente teve,

**Talita Ribeiro:** né?

**Felipe Martins Costa Brito:** que foi sobre o o comque sobre o crédit,

### 00:59:22

**Talita Ribeiro:** com a

**Felipe Martins Costa Brito:** que é o o que tá acontecendo agora,

**Talita Ribeiro:** can

**Felipe Martins Costa Brito:** já se desenhou um fluxo totalmente diferente. Então a gente nem tá mais utilizando, pelo menos não daquela conversa inicial para atendimento daquele formato que a gente pensou. Isso foi, já tá descartado, tá sendo feito de outra forma, entendeu?

**Talita Ribeiro:** Uhum. Bom,

**Felipe Martins Costa Brito:** Então acho que as coisas mudaram e aí assim a gente pode atual aproveitar o que já tá construído e ter três ou quatro saídas, entendeu? Mas aí a gente conversa depois,

**Talita Ribeiro:** tá, você se se você quiser,

**Felipe Martins Costa Brito:** então não,

**Talita Ribeiro:** eu posso amanhã na na segunda de tarde. Pode ir.

**Felipe Martins Costa Brito:** amanhã tem, eu ten de manhã eu tenho uma reunião de tarde. Deixa só ver aqui rapidinho. Eu acho que amanhã de tarde eu tô livre. de manhã. Eu tenho certeza que eu tenho M.

### 01:00:03

**Talita Ribeiro:** É,

**Thaiana Lima:** Tá ali,

**Talita Ribeiro:** amanhã eu tenho,

**Thaiana Lima:** tá?

**Talita Ribeiro:** eu tenho uma reunião de 2 horas, mas depois acho que por volta de 4 eu vou estar livre.

**Thaiana Lima:** Mas vê essa questão de vê essa questão da do armazenamento,

**Talita Ribeiro:** Oi.

**Thaiana Lima:** porque que Felipe falou de mensagem, você falou de forma mais genérica, mas a IS fala sobre aquele agendamento. Então os meninos guardaram a preferência no evento.

**Talita Ribeiro:** Mas tá certo, é isso mesmo. É pro evento.

**Thaiana Lima:** Então,

**Talita Ribeiro:** Só que é,

**Thaiana Lima:** mas você falou de forma genérica e o Felipe deu exemplo da mensagem. Nada disso relacionado ao evento.

**Talita Ribeiro:** mas é sobre aquele agendamento.

**Felipe Martins Costa Brito:** É porque mas aí se for mensagem de CP não tá relacionado a aquele

**Thaiana Lima:** Não tá relacionado aindamento.

**Felipe Martins Costa Brito:** evento. É.

**Talita Ribeiro:** Mas a gente não Como assim mensagem de CP?

**Thaiana Lima:** Mensagem. Mensagem que você manda no caso chat.

**Talita Ribeiro:** A, mas eu tenho como recuperar o caso do agendamento.

### 01:00:50

**Felipe Martins Costa Brito:** Não, porque nem todo CP veio de agendamento.

**Talita Ribeiro:** Ah, tá. É, aí não tem. Mas aí é o nosso o nosso inicial, quando eu falei genérico, era genérico referente a informações de um agendamento, não de qualquer CP, porque aí aí eu não sei como é que a gente colocaria isso. Essa informação teria que ser em outro local, talvez na hora que ele faz o cadastro no aplicativo,

**Felipe Martins Costa Brito:** É,

**Talita Ribeiro:** não sei.

**Felipe Martins Costa Brito:** pode ser. Bom, vem. Bom, amanhã quatro eu posta, mas eu tenho que ver se se se alguém do do da DGD vai participar.

**Talita Ribeiro:** da aí o

**Felipe Martins Costa Brito:** E segunda de tarde para mim também tá tranquilo.

**Talita Ribeiro:** Diogo, você pode quem é que poderia ver é eu vou mandar lá no grupo de reuniões pra gente fechar então

**Felipe Martins Costa Brito:** Tá, tem um grupo só para tratar de reuniões.

**Talita Ribeiro:** essa data é um grupo para para

**Felipe Martins Costa Brito:** Isso mesmo.

**Diogo Leite Mesquita:** Vou te colocar nele.

### 01:01:38

**Talita Ribeiro:** agendar reuniões,

**Felipe Martins Costa Brito:** Não precisa não.

**Talita Ribeiro:** tá?

**Felipe Martins Costa Brito:** Pedro, muito obrigado.

**Yann Naylor Francisco:** marcar reunião é difícil, Felipe,

**Felipe Martins Costa Brito:** Eu é mais difícil do que fazer a reunião,

**Yann Naylor Francisco:** justamente.

**Talita Ribeiro:** Tá aí a gente fecha esses pontos.

**Felipe Martins Costa Brito:** combinado? Combinado. Combinado.

**Emerson Yamamoto:** Mas só uma dúvida, Felipe. Então não tivemos decisão, né,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** por enquanto.

**Felipe Martins Costa Brito:** a gente vai aproveitar isso, só que vão ter, vamos ter que fazer algumas outras issos para aproveitar a isso, entendeu?

**Emerson Yamamoto:** Então, mas por exemplo, o envio, que seria ali na hora com o mesmo resumo do atendimento que ele acabou de receber,

**Felipe Martins Costa Brito:** Vai rolar,

**Emerson Yamamoto:** vai rolar também,

**Felipe Martins Costa Brito:** vai rolar.

**Emerson Yamamoto:** tá? Beleza, então

**Felipe Martins Costa Brito:** Então tá. Se precisar de mim, Diogo, para abertura, me chama. Valeu, gente.

**Diogo Leite Mesquita:** Tá, faltam muitas eixos aí. Como é que tá?

### 01:02:25

**Emerson Yamamoto:** um pouco, mas agora integra, acredito que seja mais rápido.

**Diogo Leite Mesquita:** Beleza,

**Emerson Yamamoto:** Faltam cinco.

**Diogo Leite Mesquita:** Felipe fugiu. Pode seguir.

**Talita Ribeiro:** Emerson, rapidinho. Isso que você acabou de falar pro Felipe, eh, tá entrando como refinamento ou naixo?

**Emerson Yamamoto:** Não, eu falei para ele que não tem como entrar como refinamento um envio para um WhatsApp porque é outro o

**Talita Ribeiro:** Não, beleza, beleza. Só para eu entender o que foi que você tinha acordado com ele,

**Emerson Yamamoto:** fluxo,

**Talita Ribeiro:** porque eu também na minha cabeça seria uma um novo fluxo, não? Só para eu saber também como eu vou falar isso com ele.

**Emerson Yamamoto:** tá? É porque ele falou que a ideia inicial dele era essa. Aí eu falei: "Pô, mas isso não tá escrito na IS de forma alguma, Felipe, não tem como". Mí. ele. Ah, não. Beleza. Vou ver com a Talita.

**Talita Ribeiro:** É, pois é. Não, não era nem isso, né? Não era, era, era.

### 01:03:06

**Emerson Yamamoto:** Sim, era armazenar mesmo,

**Talita Ribeiro:** Tanto é que aí,

**Emerson Yamamoto:** né? Sim.

**Talita Ribeiro:** tanto é que a ISO era para solicitar a confirmação do agendamento via WhatsApp. Lembra que era mais específico?

**Emerson Yamamoto:** Uhum.

**Talita Ribeiro:** foi quem trouxe a ideia para ser genérica no sentido de informações gerais sobre aquele agendamento foi você.

**Emerson Yamamoto:** Eu nem lembro. Mas que bom. Gostei da minha ideia.

**Talita Ribeiro:** É só que aí agora o Felipe gostou também da tua ideia e pensou alguma coisa além que tipo,

**Emerson Yamamoto:** Sim.

**Talita Ribeiro:** entendeu? Eu não teria como isso ter surgido naquela conversa,

**Emerson Yamamoto:** Uhum.

**Talita Ribeiro:** sendo que quem deu essa ideia foi você e não ele.

**Emerson Yamamoto:** Sim, sim. Tranquilo. Beleza. Obrigado. Eh, Alexandre, né?

**Alexandre Donnelly Vaz:** Isso sou eu.

**Emerson Yamamoto:** Bora lá, Alexandre.

**Alexandre Donnelly Vaz:** Bora. A primeira iso que eu vou apresentar é de alterar a consulta de casos de uma pessoa para verificar mapeamento entre assunto verde e assunto CNJ. Agora a gente tá podendo vincular pelo verde eh essa relação de assunto verde com o assunto CNJ, né?

### 01:04:12

**Alexandre Donnelly Vaz:** assunto unificado. Então, eu tenho um exemplo aqui de um assunto verde teste associado a alguns assuntos de CNJ, entre eles o abandono de função. Vou vir aqui na consulta de caso pessoa tem esse essa pessoa aqui. Ela tem dois casos. Um é não processual aqui, o outro é processual. Esse de caso, esse caso processual tem o assunto abandono de função, que é um dos assuntos eh judiciais que estão associados a esse assunto teste, né? Se eu filtrar pelo assunto processual dele, retorna apenas esse caso, cujo o assunto é abandono de função. A novidade dessa iso é que agora também, se eu filtrar pelo assunto verde relacionado a a esse assunto processual também vai funcionar. E por último, só vou mostrar que não quebrou a esse filtro de assunto do verde para quando eu realmente quero buscar Yeah. um diretamente por um assunto do verde. Se eu filtrar aqui por esse assunto verde aqui, preso flagrante ou provisório, vai retornar apenas esse primeiro caso que retornou um caso.

### 01:06:17

**Emerson Yamamoto:** É porque tu não filtrou ali por CNP,

**Alexandre Donnelly Vaz:** Não,

**Emerson Yamamoto:** tu botou só.

**Alexandre Donnelly Vaz:** mas tá certo.

**Emerson Yamamoto:** Tá certo. Ah, tá.

**Alexandre Donnelly Vaz:** Tá certo. pelo caso que eu queria.

**Emerson Yamamoto:** Ah,

**Alexandre Donnelly Vaz:** O caso é um caso com uma foto verde.

**Emerson Yamamoto:** tá, entendi. Uhum.

**Alexandre Donnelly Vaz:** Eh,

**Emerson Yamamoto:** Mas nesse caso aí ele teria que trazer também os que t o assunto CNJ associado a esse assunto aí, não é?

**Alexandre Donnelly Vaz:** não, mas é só que não tem não tem.

**Emerson Yamamoto:** Ah, tá, entendi. Não tem. Saquei.

**Alexandre Donnelly Vaz:** Eu mostrei só para para mostrar o caso no qual eu quero filtrar diretamente pelo assunto do verde mesmo.

**Emerson Yamamoto:** Entendi. Entendi.

**Alexandre Donnelly Vaz:** O outro o outro caso era o que eu mostrei 8472, que é o teste, o assunto teste, ele retorna caso com o assunto processual.

**Emerson Yamamoto:** Ah, legal. Uhum.

**Alexandre Donnelly Vaz:** A gente fez algumas outras mudanças para para ess porque eu antes havia apenas um filtro um parâmetro de assunto, agora tem dois.

### 01:07:22

**Alexandre Donnelly Vaz:** Eh, não sei se vale a pena passar por tudo, mas tá tudo descrito aqui na documentação. No.

**Emerson Yamamoto:** É, porque só para explicar bem rapidamente, né? Antes o tipo caso era era o que definia qual valor ia ter no ID assunto, o que é meio estranho, né? porque ficava um campo meio que multivalorado. O ID assunto poderia ser um ID assunto verde, mas poderia ser um ID assunto eh CNJ. E agora, como a gente realmente precisa retornar os dois, por exemplo, se a gente colocar um ID assunto verde que tenha a ideia assunto CNJ relacionado, aí fica mais estranho ainda. Então a gente preferiu criar um novo campo, que é o ID assunto processo para dessa forma ter campos eh definitivos ali, dedicados a cada um dos assuntos e usar o tipo caso realmente como um filtro. Se eu quiser ver todos os casos, eu deixo sem nada. Se eu quiser ver só CP, eu filtro só CP. Se eu quiser ver só CNP, eu filtro só CNP. E aí ele faz essa busca de uma forma bem mais genérica e modularizada.

### 01:08:23

**Emerson Yamamoto:** Então, dessa forma ficou bem mais organizada do que era antes, que era até um pouco difícil de entender como é que funcionava esse filtro. Talvez a APItenha que se ajustar a isso, porque de fato antes a gente só usava o ID assunto, mas de é só um campo a mais e de resto é só saber como usar o filtro ali mesmo. Então é uma mudança pequena.

**Alexandre Donnelly Vaz:** Sim.

**Emerson Yamamoto:** Beleza, pessoal, deu para entender? Então, fechou a apresentação, Alexandre?

**Alexandre Donnelly Vaz:** dessa eh

**Emerson Yamamoto:** Sim, sim. Beleza, pode seguir.

**Alexandre Donnelly Vaz:** A outras duas issos que eu tenho são o fluxo de atendimento processual em busca de órgãos. Então, eh, juntei tudo em um processo mesmo. Deixa eu consultar aqui agora ele me retorna à observação, então é bem parecida com o que o Leonardoou Marcos mostraram mais cedo para órgãos cuj endereço tem endereços de cujo órgão tem eh o tipo justiça itinerante, né? Então aqui é observação, atenção, ônibus da justiça itinerante estará no endereço nas seguintes datas.

### 01:09:44

**Alexandre Donnelly Vaz:** Aí eu coloquei uma observação, um teste aqui que vai ficar em negrito se eu remover. Eh, tem que fazer isso pelo banco.

**Emerson Yamamoto:** Mas só uma coisa, Alexandre, acho que nem precisa porque vai mudar, né? como a gente viu lá na IS, é a observação do órgão. Na verdade, essa observação aí é aquela que você pegou do imóvel, né? Então isso meio que é do órgão.

**Alexandre Donnelly Vaz:** É de órgão,

**Emerson Yamamoto:** É, o Felipe viu que era do órgão, então meio que vai mudar, a gente vai ter que trocar aí mesmo mesmo refinamento que tem lá para eixo deles vai ter aqui também.

**Alexandre Donnelly Vaz:** tá? Mas vai seguir com esse campo aqui no endereço ou vai direto pro órgão?

**Emerson Yamamoto:** Não, não, tudo igual. Só que a observação vai ter o texto. Atenção, o ano da justiça estará no endereço nas seguintes datas, dois pontos e a observação do órgão.

**Alexandre Donnelly Vaz:** Sim.

**Emerson Yamamoto:** Entendeu?

**Alexandre Donnelly Vaz:** Mas aí eu eu digo aqui na estrutura, eu tiro do endereço, coloco direto no órgão,

### 01:10:37

**Emerson Yamamoto:** Não, não, eu acho. É, não sei. Entendi agora que você falou.

**Alexandre Donnelly Vaz:** que pode ter vários endereços também,

**Emerson Yamamoto:** É,

**Alexandre Donnelly Vaz:** melhor.

**Emerson Yamamoto:** entendi, cara. Agora eu não sei, hein, porque essa realmente essa observação ela é genérica do órgão. Você tá falando, talvez trazer para fora, né?

**Alexandre Donnelly Vaz:** Ja.

**Emerson Yamamoto:** Pode ser, pode ser, já que ela é do órgão, né? Pode ser. A gente pode talvez trazer para fora, sim.

**Alexandre Donnelly Vaz:** Aí, se eu tirar esse tipo de justiça itinerante desse órgão, vai mudar o texto, né? Isso vai acontecer mesmo depois de observação. Agora é só observação teste não informa mais o questão do ônibus da justiça itinerante. Isso fecha uma das minhas isos. A última é outra que o Leonardojá apresentou o equivalente pro app, né, que é do órgão colegiado. Então esse processo aqui que eu tô usando, eh, termina em 044, tem um um órgão colegiado. Não tem muito como mostrar isso direto pelo verde, então vou ter que recorrer ao banco.

### 01:11:55

**Alexandre Donnelly Vaz:** Mas eu montei uma consulta que pega o nome do órgão DPGE a partir do órgão colegiado de um processo que é a 10 DP de defesa da criança e do adolescente, né? é o é o órgão de D1 do verde. É isso que tá sendo retornado mesmo. E agora, se eu remover eh o órgão colegiado aqui desse processo, vai ficar colegiado. Eov, já retornou um erro aqui. não foi encontrada uma vara associada a este processo, porque ele tá vendo pelo mapeamento do órgão colegiado. É isso. Não tem mais, não tem mais nada.

**Emerson Yamamoto:** Show.

**Alexandre Donnelly Vaz:** Beleza. Acho que a gente já pode passar pro Fariasse ninguém tiver nenhuma dúvida.

**Emerson Yamamoto:** Eu achei que tu tinha três.

**Alexandre Donnelly Vaz:** Foram três. É que duas são,

**Emerson Yamamoto:** Ah, tá, entendi.

**Alexandre Donnelly Vaz:** uma é de justiça itinerante e outra é do é do órgão coligado.

**Emerson Yamamoto:** Ah, tá.

**Alexandre Donnelly Vaz:** Mostrei, mas as duas são no atendimento processual,

### 01:13:32

**Emerson Yamamoto:** Verdade,

**Alexandre Donnelly Vaz:** então apresentei duas de uma vez

**Emerson Yamamoto:** verdade.

**Alexandre Donnelly Vaz:** só.

**Emerson Yamamoto:** Show. Beleza, valeu. Vou passar então aí pro Farias passar a parte do maria atendimento.

**Lucas Farias:** Boa tarde, pessoal. Eh, então vou começar pela do 10627, que é de receber um status agora vinculado a um pré-atendimento, né, de um agendamento. Agora a gente vai ter um novo end point para receber esse status. E além do status, a gente recebe o ID do agendamento, o ID também do pré-atendimento e a quantidade de documentos enviados, né, que não é obrigatório. Eh, como primeira regra, a gente vai verificar se aquele agendamento está ativo, se ele é pendente ou validado,

**Emerson Yamamoto:** Sì.

**Lucas Farias:** eh, e se existe também, né? Se ele não existir, a gente retorna como é padrão já nas nossas nossas ind points. E dependendo do status dele, a gente também informa a situação. Então eu vou mostrar aqui como é que ficou. A gente criou esse ind point aqui, entrega pré-atendimento status. E aqui eu vou inicialmente passar um um agendamento que não está validado nem pendente, pegar um cancelado aqui qualquer, só pra gente ver que não vai passar, né?

### 01:15:15

**Lucas Farias:** Aqui eu vou ter que botar um valor só para ele não reclamar, um valor válido no status. Aqui ele informa que o agendamento foi cancelado, por isso não é possível retornar. Também a gente tem a validação de tipo de evento, né? Essa não tá descrito na ISO, mas a gente botou uma validação eh para verificar se se é de fato um agendamento da CRC para ele não pegar diversos outros tipos que a gente tem nessa tabela de evento, como audiência, bloqueio. Então vou pegar um aqui que não é CRC, ele também não deixa alterar. A gente também valida o status em si, né? Por isso que eu coloquei esse iniciado aqui. Se eu deixasse string aqui, por exemplo, ele também não deixa salvar porque ele não reconhece esse status. E agora sim vou fazer o envio com sucesso, passando todas as informações, pedidos. Então eu vou pegar aqui um evento que ele ainda não tem um um ID de pré-vendimento salvo e que ele esteja validado ou pendente. Aqui eu vou colocar o status pendente que eu posso colocar maiúscula, minúscula.

### 01:16:55

**Lucas Farias:** Ah, deixa eu pegar um IDqualquer aqui de exemplo e vou colocar dois documentos aqui enviados. Beleza, ele enviou. Aí, agora eu vou mostrar esse esse agendamento aqui. A gente passou a salvar agora no banco esse status que foi enviado ali juntamente com o ID do pré-atendimento passado. E sobre o a quantidade de documentos enviados, a gente salva isso só no log, deixamos para salvar no log, achamos que não faz sentido salvar aqui no evento em si. Então, a gente deixou aqui nesse no log novo que foi criado, eh, que além de todas as informações como o status, o ID do agendamento e o ID do pré-entendimento passado, a gente também salva o número de documentos que foi enviado ali na requisição. Deixa eu voltar aqui na ISO. Ela também diz que se a gente, se já houver algum status registrado, a gente vai atualizar para o novo status. Então, vou pegar esse mesmo exemplo que eu passei e aqui eu vou mudar para iniciado. Vou mudar a quantidade aqui também de documentos. Aí agora se eu recarregar o evento foi status deles foi alterado para iniciado aí que diz também se a relação do agendamento com pré-tendimento não existir registrar o relacionamento que foi o que eu mostrei ali do dele salvar o UID, né?

### 01:19:06

**Lucas Farias:** E aqui foi até uma dúvida que a gente teve também se por acaso eu enviar um outro e o ID aqui, ele vai passar a salvar esse outro. Eu lembro que eu cheguei a comentar com a Talita na época, mas ela disse que era melhor não travar nada pro Farias,pro Maria atendimento. Então, se eles precisarem de alguma alteração nesse sentido, a gente pode fazer depois, mas a princípio a gente não tá travando casos assim. E por último, o log, né, que eu mostrei, que é esse novo log, mostrando as alterações de status que houveram. Aí salvou esses dois que eu enviei por último agora. Beleza, vou passar pro próximo.

**Thaiana Lima:** Falei,

**Lucas Farias:** Oi.

**Thaiana Lima:** passar uma pergunta.

**Lucas Farias:** Oi.

**Thaiana Lima:** Eu não trabalhei nessa também não. Eu só fiquei na dúvida de uma coisa que você falou que é de verificar se o agendamento é CRC.

**Lucas Farias:** Sim.

**Thaiana Lima:** Isso inclui o agendamento de aplicativo Maria CRC, que é o nosso chatbot ou tá só CRC?

**Lucas Farias:** Eh, boa pergunta. Deixa eu ver.

### 01:20:16

**Emerson Yamamoto:** inclui tudo porque CRC é o tipo de agendamento, Taiana, tipo, todos os outros tipos, eles não são no tipo, eles são no origem agendar, na flag in cidadão.

**Thaiana Lima:** Entendi.

**Emerson Yamamoto:** O único que ficaria fora da CRC seria o agendamento de pauta interna,

**Thaiana Lima:** Tipo de evento ali.

**Emerson Yamamoto:** que é o atendimento, o item cinco ali. Mas eu acho que pauta interna, né?

**Thaiana Lima:** Não sei.

**Emerson Yamamoto:** Pois é, eu acho que não.

**Thaiana Lima:** Entendi. Obrigado.

**Lucas Farias:** Tem até um via atendimento aqui que eu não sei que agendamento é esse.

**Emerson Yamamoto:** Ah, verdade. Via atendimento é o é o atendimento do núcleo digital. Esse entra no pré-atendimento, será?

**Thaiana Lima:** Eu acho que não, porque ali você já tá na hora fazendo contato, enviando dados.

**Emerson Yamamoto:** É,

**Thaiana Lima:** M.

**Emerson Yamamoto:** se esse entrasse a gente precisaria incluir ele. Farias ou vi atendimento.

**Lucas Farias:** Aham.

**Emerson Yamamoto:** Não sei porque que esse a gente criou um evento separado,

**Lucas Farias:** Não sei também.

**Emerson Yamamoto:** mas é assim, essa trava foi mais um, foi mais um plus assim, a gente pode tirar porque e foi mais pra gente, tipo assim, ah, o cara não passar uma audiência, um bloqueio, sei lá, um agendamento que não é CRC, que não que não faz parte, não é um agendamento de fato, né?

### 01:21:32

**Emerson Yamamoto:** Mas a gente pode flexibilizar ou tirar, sei lá.

**Lucas Farias:** É, é, a gente botou mais para proteger, né? Porque provavelmente não vai acontecer, mas para garantir a gente achou melhor colocar essa trava.

**Thaiana Lima:** Tudo bem, é só realmente ver se CRC era origem CRC que estava falando,

**Emerson Yamamoto:** Não,

**Thaiana Lima:** pegando as outras origens também,

**Lucas Farias:** Não,

**Emerson Yamamoto:** não é,

**Thaiana Lima:** então não deve ter problema.

**Lucas Farias:** não é

**Emerson Yamamoto:** é,

**Thaiana Lima:** M.

**Emerson Yamamoto:** é mais abrangente. CRC engloba tudo, aplicativo, Maria, site, tudo, tudo é tipo CS.

**Lucas Farias:** esses tipos aqui são aqueles que aparecem no verde na agenda, né?

**Emerson Yamamoto:** Isso. Exato.

**Lucas Farias:** Quando a gente cria um agendamento,

**Emerson Yamamoto:** Na agenda.

**Lucas Farias:** aí tem um os tipos lá para filtrar são esses aí.

**Emerson Yamamoto:** Exatamente.

**Lucas Farias:** Todos esses que Taiana mencionou entram no CRC, né?

**Emerson Yamamoto:** É, quem começou com isso foi o app, né, que quando o app começou a agendar, ele escolheu ser o tipo CRC, mas com uma um modificador em cidadão. Aí a partir daí tudo virou CRC.

### 01:22:25

**Emerson Yamamoto:** Eu até acho que era para ter um tipo de evento para cada um, mas aí agora é mais difícil de mudar isso, né?

**Lucas Farias:** Show.

**Emerson Yamamoto:** Mas é isso.

**Lucas Farias:** Então, a gente mantém essa esse filtro.

**Emerson Yamamoto:** É só tem que confirmar a questão do viaatendimento, que é o atendimento do núcleo digital, né? Se realmente vai precisaria ter pré-atendimento. Talvez é uma coisa que a gente possa perguntar para pra Talita. Eu acho até que tem,

**Lucas Farias:** Beleza.

**Emerson Yamamoto:** tá? Por isso que eu acho que talvez a gente tenha que flexibilizar para 5 e8, 4 e 8, na verdade. Vou anotar aqui, F, pra gente tirar essa dúvida.

**Lucas Farias:** Tá show.

**Emerson Yamamoto:** Pode seguir.

**Lucas Farias:** Então, vou paraa próxima que tá relacionada com o mesmo assunto. Eh, essa aqui é é naquele end point de gerar o link do pré-atendimento, né, que a gente tem aqui. A gente até mudou ele um pouco, que a gente criou uma nova sessão de pré-endimento. Antes tava tudo no aqui no agendamento e o agendamento tá com muito end point, então a gente achou melhor passar para cá.

### 01:23:33

**Lucas Farias:** Mas o antigo ainda tá lá, não vai quebrar nada se continuarem usando ele.

**Emerson Yamamoto:** É até importante isso, tá? Porque a gente só descontinuou. A gente fez uma cópia, descontinuou, mas ele continua funcionando. Então, daria para fazer uma transição suave assim, subir e falar para eles, ó, agora a gente tá com esse novo end point aí, quando for possível realizem a troca. Eu nem sei se subiu, acho que já subiu esse,

**Lucas Farias:** É esse já.

**Emerson Yamamoto:** mas é só pra gente fazer uma transição suave. Então ele ele vai continuar existindo aí até a gente migrar de vez.

**Lucas Farias:** Isso. E aí a gente vai, achou melhor deixar nessa nova sessão porque podem ter e provavelmente vão ter, né, outros end points de pré-tendimento. Então a gente já deixa tudo aqui centralizado. Aí aqui é a questão agora é que a gente quando a gente gerar um link para um agendamento, né, um pré-tendimento de agendamento, a gente já vai criar esse pré-endimento com status pendentes. Então, vou pegar aqui um um agendamento novo que não tenha pré-atendimento ainda vinculado.

### 01:24:46

**Lucas Farias:** No. Beleza, ele gerou aqui o link e agora eu vou aqui no no evento. E aqui ele já criou com o status pendentes, estatus já tá sendo setado. E a gente também aproveitou para colocar no log, né, essa alteração. Então aqui ele também informa que foi setado pendente ali sem documentos, né, nesse caso, já que não passamos nada. E a outra regra é que se uma for feita uma requisição repetida pro mesmo link e ID de pré-atendimento, a gente não vai registrar esse status pendente e nem alterar o status atual. Então, vou pegar aqui, por exemplo, um evento que ele já tenha um pré-atendimento vinculado, mas ele tem um status diferente do pendente, né? Pegar qualquer um desses aqui. E aí, nesse caso, ele não pode mudar para pendente, não pode voltar atrás, né, do status. Então vou recarregar aqui. É que ele não mudou, deixou iniciado. E aí é um efeito colateral disso é que se o pré-atendimento, se o evento, quer dizer, ele já estiver vinculado com pré-atendimento, mas ele não tiver um status, ele também não vai ser alterado.

### 01:26:37

**Lucas Farias:** Mas isso a gente acha que até faz sentido porque pode ser que o a gente não sabe qual o status de fato desse pré-atendimento, né? Então produção podem ter vários assim, na verdade vão ter vários assim. a gente não sabe se ele já tá iniciado, se ele já tá finalizado. E aí para isso que existe aquele primeiro end point que eu mostrei, que é para atualizar esse valor. Então, vou pegar um desses aqui.

**Emerson Yamamoto:** É basicamente porque a gente vai ter esse passivo, né, de todos os pré-atendimentos que estão sendo criados até até quando isso subir. E a gente nunca vai saber qual é o status deles de fato. Então, se a gente mudar esse N para para algum valor, realmente fica um pouco complicado, porque a gente pode estar sobrescrevendo alguma coisa, voltando ele para pendente, sendo que ele não tá mais pendente, enfim. Então, a gente preferiu não alterar.

**Lucas Farias:** Isso aí eu fiz a requisição para esse segundo aqui e ele também não alterou, deixou no como ele já tava. E aí acho que finaliza essa também.

### 01:27:43

**Lucas Farias:** Beleza.

**Emerson Yamamoto:** Beleza. Lembrando que o o que altera o status de fato, sim, ele poderia alterar o status, né?

**Lucas Farias:** Yes.

**Emerson Yamamoto:** Só esse que? e recebe o link, que teoricamente ele já usa um status eh inicial, é que a gente não seta porque a gente tá entendendo que aquele não é inicial, né? É isso.

**Lucas Farias:** Isso.

**Emerson Yamamoto:** Beleza. Eh, alguma dúvida, pessoal? Alguma questão que vocês queiram comentar? Senão a gente já poderia partir paraa abertura. Ô Diogão, não tem ninguém esperando aí para entrar não? O o Mal tinha falado aqui comigo, até mandei aí no chat, mas agora ele já deve ter até desistido,

**Diogo Leite Mesquita:** Deixa eu ver aqui,

**Emerson Yamamoto:** mas vê aí se tem alguém aí esperando.

**Diogo Leite Mesquita:** cara. Não, a princípio não.

**Emerson Yamamoto:** Beleza.

**Thaiana Lima:** D para abertura, então.

**Emerson Yamamoto:** Uhum.

**Diogo Leite Mesquita:** Depois só se tiver mais alguém que não tá nessa reunião aqui, tá gente? Bota aí no nos comentários o e-mail que eu adiciono.

### 01:29:07

**Emerson Yamamoto:** Vou mandar.

**Thaiana Lima:** Carregando a planilha. Então, a gente tem um conjunto issuesaté eh razoável. Eu tirei da dos candidatos essas três que são notificações necessárias para eh uma funcionalidade do verde, que é alertar quando o endereço do órgão for inativado e existir algum jendamento presencial ali, porque essas me parecem ser mais importantes, mas aí tá tudo pontuado. Vocês podem me dizer se é ou não? Então, a ideia é a gente colocar 30 pontos de API, todas essas que estão em negrito, eh, alterar o encaminhamento pra gente solicitar preferência de atendimento. Só se a pessoa tiver, se o órgão tiver pauta remota ou contato publicável, ou seja, um órgão que não tem nenhuma dessas informações, ele provavelmente só tem presencial. Então, acho que a ideia era não perguntar vai ser questão da Talita alterar um encaminamento processual pra gente reaproveitar ou criar o caso. Isso vem no pedido antigo do Felipe. É, a gente fez o encaminhamento processual ter aquela decisão se vai pro natural ou pro tabelar e depois disso a gente iria começar a criar caso processual ou pro natural ou pro tabelar de acordo com o que a gente encontrar no fluxo de encaminhamento.

### 01:30:51

**Thaiana Lima:** Hoje, a gente cria o caminhamento e para ali, né? A ideia é que o caso venha junto. Eh, a visualização do caso em si, ela hoje tá exibindo vários andamentos, inclusive os andamentos de agendamentos que foram marcados como não visíveis no app. Quando a gente fez essa configuração de não visível, não é, por pauta interna, a gente tirou dos mesmos andamentos, só que o usuário encontrou isso no andamento do caso e aí foi lá no órgão. Então, para deixar consistente, a gente vai tirar do andamento que o usuário enxerga no caso do aplicativo.

**Emerson Yamamoto:** Ja.

**Thaiana Lima:** Eh, essa questão do cadastro eh começou pelo apóstrofe, né, que a pessoa não conseguiu se cadastrar com o nome e com apóstrofe. que na verdade pode, o que não pode é o IFEN. Então, cadastro do de pessoa no o nome da pessoa vai passar a permitir o IFEN. Eh, aqui vem o pedido do Felipe sobre eh o réu liberto não se agendar ele mesmo, mas ter um representante, um familiar, alguém que entre no fluxo de real liberto e e agende ou encaminhe por ali.

### 01:32:00

**Thaiana Lima:** Isso nunca foi previsto. Então, a gente sempre assumia que a pessoa logada no aplicativo, a pessoa logada no chatbot era o próprio R. Agora a gente vai fazer uma pergunta se ele é ou não o réu fazer algumas verificações. Se não for vai pedir o RG se você é representante, tá? Então me dá aqui o RG do R e isso vai ser armazenado no no encaminhamento. Isso para vai ser feito na CRC, vai ser feito no no aplic no fluxo real do aplicativo e da API. Eh, aí temos a consulta de processo verificando a parte informada, porque lá na lá na parte da da Tike, ela precisa saber se a pessoa é ou não ré do processo para fazer a pergunta, né? Porque ver se ela já é a ré do processo. Eu não vou fazer a pergunta se ela é representante ou não. Então, eh, a TEC não sabe disso. A gente vai fazer uma uma alteração na consultora de processo para retornar se aquela pessoa é ré do processo ou não. Aí eu sei se o R liberto é a quem entrou em contato comigo ou se eu pergunto do representante.

### 01:33:08

**Thaiana Lima:** Então, alteração que vai pedir que a TA altere o fluxo para fazer uma uma verificação e uma pergunta lá. A PI sozinha não não eh ajusta isso. E agora volta, né? Uma vez que eu identifiquei que aquela pessoa é representante, no encaminhamento eu vou passar a armazenar o RG do R, que ela me informou manualmente. Aqui é o complemento, é a versão, né, versão app da do que eu falei da Integra, que é alterar o fluxo do réu, verificando se é representante ou próprio. Então, para fazer nos dois meios, né, aqui da Integra aqui do app. E por último, o encaminhamento comum que hoje já é chamado pela rotina quando a pessoa não eh responde. respondida em 30 dias. A mensagem não respondida em 30 dias, ela mandou um e-mail que tá com modelo um pouco misturado entre remoto, presencial. Então, a gente vai fazer um novo modelo de e-mail que avise a pessoa que ela vai ser encaminhada presencialmente porque não foi respondida e tal e vai ser esse meio que vai ser substituído.

### 01:34:13

**Thaiana Lima:** Então, uma substituição de modelo de de meio que é a rotina que chama, tá? Então, foi foram essas que eu separei.

**Leonardo de Melo:** Eh, pode só ver quantas de API tem pro app, porque eu não sei se vai ficar muito desequilibrado.

**Emerson Yamamoto:** Sim, tem bastante de app ali e vai ser bem bastante peso de API. Todas essas de cima ali. app 3 13

**Leonardo de Melo:** É, acho que a principal é de 13, né? É.

**Emerson Yamamoto:** 16 18 20 22.

**Diogo Leite Mesquita:** Mas tá dando quanto aí?

**Thaiana Lima:** Tá dando 30 de API e 11 de R, mas acho que eles estão falando é outra outra questão.

**Leonardo de Melo:** É, é Zap de app. É porque atualmente só tem eu na equipe do app da parte da P.

**Emerson Yamamoto:** Mas o Moltá aí. Mol vai reforçar a equipe. Eu não sei se vai dar para fazer tudo não, mas o Mol vai atuar na equipe do cidadão.

**Leonardo de Melo:** Ah, beleza.

**Emerson Yamamoto:** Audar.

**Felipe Martins Costa Brito:** Quer quer ver alguma para ficar de bônus?

### 01:35:25

**Leonardo de Melo:** Aí tá aí.

**Felipe Martins Costa Brito:** Diogo não, desculpa aí.

**Emerson Yamamoto:** É, o grande problema, eu acho que é a de 13, assim, a gente,

**Thaiana Lima:** Ah.

**Emerson Yamamoto:** o o Leonardopode pegar a de 13, por exemplo, e aí o Mol tá chegando agora nessa equipe. O Mol tá um nomeade de equipe, ele tá transitando em todas as equipes. Então é natural que é mais complicado de atuar na equipe do cidadão, alguém que chegou agora. O sistema tem muita história, é muito complicado. Então ele vai tentar ajudar nessas outras iss aí de três, dois pontos, ver se dá para para seguir, entendeu? Mas realmente tem muita pontuação de API do app. É porque é meio complicado, né, API, mas é API do app e não integra. Porque o Alexandre e o Farias só trabalham na Integra PI, já que eles também tão no verde. Bem complexa essa organização, mas enfim, é isso. Tá, tá com bastante ponto de app, é isso que eu quero dizer. E aí pode ser que isso complique um pouco paraa gente entregar tudo, mas não não adianta botar como o principal é a de 13, né?

### 01:36:35

**Emerson Yamamoto:** Então tem muito o que fazer. A gente vai ver o que dá para fazer para entregar aí de app, tentar entregar tudo. Mal é bom, vai conseguir dar conta aí.

**Leonardo de Melo:** É isso. Qualquer coisa eu aí também os caminhos.

**Emerson Yamamoto:** Sim, sim,

**Thaiana Lima:** Então a gente fecha assim.

**Emerson Yamamoto:** é, vamos fechar assim, vamos ver o que que dá. Vamos, vamos fazer um uma experiência porque vai ser a primeira sprint do M, né? Então vamos ver se se a gente consegue evoluir para entregar tudo. Senão a gente chega atéonde o máximo que a gente conseguir. De com certeza vai entregar porque a gente tem dois debit para fazer, sei lá, cito, oito pontos. É muito pouco. Qualquer coisa eu peço ajuda pro Farias e pro Alexandre aí no cidadão também. Mas aí, como eu falei, é outro contexto totalmente diferente. Não é não é tão simples essa migração, não.

**Thaiana Lima:** que eu esqueci do o tr.

**Gustavo Pinto:** Então é só questão, é só ver a data.

### 01:37:56

**Gustavo Pinto:** Então é isso,

**Emerson Yamamoto:** Sim.

**Thaiana Lima:** É isso.

**Gustavo Pinto:** já que já que já que já que é o que é o que temos,

**Thaiana Lima:** É, Diogo e Felipe deram OK. M.

**Gustavo Pinto:** né? Não temos não temos outra solução.

**Emerson Yamamoto:** É o que tem.

**Gustavo Pinto:** É o que temos. Eu vi que o Marcos tá de férias na semana que vem, né? Mas eu o Marcos é é fronte,

**Emerson Yamamoto:** É,

**Gustavo Pinto:** né?

**Emerson Yamamoto:** a gente tá com pouco ponto de fronte,

**Gustavo Pinto:** É, eu vi ali.

**Emerson Yamamoto:** isso não vai ser problema não.

**Gustavo Pinto:** É, é, eu tava olhando exatamente isso. Beleza.

**Emerson Yamamoto:** É, pelo pelo que eu vi aqui, cai dia 12.

**Gustavo Pinto:** Datas tem finados

**Emerson Yamamoto:** O problema é que tem tem finados.

**Gustavo Pinto:** dia dois,

**Emerson Yamamoto:** dia dois, então não sei se tá

**Gustavo Pinto:** dia do servidor público pra gente não faz diferença, né? a gente não usa. Eu não sei se a a Defensoria

**Emerson Yamamoto:** eles vão emendar, eu acho.

### 01:38:45

**Emerson Yamamoto:** Vai, vai pro dia 30 esse feriado. Vai ser feriadão aí eu acho,

**Gustavo Pinto:** a É vai ser feriadão, dia 30.

**Emerson Yamamoto:** né, Diogão? Acho que tá decidido,

**Gustavo Pinto:** É,

**Emerson Yamamoto:** né? É isso.

**Gustavo Pinto:** éendal aqui.

**Diogo Leite Mesquita:** Hoje eu parta para sexto.

**Emerson Yamamoto:** Sempre fazem isso. Então, não sei. Tal eu sugeriria talvez jogar um pouquinho mais para frente, hein?

**Gustavo Pinto:** Uhum.

**Emerson Yamamoto:** Em vez de 12, jogar para 17, que é terça-feira. Ganhar aí sexta e segunda.

**Gustavo Pinto:** Uhum.

**Emerson Yamamoto:** Seria bom para vocês. 17.

**Gustavo Pinto:** Deixa eu ver aqui se eu tenho coisa já indicada. Não tem nada marcado na minha agenda. Então tem CCAR na segunda exatamente antes, mas não faz diferença, né? Não é a mesma equipe. Угуm.

**Diogo Leite Mesquita:** 17 terça tá livre.

**Emerson Yamamoto:** É mais pra gente tentar entregar tudo mesmo. Eu eu geralmente não gosto de mudar a data, não. É bom deixar fixo, mas talvez com 12, menos gente, feriado vai apertar um pouquinho, a não ser que a gente queira reduzir a pontuação,

### 01:39:57

**Diogo Leite Mesquita:** O Ian tá por aí.

**Emerson Yamamoto:** senão

**Diogo Leite Mesquita:** Yann,

**Yann Naylor Francisco:** Tô aqui, tô aqui. Diga aí.

**Diogo Leite Mesquita:** você pode duplicar essa também que acho que eu não vou estar ainda não, cara.

**Yann Naylor Francisco:** Posso, posso sim.

**Diogo Leite Mesquita:** Voltar férias.

**Yann Naylor Francisco:** Dia 17.

**Diogo Leite Mesquita:** É, vai ser o último dia das minhas férias.

**Gustavo Pinto:** Ô, Diogo volta,

**Diogo Leite Mesquita:** Yeah.

**Gustavo Pinto:** Diogo volta só no final do ano, no janeiro já.

**Yann Naylor Francisco:** Diogoé só em janeiro.

**Gustavo Pinto:** Ele tira férias e já não volta mais agora.

**Felipe Martins Costa Brito:** Mas, mas vem cá,

**Yann Naylor Francisco:** Só em janeiro.

**Felipe Martins Costa Brito:** que férias é essa? De que exercício?

**Emerson Yamamoto:** eu queria também.

**Yann Naylor Francisco:** Hum. É.

**Emerson Yamamoto:** Tô precisando não.

**Gustavo Pinto:** Eu

**Felipe Martins Costa Brito:** Já é de já é do exercício 202.

**Emerson Yamamoto:** O Felipe nem pode falar nada que o Felipe tira mais cinco férias por ano.

**Yann Naylor Francisco:** Felipe não, eu ia falar exatamente isso.

**Emerson Yamamoto:** Então, né?

### 01:40:29

**Felipe Martins Costa Brito:** Não, não.

**Yann Naylor Francisco:** É exato,

**Emerson Yamamoto:** Aí também não tem lugar de fala não.

**Yann Naylor Francisco:** exato, exato. Felipe é outro. 17 de novembro, 2:30.

**Gustavo Pinto:** eu eu alcancei o que eu queria, que era só criar Discordia.

**Yann Naylor Francisco:** Boa.

**Emerson Yamamoto:** É 2:30. Tranquilo.

**Yann Naylor Francisco:** Deixa eu ver.

**Emerson Yamamoto:** Terça-feira.

**Gustavo Pinto:** É.

**Yann Naylor Francisco:** Tá enviado aí, pessoal.

**Diogo Leite Mesquita:** chegando inclusive o recesso, né? Temos que ver aí se impacta em alguma questão de sprints,

**Emerson Yamamoto:** Sempre tem quear o no recesso,

**Diogo Leite Mesquita:** de entregas e de mensagens de API,

**Emerson Yamamoto:** Diogão, né?

**Diogo Leite Mesquita:** de alguma coisa aí, né? Você fica naquela ai ninguém me falou e aí não sabia que isso tinha que mudar, né, Dr.

**Emerson Yamamoto:** É.

**Diogo Leite Mesquita:** Felipe?

**Gustavo Pinto:** Ô, ô, Felipe, eh, a Tik tá lá com todo o esquema de de atendimento durante o recesso, já já funcionando. Vocês já testaram lá na homologação?

**Felipe Martins Costa Brito:** em em tese.

### 01:41:18

**Felipe Martins Costa Brito:** Sim.

**Emerson Yamamoto:** Recesso tá mais que testado já,

**Gustavo Pinto:** Depois vale a pena fazer

**Emerson Yamamoto:** pô.

**Felipe Martins Costa Brito:** Em tese,

**Emerson Yamamoto:** validado.

**Felipe Martins Costa Brito:** sim. Não,

**Gustavo Pinto:** um teste de novo, né?

**Felipe Martins Costa Brito:** eu fiz eu fiz um teste num feriado desses e deu certo. Um desses feriados que emendou, acho que 7 de setembro, não sei, mas eu fiz um teste num feriado que que emendou e eu criei um recesso específico e funcionou na tec normal.

**Gustavo Pinto:** Não, beleza. É só é só aquela pergunta pra gente não sair na

**Felipe Martins Costa Brito:** Mas aí eu eu vou boa boa boa boa colocação que eu testo agora no feriado de de 32 eu crio recesso.

**Gustavo Pinto:** Uhum. Ah,

**Diogo Leite Mesquita:** Tem um esquema de app,

**Gustavo Pinto:** sim.

**Diogo Leite Mesquita:** tem o esquema de Maria e tem o esquema do da CAN também, né, da do telefone.

**Emerson Yamamoto:** É,

**Felipe Martins Costa Brito:** Não,

**Diogo Leite Mesquita:** Então eu p

**Felipe Martins Costa Brito:** mas o o da Can, é, a ura já tá pronta.

### 01:42:10

**Felipe Martins Costa Brito:** da C. Não, não, não,

**Emerson Yamamoto:** é porque verde,

**Felipe Martins Costa Brito:** não é não,

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** não, não interfere nada verde

**Emerson Yamamoto:** A já tá em funcionamento, Felipe.

**Felipe Martins Costa Brito:** já. Acho que já tá desde lá abril, eu acho. Abril ou maio. Abril.

**Emerson Yamamoto:** É porque eles pediram token agora é outra coisa.

**Felipe Martins Costa Brito:** Não, isso aí é um desenvolvimento que eu pedi.

**Emerson Yamamoto:** Ah, tá,

**Felipe Martins Costa Brito:** É outra coisa.

**Emerson Yamamoto:** entendi. Saquei.

**Felipe Martins Costa Brito:** Isso outra parada. A que tá em funcionamento, tá?

**Emerson Yamamoto:** Tá. Eh,

**Gustavo Pinto:** Mas, mas eles perderam o token,

**Emerson Yamamoto:** deixa eu perderam.

**Gustavo Pinto:** né? Porque porque

**Felipe Martins Costa Brito:** perderam toque porque ainda não eh tá com a equipe do Alan, Gustavo, botar em produção a questão До

**Gustavo Pinto:** No. Não, o token que eu digo que eles usam em produção, Felipe, não existe outro, entendeu? É o mesmo token.

### 01:42:59

**Felipe Martins Costa Brito:** Então,

**Gustavo Pinto:** É isso.

**Felipe Martins Costa Brito:** mas ainda não tá usando,

**Gustavo Pinto:** É isso que a gente não tem. Ah,

**Felipe Martins Costa Brito:** não tá usando o token porque ainda tá dependendo daquelas issos lá do do verde dois, entendeu? Ainda não tá integrado com verde não.

**Gustavo Pinto:** não.

**Felipe Martins Costa Brito:** Ainda não.

**Gustavo Pinto:** Ah,

**Felipe Martins Costa Brito:** Eu até falei com a Alan isso essa semana.

**Gustavo Pinto:** mas a gente

**Felipe Martins Costa Brito:** Ela não, já eu acho que Ian já é a equipe do Ian acho que já homologou. Ele ia ver contigo uma data para subir.

**Gustavo Pinto:** Ah, é isso aí que isso já tinha sido resolvido há muito tempo,

**Felipe Martins Costa Brito:** Conversa com ele que ele que que ele não tá

**Gustavo Pinto:** que o problema Ah, o problema foi na reunião. Ah, sim,

**Felipe Martins Costa Brito:** me lembra que foi na na reunião.

**Gustavo Pinto:** tinha agora. É, tava isso, é,

**Felipe Martins Costa Brito:** Isso é isso.

**Gustavo Pinto:** tava uma confusão.

### 01:43:36

**Gustavo Pinto:** Aí fizeram uma reunião e finalmente deu certo. É isso. É isso.

**Felipe Martins Costa Brito:** Só que aí ele aí aí ficou o pessoal do do Verdedor de fazer os ajustes. Acho que fizeram.

**Gustavo Pinto:** Uhum.

**Felipe Martins Costa Brito:** Acho que já até homologou. Acho que só falta subir.

**Gustavo Pinto:** E então não sei, tem que ver isso.

**Felipe Martins Costa Brito:** Fala eh conversa com ele que eu falei disso com ele essa semana.

**Gustavo Pinto:** Vou perguntar para Tá, tá bom. Tá beleza. Beleza. Mas o o de qualquer forma a Can já tá consultando algumas coisas no fluxo lá da URA, não tá? Porque ele tá ele tá ele tá usando.

**Felipe Martins Costa Brito:** tá fazendo testes agora.

**Gustavo Pinto:** Ah, tá.

**Felipe Martins Costa Brito:** Tá fazendo testes para um para uma para verbalizar o andamento do processo. Por isso que ele pediu, porque ele percebeu que caiu, entendeu?

**Gustavo Pinto:** Ah,

**Felipe Martins Costa Brito:** Percebeu que caiu.

**Gustavo Pinto:** tá bom.

**Felipe Martins Costa Brito:** Enfim,

### 01:44:14

**Gustavo Pinto:** Então,

**Felipe Martins Costa Brito:** tá?

**Gustavo Pinto:** então ele a parte boa é que isso não tá impedindo o ambiente de produção dele. Essa é a parte boa.

**Felipe Martins Costa Brito:** Não, não está.

**Gustavo Pinto:** Tá bom. Menos mal. Porque a gente ficou, fiquei até preocupado aqui. A gente tava em reunião, mas ele tava pedindo um negócio de produção. Falei assim: "Ih, caramba, parou alguma coisa lá." Bom,

**Felipe Martins Costa Brito:** Não parou, não parou não.

**Gustavo Pinto:** menos. Beleza. Tá joia, gente. Obrigado.

**Emerson Yamamoto:** Só uma última coisa,

**Gustavo Pinto:** Deixa eu pelo menos o meu

**Emerson Yamamoto:** aproveitar aproveitar que o Ian tá aí que ele não tava na hora que eu falei que é a questão do gov. Eu tava falando que a gente deve liberar até amanhã, né, uma versão ambiente tem do GOV no aplicativo e no verde, porque o verde vai precisar identificar essas verificações, né, saber que foi pelo e tal. E e essa versão de app também vai ter várias outras correções, inclusive aquela correção da N aplicação de verificações de identidade, que é um problema que a gente já tentou corrigir algumas vezes e e não resolveu ainda.

### 01:45:08

**Emerson Yamamoto:** Então, a gente deve liberar até amanhã, mais ou menos essa versão para vocês homologarem e logo depois a gente vai testar também aqui com a nossa equipe de teste pra gente poder planejar uma subida. Eu acho que acho que isso ganhou prioridade, né? Então, só paraa ciência aí de posteriormente vocês homologarem essa parte. Só vai ter que ver na hora de subir a questão do se você já tem um broken em produção. Acredito que sim, né? Porque eu acho que GVBR já subiu no Maria.

**Gustavo Pinto:** OBR tá no Maria, já tá em produção já.

**Yann Naylor Francisco:** Isso.

**Emerson Yamamoto:** Entendi.

**Gustavo Pinto:** Já tá.

**Emerson Yamamoto:** Então, então isso aí de boa, tá? tá resolvido.

**Yann Naylor Francisco:** Tranquilo.

**Gustavo Pinto:** Так.

**Yann Naylor Francisco:** Publica lá. var. A lista de de coisa para homologar tá gigantesca, mas vai dar tudo certo.

**Emerson Yamamoto:** Go BR são duas isso, só uma do app, uma do verde. É bem tranquilo.

**Yann Naylor Francisco:** É, aí entra nível de prioridade aqui. Vamos ver.

### 01:46:07

**Yann Naylor Francisco:** Mas beleza,

**Emerson Yamamoto:** Tranquilo.

**Yann Naylor Francisco:** manda assim, por favor.

**Emerson Yamamoto:** Beleza. É isso, pessoal. Obrigado. Até mais.

**Gustavo Pinto:** Boa tarde, pessoal. Parabéns aí pela pela apresentação.

**Yann Naylor Francisco:** Valeu,

**ICARO LUIZ ALBAR EDUARDO:** Fala pessoal.

**Yann Naylor Francisco:** pessoal. Boa tarde. Obrigado, hein,

**Thaiana Lima:** Чи

**Diogo Leite Mesquita:** Ô Gustavo e Emerson,

**Bianca Tavares Soares Silva:** Ah, tá pessoal, boa tarde,

**Emerson Yamamoto:** Sim.

**Gustavo Pinto:** Diogo.

**Diogo Leite Mesquita:** a gente precisa só alinhar essa questão do deploy das próximas APIs, tá? Marcar uma reunião, alguma coisa.

**Gustavo Pinto:** Sim. O Martins já passou pra gente a lista. Eu já repassei poema, senão a gente vai ver logo o que que tem lá de dependência,

**Diogo Leite Mesquita:** Eh,

**Gustavo Pinto:** tá?

**Diogo Leite Mesquita:** o Ícaro me passou uma listinha aqui também. Eu não sei se a Camila tem,

**Emerson Yamamoto:** Ja.

**Diogo Leite Mesquita:** mas aí eu não sei se a gente consegue chegar a algum acordo aí, é porque também tem as homologações do do Ian, né?

### 01:46:50

**Diogo Leite Mesquita:** Eh, naquela listinha lá tem o que tá homologado, que não tá. A gente precisa dessa listinha para poder passar pro Ian e ver se é

**Gustavo Pinto:** Mhm.

**Emerson Yamamoto:** Na minha lista também tem.

**Diogo Leite Mesquita:** factí.

**Emerson Yamamoto:** Ô Diogão, o que tá homologado? Não atualizei também.

**Diogo Leite Mesquita:** É, tem algumas lá mais antigas de sprint 4, 5 que não tão, eu não sei se a gente eh precisa de uma atuação junto, se se algumas coisas aí tem que conversar com aí, se a gente vai ter que fazer plantão, mas acho que é melhor talvez vocês conversarem primeiro e a gente ter essa conversa. e fez tipo assim,

**Emerson Yamamoto:** Uhum.

**Diogo Leite Mesquita:** ah, vamos conseguir botar tudo até sprint 5 ou seis, fazer uma onda, entendeu?

**Emerson Yamamoto:** É, pelo que eu vi, não era nada pendente do nosso lado, não. Até olhei, realmente tem uma uns buracos ali de homologação de algumas IFS antigas, mas eu não vi nenhum comentário cobrando nada, então fala aí, ó.

**Yann Naylor Francisco:** Não, acho que o que a gente precisa mais, ô Emerson, é o que que a gente consegue subir, entendeu?

### 01:47:51

**Yann Naylor Francisco:** Independente que esteja em homologação ou não. Ah,

**Emerson Yamamoto:** Uhum.

**Yann Naylor Francisco:** tá, eu consigo subir tudo de uma só vez. Aí aqui a gente se organiza, entendeu? Ah, eu não consigo subir tudo de uma só vez. Eu tenho que fazer em lote. Aí, beleza. Esse lote como é que é? A gente consegue começar quando? Eh,

**Emerson Yamamoto:** Uhum.

**Yann Naylor Francisco:** é mais isso, porque eu sei que vai ter pendência nossa aqui de homologação, porque tem 1000 projetos para homologar,

**Emerson Yamamoto:** Ah, sim, sim, sim,

**Yann Naylor Francisco:** mas eu preciso ter um norte. E esse norte,

**Emerson Yamamoto:** sim.

**Yann Naylor Francisco:** ele vem, claro, da priorização interna aqui, mas ele também vem do das issas que vocês conseguem disponibilizar em produção através de pacotes. s\*\*\*. Yeah.

**Emerson Yamamoto:** Sim. Não, tranquilo, tranquilo.

**Diogo Leite Mesquita:** Eu fiz um simulado aqui,

**Emerson Yamamoto:** É porque tô vendo.

**Diogo Leite Mesquita:** vocês estão vendo aí a aquela planilha?

### 01:48:39

**Emerson Yamamoto:** Ah, sim.

**Diogo Leite Mesquita:** Aí eu dupliquei aquela planilha que vocês têm e fiz um recorte, tipo sprint 1 2 3 4 5 e 6. Eh, aí fui pegando aqui também, botando tudo em amarelinho. 1 2 3 4 Aí 7 8 não. 4 11 9 não e 7 8 não. Aí eu marquei em laranja as que o Felipe falou que seria interessante e marquei

**Emerson Yamamoto:** M.

**Diogo Leite Mesquita:** em roxo algumas que o Cuíaro tinha comentado que seria interessante para ele. E aí eu acho que se a gente conseguir priorizar o que é de até sprint 7, eh sprint 6, desculpa, eh seria um um bom recorde.

**Emerson Yamamoto:** É, o que é importante subir, que não tá na sua lista aí, é aquela primeira, a segunda do geral, que é o a questão da alteração dos nomes, porque isso até hoje já tá diferente no verde. O verde já cito Maria,

**Diogo Leite Mesquita:** aqui.

**Emerson Yamamoto:** mas lá tá via atendimento.

**Diogo Leite Mesquita:** Posso até botar que talvez esse daqui seja importante. O

### 01:49:47

**Gustavo Pinto:** Essa daí é até prioritária, Diogo,

**Emerson Yamamoto:** É,

**Gustavo Pinto:** nas nas coisas que a gente tá conversando,

**Emerson Yamamoto:** essa é

**Gustavo Pinto:** inclusive com a Camila.

**Diogo Leite Mesquita:** aqui talvez o Ian tenha que priorizar.

**Emerson Yamamoto:** isso sim.

**Diogo Leite Mesquita:** Então, eh,

**Emerson Yamamoto:** Essas do via,

**Diogo Leite Mesquita:** vamos passando aqui

**Emerson Yamamoto:** essas do via atendimento que o Ícaro marcou, só tem que ver porque eu não sei o quanto elas impactam o sistema lá do Braid, porque se impactar ele teria que se adaptar. e fazer adaptações. Então essas tem que dar uma olhada se precisa ou não adaptar.

**Diogo Leite Mesquita:** e tá interessante. É só descendo aqui.

**Emerson Yamamoto:** E a mesma coisa com as do chatbot, Diogão, tem que ver só se a Tik precisa ajustar algo na PI delas para a gente poder liberar eles ajustarem e depois a gente combinar de subir, entendeu?

**Diogo Leite Mesquita:** Tá. Ô Ian, você sabe, você tem alguma pendência nessas duas aqui? Nessa e nessa na 961,

**Emerson Yamamoto:** Tem o link ali. Pode até abrir ali, Diogão.

### 01:50:41

**Emerson Yamamoto:** Tem o link ali.

**Diogo Leite Mesquita:** pacote de prioridades e rotina.

**Yann Naylor Francisco:** A princípio deve ser só pra gente incluir paraa priorização de homologação,

**Diogo Leite Mesquita:** Não,

**Yann Naylor Francisco:** ô Diogo. Só que eu recebi uma outra priorização de homologação.

**Diogo Leite Mesquita:** não,

**Yann Naylor Francisco:** Aí a gente precisa conversar internamente.

**Diogo Leite Mesquita:** eu tô não. Perfeito. Eu só tô, acho que a lista aqui que eu marquei de priorização é uma, duas, 3, 4, cro eixos nesse universo. Acho que não,

**Yann Naylor Francisco:** É,

**Diogo Leite Mesquita:** não é um túmulo tão grande,

**Yann Naylor Francisco:** aí eu tenho uma outra listagem maior que

**Diogo Leite Mesquita:** mas essa listagem é da Camila,

**Yann Naylor Francisco:** Aham.

**Diogo Leite Mesquita:** tá?

**Yann Naylor Francisco:** E que sobe semana que vem.

**Diogo Leite Mesquita:** Mas é de API.

**Yann Naylor Francisco:** Tem em teoria,

**Diogo Leite Mesquita:** Mas é de API.

**Yann Naylor Francisco:** não.

**Gustavo Pinto:** É de verde, ô Diogo.

**Yann Naylor Francisco:** Exato.

**Diogo Leite Mesquita:** É de deploy de ver.

**Gustavo Pinto:** É do é é distribuição de plantão e distribuição de

### 01:51:28

**Yann Naylor Francisco:** Uhum.

**Gustavo Pinto:** agravo.

**Yann Naylor Francisco:** Que é bem punk,

**Diogo Leite Mesquita:** Tá tudo bem.

**Gustavo Pinto:** É.

**Diogo Leite Mesquita:** Eh, mas aí só para combinando aqui com vocês,

**Yann Naylor Francisco:** mas a gente consegue moldar, tá?

**Diogo Leite Mesquita:** não? Perfeito. Não é porque acho que tô entendendo que isso aqui não interfere lá tecnicamente. Aí a minha dúvida é, o Emerson,

**Emerson Yamamoto:** M.

**Diogo Leite Mesquita:** uma vez num cenário perfeito que a equipe aqui da Defensoria consiga homologar essa Sim Dá para subir esse pacote.

**Emerson Yamamoto:** Então só tem que ver essa questão que eu falei do que que tem dependência externa externa a nós, inclusive que é assim, o que que depende da taque, o que que depende do maria, entendeu? Que eu não posso subir uma coisa que vai quebrar a ta quebrar o maria, entendeu?

**Diogo Leite Mesquita:** Tá, tá bom. Vamos tentar trabalhar com isso. Eh, eu sei que é prioritário, mas aí a gente vê, por exemplo, aí sobe só essa daqui, que é muito importante, e aí depois sobe esse outro pacote.

### 01:52:21

**Diogo Leite Mesquita:** Aí eu te mando isso aqui, aí a gente conversa semana que vem de novo.

**Emerson Yamamoto:** Tá? É, a sprint 11 especificamente ainda não está em em homologação porque é a sprint anterior, é a que a gente acabou de terminar antes dessa agora. Então aquela ali importante ainda não tá em homologação. A gente vai precisar subir ainda.

**Diogo Leite Mesquita:** Beleza? Aí talvez vocês possam falar que seja mais simples a gente subir um um pacote sem essa, entendeu? Do até a meu com essas que a gente marcou aqui que tão que tão marcadas como homologadas,

**Emerson Yamamoto:** Não dá para subir ela.

**Diogo Leite Mesquita:** entendeu?

**Emerson Yamamoto:** Poderia ser até o pacote com ela também, tudo junto mesmo.

**Diogo Leite Mesquita:** Tá, tá bom. A gente tem um panorama aí, a gente volta a conversar, conversar internamente aqui, eu falo com vocês. Fala aí,

**Yann Naylor Francisco:** Eh, nesse conjunto de entender se tem independência ou não, aí eu acho que a gente vai precisar do apoio de vocês da da COP,

**Emerson Yamamoto:** Sim, sim.

### 01:53:19

**Emerson Yamamoto:** Eh,

**Yann Naylor Francisco:** né?

**Emerson Yamamoto:** eu vou dar uma avaliada nisso, no que que pode depender de outros sistemas fora da gente, porque eu botei ali dependência, mas eu tava pensando em dependência de verde, cidadão e não e não de ta e via,

**Yann Naylor Francisco:** É isso.

**Emerson Yamamoto:** né, que entrou agora. Então eu vou avaliar isso. Me manda o link depois dessa planilha aí, Diogo,

**Diogo Leite Mesquita:** Tá.

**Emerson Yamamoto:** que eu posso avaliar eh dentro dessas que vocês selecionaram o que que tem independência de ajuste.

**Diogo Leite Mesquita:** Tá. Só eu vou te passar, mas aí só eu, como eu copiei, pode ser que alguém mexa lá na outra e não mexa aqui, a gente se perca, mas talvez.

**Gustavo Pinto:** Não é melhor mexer naquela que já tem. Você tem permissão para mexer?

**Diogo Leite Mesquita:** Eh, não,

**Gustavo Pinto:** Não.

**Diogo Leite Mesquita:** não tinha, não tinha permissão. Por isso que eu talvez a aí eu faço, pode fazer o seguinte, a gente pega aquela lá, gera uma nova aba, versiona, entendeu?

**Emerson Yamamoto:** Uhum.

### 01:54:06

**Emerson Yamamoto:** Pode ser.

**Diogo Leite Mesquita:** trava a trava a versão antiga e vai mexendo. Beleza,

**Emerson Yamamoto:** Tá,

**Diogo Leite Mesquita:** tranquilo.

**Emerson Yamamoto:** eu vou gerar uma nova aba aqui de proposta de deploy se você quiser de algum copiar para cá ou refazer essas marcações. Vou liberar aqui para vocês poderem editar.

**Diogo Leite Mesquita:** OK. Beleza. Vou mandar lá no, posso mandar lá no grupo mesmo de versão técnica. Isso aí, não tem problema não. Vou liberar. Valeu. É,

**Emerson Yamamoto:** Beleza.

**Gustavo Pinto:** Encerramos.

**Emerson Yamamoto:** Quem você quer que possa editar aí, Diogão? Você, o Ian e mais quem?

**Diogo Leite Mesquita:** acho que é o e Camila, cara. Reativado em novembro do feedback os clientes da

**Emerson Yamamoto:** Beleza,

**Diogo Leite Mesquita:** comunidade reativaram.

**Emerson Yamamoto:** show de bola. Criei a criei uma nova aba aqui. Valeu. É isso, pessoal. Ó,

**Diogo Leite Mesquita:** Valeu,

**Emerson Yamamoto:** vou mandar lá aqui.

**Diogo Leite Mesquita:** pessoal.

**Emerson Yamamoto:** Mais

**Gustavo Pinto:** Até mais, pessoal. Boa tarde,

**Leonardo de Melo:** Olha p

**Lucas de Oliveira Mol Silva:** Valeu, pessoal. Yeah.
