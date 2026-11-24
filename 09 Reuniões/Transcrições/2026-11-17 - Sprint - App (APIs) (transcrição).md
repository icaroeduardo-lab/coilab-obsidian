---
tipo: transcricao
data: 2026-11-17
reuniao: "[[2026-11-17 - Sprint - App (APIs)]]"
tags:
  - transcricao
  - sprint
---

# Sprint - App (APIs): transcrição (17/11)

> Transcrição automática do Google Meet; pode conter erros. Ata: [[2026-11-17 - Sprint - App (APIs)]]. Encerrada após 02:18:12.

### 00:00:22

**Emerson Yamamoto:** Fala, doutor. Boa tarde.

**Yann Naylor Francisco:** fala.

**Bianca Tavares Soares Silva:** Boa tarde,

**Emerson Yamamoto:** Tranquilo.

**Yann Naylor Francisco:** Так. Emerson, hoje só vai ter a gente aqui. Eu, Bianca, Léo. Léo vai entrar aí daqui a pouco, Felipe. Mas por enquanto Camila tá voltando de viagem. Eh, e o Diogo tá de férias. Vou ver confirmar se o Íaro vai entrar e aí vocês podem iniciar,

**Emerson Yamamoto:** Tranquilo.

**Yann Naylor Francisco:** tá bom?

**Emerson Yamamoto:** Show de bola. Gustavo também falou que não era para esperar ele,

**Yann Naylor Francisco:** É,

**Emerson Yamamoto:** então só vou esperar a galera entrar aí.

**Yann Naylor Francisco:** a Camila só me deu uma informação aqui que naquele no quesito de abertura, né, na hora de pontuar, que a gente foque lá na questão do pré-atendimento para varas. Ela já já eu acho que já falou até com o Gustavo sobre isso, mas aí na abertura a gente vê

**Emerson Yamamoto:** Tá. Eu acho até que essa informação é mais importante pra Thaiana,

### 00:04:49

**Yann Naylor Francisco:** isso.

**Emerson Yamamoto:** que eu acho que a Thaiana não entrou ainda.

**Yann Naylor Francisco:** Tá, tá bom. Vamos esperar. Quando chegar no final, a gente a gente vê isso,

**Emerson Yamamoto:** Beleza,

**Yann Naylor Francisco:** ó. O Ícaro já entrou aí. Felipe tá aí também aqui do nosso lado.

**Emerson Yamamoto:** tranquilo. Esperar a Thaiana entrar aí. E faltou o Alexandre também. Что?

**Leonardo de Melo:** Boa tarde,

**Emerson Yamamoto:** números atualizados aí, já que vocês estão acompanhando, a gente já tem 1567 pessoas validadas com gov. Para tu ver, ontem 10 horas da manhã, não, 10 não, meio-dia tava em 1000, né? De ontem para hoje já teve mais 500 pessoas. Muito doido isso.

**Yann Naylor Francisco:** Bo coisa boa. Coisa boa. Menos 1500 pessoas aí para para CRC validar.

**Emerson Yamamoto:** Sim, Alexandre, ele já entrou. Gabriel, Marcos estão aí, Lucas, Lucas e Léo. É, eu acho que tá todo mundo aí. Agora acho que a gente já pode começar.

### 00:07:48

**Emerson Yamamoto:** Eh,

**Yann Naylor Francisco:** Так. Yeah.

**Emerson Yamamoto:** só um minuto. Vamos lá. Vou compartilhar aqui pra gente mostrar a ordem. Eu priorizei o app. Vou colocar as do app primeiro e depois a gente parte pra parte da integra. Beleza? Show. Bom, então a gente tá com essa sprint aqui que tá bem eh meio a meio. Acho que tem uma eixa a mais de, mas são nove eixos. Eh, e aí a gente vai começar aqui com a 1043, que é o alterar encaminhamento para solicitar preferência de atendimento apenas se houver pauta remota ou contato publicável do órgão. É uma iso basicamente para hoje em dia, né? A gente solicita a preferência remota ou presencial, independente de qualquer regra. E agora o que a gente vai ver é se aquele órgão que que vai receber o encaminhamento, se ele possui uma pauta remota ou se ele tem algum contato publicável. Até porque se ele não possuir nenhum desses dois, não tem muito o que fazer de encaminhamento remoto.

### 00:09:10

**Emerson Yamamoto:** O encaminhamento remoto seria mostrar o endereço. Então agora a gente vai aplicar essa regra para poder mostrar o a opção do remoto ou apenas a opção de presencial mesmo com o endereço. Aí depois a gente tem a 10678. alterar a visualização do caso, ocultando o andamento de agendamento de pauta interna configurado como não visível no app. Fala aí, ó.

**Yann Naylor Francisco:** Só colocar para gravar aqui.

**Emerson Yamamoto:** Tranquilo.

**Yann Naylor Francisco:** Isso aqui ajuda na na hora da homologação.

**Emerson Yamamoto:** Beleza.

**Yann Naylor Francisco:** Valeu, pessoal. Desculpa. Pode continuar. Yeah.

**Emerson Yamamoto:** Eh, então essa 10678 e é basicamente porque apesar de agora o app eh não exibir, né, o os agendamentos de pauta interna configurados como não visíveis, eh, o andamento tava aparecendo. Então, agora a gente vai fazer uma modificação para que o andamento desse agendamento também não apareça, que é o que faz sentido, né? Depois a gente tem a 10682, alterar cadastro de pessoa permitindo o IFEN. Essa foi uma melhoria que foi pedida em relação a a nomes com IFIN.

### 00:10:30

**Emerson Yamamoto:** O app não tava permitindo, não é tão comum assim, mas existe. E agora a gente vai permitir nomes com if. A gente já tinha permitido o apóstrofo, né? E agora a gente vai permitir também o if. Depois a gente tem a 10689, alterar fluxo de réu liberto, verificando se o assistido é o próprio réu ou representante. Eh, aqui a gente eh agora vai dar essa opção do assistido ser o representante, né, e não o próprio Ré Liberto, que aí a gente consegue fazer uma lógica ali para se ele for o representante informar o RG do réu, enfim. Eh, eh, a gente vai tá acrescentando mais funcionalidade nesse fluxo de ré liberto, porque antes, se eu não me engano, era só pelo RG mesmo do próprio R, né? Você teria que ser o próprio R. Depois a gente tem a 10626, que é a última do app, que é alterar encaminhamento processual para reaproveitar ou criar caso processual. Eh, aí a gente vem na parte do encaminhamento processual, criar caso, que é uma coisa que já foi discutida há tantos anos, né?

### 00:11:40

**Emerson Yamamoto:** Acho que deve ter pelo menos uns 4 anos que a gente discute isso de criar ou não caso processual para encaminhamento. E agora a gente vai implementar e inclusive essa é a ISO mais complexa dessa sprint com 13 pontos. E aí, ou a gente vai reaproveitar ou vai criar o caso processual. Beleza? Depois a gente tem, partindo agora para para as IFS da Integra PI, a gente tem um alterar consulta de órgão para réu liberto, incluindo RG do réu, informado pelo representante. Aqui bem parecido com o que é feito no app. Quando a gente for consultar os órgãos, a gente vai ver se a pessoa se é um ID pessoa, ou seja, se a pessoa é o próprio real ou se o representante informou qual é o RG do R. é baseado nesse RG. Essa consulta de órgão de real liberto, ela olha pro pro número antes do dígito do verificador. Então é importante e é vital ter o RG, na verdade. E aí a gente vai poder aceitar esses dois caminhos, seja pelo ID pessoa com RG, ou seja pelo número próprio do RG ali digitado pelo representante.

### 00:12:49

**Emerson Yamamoto:** Depois a gente tem a 10690, alterar encaminhamento armazenando RG do Real Liberto. E aí aqui é basicamente para armazenar esse RG mesmo, porque hoje a gente armazena um FK pessoa da pessoa presa, eh, ou coloca na observação informações ali sobre a pessoa presa, o RG e tal. E agora a gente vai ter um campo novo para isso, para ter só o RG. Então vai ser um campo dedicado para essa informação. Eh, inclusive depois a gente até pode mostrar que houve um houve uns casos onde a gente teve uma certa divergência ali, porque se você informa um RG diferente, acaba que o RG que aparece no encaminhamento é um, mas a pessoa presa às vezes é outro. A gente chegou a simular esse esse caso, depois a gente pode tentar mostrar. Eh, como é que ficou? Depois a gente tem a 107. Alterar consulta de processo, verificando o tipo da parte informada. Eh, essa aqui eu não lembro como é que é essa daqui. Deixa eu ver aqui rapidinho que eu não não lembro dessa.

### 00:14:09

**Emerson Yamamoto:** Ah, tá, lembrei. Você vai passar um ID pessoa aqui agora paraa consulta de processo. Você pode passar, né? É um parâmetro opcional. E a partir dessa consulta, a gente vai verificar se essa pessoa é parte ou não no processo. Se ela for parte, a gente vai retornar qual é o tipo de parte, autor, é, o ou outro. E se ela não for parte, a gente simplesmente não retorna, porque significa que não tem essa informação. Beleza? E por último, a gente tem uma que é da API. Na verdade, ela não é não é Integra e nem app. Ela é um encaminhamento, eh, ela é um método que é chamado pelo próprio verde, que é, se eu não me engano, quando a gente cadastra uma interrupção no atendimento, alguma coisa. Yeah. Assim, a gente precisa fazer um encaminhamento comum e mandar um e-mail por Ah, não, se eu não me engano, essa daqui é, deixa eu ver aqui, deixa eu lembrar se essa é do não resposta. Essa é a falta de resposta, se eu não me engano.

### 00:15:14

**Emerson Yamamoto:** É, ó, ressaltamos que a Defensoria Pública não nessa parte aqui não. Cadê? Solicitamos que comp eh considerando que não houve resposta da sua solicitação, essa daqui, na verdade, é quando é uma é um e-mail enviado pela rotina, quando acho que fica 30 dias sem responder no app. Eu confundi esse essa outra que eu falei é outra coisa, mas essa daqui é uma rotina que manda esse encaminhamento comum. Eh, e aí a gente vai colocar um modelo de e-mail específico, porque o modelo de e-mail que a gente tava usando, ele era compartilhado com outros encaminhamentos. Eh, então aqui a gente vai conseguir ser bem mais específico, né, nesse nesse e-mail. É uma I que é um end point que é usada só pela rotina mesmo, então ela não é usada nem pelo aplicativo e nem pela Integra, beleza? E aí o encaminhamento vai ser gerado normal. Já existe essa regra, uma regra até bem antiga aqui, 5295. Beleza? E essa é a última. Esse end point aqui da verde API. Então são essas nove IFs.

### 00:16:20

**Emerson Yamamoto:** A gente vai começar aqui pela parte do app. Eu não sei, Felipe, eu acho, eu acho que tudo importa aqui para você hoje, então não sei se vai dar para sair antes,

**Felipe Martins Costa Brito:** Não.

**Emerson Yamamoto:** mas você que sabe. Se você achar que depois do app não precisa mais,

**Felipe Martins Costa Brito:** Beleza.

**Emerson Yamamoto:** beleza? Mas eu acho que aqui tudo é importante. É isso. Então vou passar pro pessoal. Quem vai começar é o é o Gabriel e depois a gente passa pro pro mall, o mall do CDA do Verde agora tá aqui no cidadão, nosso o nosso nômade digital. Vai lá, Gabriel. Yeah.

**Gabriel Távora:** Boa tarde a todos. Eu vou apresentar a 10.43 alterar encaminhamento para solicitar preferência de atendimento apenas houver pauta remota ou contato publicável do órgão. Então essa iso tem dois critérios. Eh, são dois critérios iguais. A única diferença é em qual fluxo ele se aplica, né? Eh, basicamente, se o órgão possuir alta remota ou contatos publicáveis, a gente mostra a preferência de atendimento nos fluxos de de encaminhamento.

### 00:17:42

**Gabriel Távora:** Se não tiver um dos dois, a gente só exibe a opção de atendimento presencial. Então, o primeiro critério, ele ele fala do fluxo de primeiro atendimento e o segundo ele fala dos demais fluxos. Eh, é uma aparente. simples, né? A dificuldade é a quantidade de de lugares que a gente tem que alterar. A gente aqui nesse segundo critério, a gente tem o fluxo de violência doméstica, eh o atendimento prisional, eh ré liberto, eh buscar processo e receber uma intimação. Então vou começar pelo fluxo de primeiro atendimento. Eh, eu vou mostrar só o fluxo em que não aparece o o órgão para atendimento remoto. Eu tenho aqui um exemplo do da DPU. DP Única de Italva e Cardoso Moreira. Esse órgão não tem não tem balta remota, ele até tem pouco contatos publicados aqui. Mas então quando eu fizer um atendimento de plano de saúde negativo em realizar exames, é um encaminhamento de urgência, a gente não vai ver esse órgão na lista. Procurar aqui plano de saúde. Plano de saúde negativo em realizar exames.

### 00:19:19

**Gabriel Távora:** Tô no município de Taua, ele mostra o órgão, DP Única Digitalva e de Cardoso Moreira. Aqui nessa opção, antes a gente tinha atendimento presencial e atendimento remoto. Eu preferi deixar essa tela para deixar claro pro usuário que ele vai seguir para um atendimento presencial. Se vocês preferirem, a gente pode pular direto, mas aí quando eu clicar em atendimento presencial, ele vai seguindo o fluxo. Encaminhamento, fez um encaminhamento presencial. Eh, o endereço em branco.

**Emerson Yamamoto:** Só falta o endereço, né? É,

**Gabriel Távora:** É, provavelmente ele ele não tá com endereço cadastrado aqui.

**Emerson Yamamoto:** mas e esse endereço aí? Ah,

**Gabriel Távora:** Depois eu vou ter que verificar por

**Emerson Yamamoto:** vou anotar aqui. É porque eu acho que nem tem como não ter endereço. Não deveria, pelo menos, né? Vou anotar aqui como bang.

**Gabriel Távora:** endereço. Não. Ah, veio sim. né? Vou investigar depois porque que não tá most

**Emerson Yamamoto:** Beleza. Да.

**Gabriel Távora:** eh o encaminhamento, o encaminhamento no primeiro atendimento é basicamente isso.

### 00:20:51

**Gabriel Távora:** Eh, agora a gente precisa ver o fluxo de violência doméstica. começar aqui. Eh, violência doméstica contra a mulher. Vou mostrar aqui o esse órgão que é a primeira DP de Rio Bonito. Esse órgão não tem dados de contato ou tem? Sim. Então acho que ele não tem pauta remota. Ah, não, perdão. Esse é o esse é o caso que vai aparecer aqui. Eh, o atendimento remoto. Vou mostrar que é o município de Rio Bonito. Esse aqui ele vai deixar eu continuar com atendimento remoto. Eh, o fluxo de violência doméstica era um pouco diferente. o a seleção de atendimento presencial remoto acontece aqui no no início.

**Emerson Yamamoto:** Ah, é verdade.

**Gabriel Távora:** Não.

**Emerson Yamamoto:** Esse é aquele fluxo que a gente tentou modificar menos possível, né, Gabriel? Porque a pergunta é antes. Aí tem isso, Felipe. Essa pergunta nesse fluxo de violência doméstica, ela vinha antes de tudo, na real, antes até da gente escolher o o órgão. Aí a gente tentou fazer uma solução mantendo esse fluxo, mas talvez se vocês acharem melhor a gente pode redesenhar.

### 00:22:50

**Emerson Yamamoto:** Só vai dar um pouco mais de trabalho porque teria que passar essa seleção lá para depois da seleção do

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** órgão,

**Felipe Martins Costa Brito:** mas eu acho que não vai ter jeito de fugir disso não, hein?

**Emerson Yamamoto:** tá? Deixa só o Gabriel mostrar como é que ficou, mas se não for, a gente reordena isso aí, não tem problema não. M.

**Gabriel Távora:** Beleza. Esse esse órgão é a primeira petição Fideles, não tem dados de contato, até tem uma pauta remota, mas ele não vai permitir eu continuar o agendamento. Tem o órgão aqui. Caminhamento de urgência. Opa.

**Emerson Yamamoto:** Não, ele deixou aí,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** mas não é São Fideles, é outro órgão, por isso que deixou. Não tá errado não, Gabriel. Deu certo. É porque esse órgão aí tá em todo estado.

**Gabriel Távora:** Ah, é verdade. Porque quando eu fiz os testes, esse órgão não tava aparecendo. né, por algum motivo ele passou a aparecer na lista.

### 00:24:01

**Gabriel Távora:** Se se não tivesse, né, um órgão na lista, aí sim ele apare aí ele sim mostraria o erro de que não tem atendimento remoto disponível. Eu ia perguntar se eu queria fazer a bucha para atendimento prisional,

**Emerson Yamamoto:** presencial.

**Gabriel Távora:** é, presencial, perdão. Agora eu tô sem exemplo aqui para mostrar para vocês.

**Emerson Yamamoto:** Ele, se ele vai aparecer para tudo, não vai ter exemplo,

**Felipe Martins Costa Brito:** Não, não.

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** Eu acho que tá certo. Mas aí é aquilo, vai ter que jogar para trás mesmo.

**Emerson Yamamoto:** Tá pra frente, né?

**Felipe Martins Costa Brito:** Paraa frente.

**Emerson Yamamoto:** Tá, tá. Vamos alterar. Eh, eu só acho que isso vai perder a compatibilidade com apps antigos, né, Gabriel?

**Gabriel Távora:** Vai sim.

**Felipe Martins Costa Brito:** Mas eh não tu vê algum prejuízo de de atendimento? Não vejo nenhum.

**Emerson Yamamoto:** Não, eu acho que o fluxo só foi desenhado dessa forma e a gente fez assim. Não, não vejo prejuízo, não. Só o prejuízo vai ser que a gente vai ter que assim que o que os apps antigos vão meio que perder a compatibilidade, mas fora isso não vejo prejuízo nenhum, né?

### 00:25:02

**Emerson Yamamoto:** É, vai ficar até igual é nos outros fluxos, né? Eu não sei porque que a gente pensou nisso antes da outra vez.

**Felipe Martins Costa Brito:** Também não vou me lembrar. Eh, a gente consegue, acho que já te perguntei isso uma vez, acho que você disse que não, a gente não, se a pessoa for optar por esse fluxo, a gente pedir para ele atualizar,

**Emerson Yamamoto:** Não, a gente só a gente já pede para atualizar assim que ele abre o app. Assim, assim que ele abre o app numa versão antiga,

**Felipe Martins Costa Brito:** a gente já pede.

**Emerson Yamamoto:** a gente já fala já.

**Felipe Martins Costa Brito:** Então, então é isso. Então não vejo problema não.

**Emerson Yamamoto:** Tá? Então vou colocar aqui pra gente mover, Gabriel. E aí a gente vai ter que jogar essa opção lá para depois de de selecionar o órgão. É porque o que a gente faz ali é já mostrar se é se é encaminhamento remoto, tá? Tá, a gente vai ter que vai ter que ver como fazer para ficar igual o encaminhamento do primeiro atendimento.

### 00:25:52

**Emerson Yamamoto:** Eu não sei agora muito bem como é que isso é feito no app, mas é porque no app ele já mostra remoto ou já mostra presencial. a gente teria que fazer igual é no primeiro atendimento. Tô pensando aqui, é, de qualquer forma, como é encaminhamento, eu sempre posso encaminhar remoto presencial, né? Tá, vou anotar aqui. Eh, mover a seleção. É porque eu realmente não tô lembrando porque a gente jogou isso para antes. Provavelmente tem um motivo. Preferência de atendimento para

**Felipe Martins Costa Brito:** Eu acho que aqui não não tinha nos outros. A gente botou nesse e os outros não tinham a pergunta. Depois que a gente botou nos outros.

**Emerson Yamamoto:** ser. Eu não sei se isso mudava alguma coisa na nas opções que que vinham depois,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** não,

**Felipe Martins Costa Brito:** não,

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** não, não. M.

**Emerson Yamamoto:** Tá bom. OK.

**Gabriel Távora:** Eh, vou mostrar o atendimento prisional agora.

### 00:26:59

**Gabriel Távora:** pessoa presa.

**Emerson Yamamoto:** Vai ter que alterar a PI, né, Gabriel, né? Nesse fluxo novo, né? Vai ter que alterar bastante, eu acho, porque acho que os retornos ali vão ter que mudar, não vai vir mais remoto e tal, vai vir só os órgãos,

**Gabriel Távora:** Sim.

**Emerson Yamamoto:** tá? Beleza?

**Gabriel Távora:** Eh, colocar aqui um RG que vai trazer a 17ª DP de defesa da pessoa presa que não tem contatos publicáveis. Eh, esse aqui tem o mesmo a mesma a o mesmo esse mesmo detalhe do da violência doméstica. Eh, eu tentei interferir menos o mínimo possível no fluxo. Então, se eu clicar em atendimento remoto, ele até vai mostrar que ele vai até mostrar o atendimento, mas aparece o erro que no momento não atendimento remoto disponível. Gostaria de buscar atendimento presencial? Se eu clicar em sim, ele vai seguir com atendimento presencial. Se eu clicar em não, ele vai simplesmente parar, né? Porque não tem atendimento remoto.

**Emerson Yamamoto:** Ah, que você acha? acha que tem que mudar também, Felipe?

### 00:28:51

**Felipe Martins Costa Brito:** Também acho.

**Emerson Yamamoto:** Mesma coisa.

**Felipe Martins Costa Brito:** É, também acho. A gente tem que espadroniza e fica, não precisa ter esse, erro,

**Emerson Yamamoto:** Uhum.

**Felipe Martins Costa Brito:** né?

**Emerson Yamamoto:** Tá. É, isso vai dar mais trabalho do que a gente tava imaginando. Então, acho que na hora de abrir sprint a gente vai ter que vai ter que considerar desse trabalho, porque é meio que como a gente tava pensando só em tentar manter ao máximo como funciona hoje, quando a gente joga isso pra frente muda bastante o que a PI faz e o que o precisa receber. Então, vai ter um impactozinho aí. Mas beleza, vou anotar aqui também.

**Gabriel Távora:** Por último fluxo de ré liberto. Deixa eu só pegar um RG aqui. Aqui é a mesma lógica. Não, atendimento remoto disponível. Gostaria de buscar atendimento presencial. Clicando assim, ele direciona para DP eh como encaminhamento presencial. Então, provavelmente a gente vai ter que fazer alteração nesse fluxo também.

**Felipe Martins Costa Brito:** Ja.

### 00:30:23

**Emerson Yamamoto:** Beleza. Anotei aqui também. Uma

**Gabriel Távora:** Beleza? São esses fluxos. Eh, se vocês quiserem fazer mais algum teste, M.

**Emerson Yamamoto:** dúvida que eu fiquei, Felipe, é é como é que isso se comporta no plantão, porque plantão acho que os órgãos de plantão nunca t pauta, né?

**Felipe Martins Costa Brito:** Não tem, não tem pauta, mas tem canal remoto.

**Emerson Yamamoto:** Ah, então para plantão a gente teria que ver também se ele tem o canal remoto,

**Felipe Martins Costa Brito:** É para plantão.

**Emerson Yamamoto:** tá?

**Felipe Martins Costa Brito:** E aí é como a gente tá nas proximidades pro recesso, né?

**Emerson Yamamoto:** no recesso também, né?

**Felipe Martins Costa Brito:** É. É, não sei se muda alguma coisa ou não. Não sei. Acho que não, né?

**Emerson Yamamoto:** Não sei. A gente vai ter que dar uma olhada também.

**Felipe Martins Costa Brito:** Porque eu testei recesso nesse feriadão passado. Eu te falei, Emerson.

**Emerson Yamamoto:** Não.

**Felipe Martins Costa Brito:** Então, não teve um feriadão aí passado eh do

### 00:31:18

**Emerson Yamamoto:** Sim. foi do defend eh, feriado do servidor público.

**Felipe Martins Costa Brito:** servidor com finados.

**Emerson Yamamoto:** Uhum.

**Felipe Martins Costa Brito:** Isso aí a gente testou tanto a API lá do do chatbot quanto o app. Tudo funcionou conforme esperado, então acho que a gente não vai ter problemas esse ano não.

**Emerson Yamamoto:** Ah, que bom. Tá. Eh, tá. Eu coloquei aqui eh aplicar também para os casos de plantão em recesso, que eu tudo isso é no fluxo de primeiro atendimento, né? Pode ser que vá funcionar, mas é bom a gente conferir porque eu acho que você não fez esse teste, né, Gabriel? Nem eu fiz na interna, eu acabei não fazendo esse teste. A gente vai ter que verificar se no plantão e no recesso, é porque eu sei que o plantão e recesso eles têm um fluxo diferente na API, apesar do fluxo aqui não é ser o mesmo, mas tem bastante decisão diferente na API. Eh, então eu acho que vai gerar alteração também. Eu acho que eu gerou essa confusão porque tem alguma isa que o plantão em recesso não alguma outra isa que a gente fez que não se aplica ao plantão em recesso.

### 00:32:32

**Emerson Yamamoto:** Mas beleza, anotei aqui. E então essa eixo ela tá com dois refinamentos pesadinhos aí, que é a gente mudar essa ordem e jogar essa ordem para depois e aplicar isso para plantão em recesso. OK. Beleza, Gabriel. Então, vamos ter que trabalhar mais nela. Eh, então vou passar agora pro pro MOL. Mol vai mostrar a questão do IFEN e a parte ali do movimento de pauta interna, de agendamento de pauta interna aparecendo quando não é visível no app.

**Lucas de Oliveira Mol Silva:** Boa tarde, pessoal. Vou partilhar a tela aqui e vocês me confirmam, por favor, se vocês vão conseguir ver. Sim,

**Yann Naylor Francisco:** tá movendo a planilha e o e o aplicativo aí do lado.

**Emerson Yamamoto:** Dá para ver sim.

**Lucas de Oliveira Mol Silva:** perfeito. Yann, valeu. Então, como o Emerson falou, eu vou apresentar essa tarefa aqui e essa primeiro vou começar por essa de altera alterar visualização do caso ocultando andamento de agendamento de pauta interna configurado como não visível no app.

### 00:33:55

**Lucas de Oliveira Mol Silva:** Basicamente a ideia é que acessaram um caso, a gente não deve mostrar os andamentos, né, que tiverem um agendamento por pauta interna que a gente marcar como não visível quando a gente cria esse esse agendamento lá no no verde. Então eu vou criar um exemplo para esse usuário que eu já tô logado de um agendamento. Vou criar dois, na verdade, eu vou criar um exemplo visível e outro não visível e a gente vai ver o comportamento lá no aplicativo. Ah, esses aqui já estão passados que eu tinha testado antes. Eu vou criar um agora. Certo. Vou selecionar uma pauta interna. O que importa aqui é marcar como que o agendamento não deve ser exibido, né? Ou aqui no caso exibido, ele vai exibir. Então no aqui vou botar uma data qualquer aqui. Dia 18, então vai ser um que vai ser exibido, deve aparecer lá.

### 00:35:08

**Lucas de Oliveira Mol Silva:** Legal. Deixa eu abrir aqui. Beleza. Esse é visível no app. Fazer a mesma coisa, só que agora não visível. Pá, agora não visível. Aliás, vou botar uma data diferente também pra gente saber. Legal. Vamos abrir então. O dia 19 não deve aparecer no app e o de dia do dia 18 deve aparecer. Aqui eu posso nos meus agendamentos também tá refletindo lá, mas eu vou a ISO em si tá comentando sobre ao acessar um caso, né? Então eu vou acessar o caso desse processo que termina com 05. Esse aqui, pena privativa de liberdade. E aqui a gente vê os andamentos, só tem um aparecendo que é o do dia 18 às 10 horas. Esse aqui que é visível no app. O outro não tá aparecendo aqui.

### 00:36:32

**Lucas de Oliveira Mol Silva:** A gente consegue confirmar isso também no agendamento aqui, nos meus agendamentos. Eh, esse aqui tá carregando de antes. Deixa eu recarregar a tela. Foi. Aí, esse aqui só tá aparecendo também do dia 18. Eu posso editar aqui também na prática, a partir do momento que eu editar aqui e marcar para ser visível e atualizar no app, deve aparecer também. Show. Vai recarregar aqui. Aí passou a aparecer o do dia 19. Vamos ver lá no caso também. Mesma coisa.

**Emerson Yamamoto:** Beleza. É isso. É isso, né, Felipe?

**Lucas de Oliveira Mol Silva:** Show.

**Emerson Yamamoto:** Maravilha. Então, a gente vai para 10682 agora, né, irmão?

**Lucas de Oliveira Mol Silva:** Isso aí. Vou para essa aqui que é para alterar,

**Emerson Yamamoto:** Eu

**Lucas de Oliveira Mol Silva:** para permitir cadastrar um usuário permitindo o IFEN. Eh, é bem simples essa tarefa, mas a ideia dela também foi da gente permitir adicionar o ifen e a apóstrofe simples, né?

### 00:38:03

**Lucas de Oliveira Mol Silva:** Aqui na iso não comenta em si, mas em algum momento acho que foi acordado isso, né?

**Emerson Yamamoto:** acho que o apóstrofo já deixava.

**Felipe Martins Costa Brito:** Não,

**Lucas de Oliveira Mol Silva:** É.

**Felipe Martins Costa Brito:** alguma coisa mais você falou comigo,

**Emerson Yamamoto:** É o eu falei do assento agudo, né, que você queria colocar, mas que não era recomendado. E aí você tinha falado assim: "Ah, tem como liberar o acento agudo?" Porque o pessoal confunde apóstrofo com acento agudo?

**Felipe Martins Costa Brito:** foi isso, foi isso, foi isso.

**Emerson Yamamoto:** Aí eu falei: "E não era muito bom porque poderia dar problema em outras coisas". Aí você falou: "Então libera o IFEN porque o IFEN não funciona". Aí a gente liberou o IFEN, mas o apóstrofo já funcionava assim.

**Lucas de Oliveira Mol Silva:** Então, então foi mais ou ou do IF mesmo. A partir dessa tela já bloquearia, mas eu vou colocar o nome aqui. Eh, Falando assento, eu botei quase acento ali. Vou botar de novo Santana, só pra gente ver que não tá bloqueando.

### 00:39:11

**Lucas de Oliveira Mol Silva:** Tem tanto no nome como no sobrenome, né? Eh, aquela fase já bloquearia, mas eu vou seguir o fluxo só pra gente finalizar a criação de um de um de um usuário e ver que vai criar com sucesso. O nome ficou com Não,

**Emerson Yamamoto:** Faltou o IF,

**Lucas de Oliveira Mol Silva:** faltou o ifen,

**Emerson Yamamoto:** pô.

**Lucas de Oliveira Mol Silva:** pô. Eu botei o exemplo da aposta simples, perdão. Ah, não sei. Vou botar qualquer, sei lá. Tá, agora sim. Com if hein.

**Emerson Yamamoto:** Bota lá o antes de tu criar, volta lá,

**Lucas de Oliveira Mol Silva:** Uhum.

**Emerson Yamamoto:** bota o assento agudo só pra gente ver que ele que ele não vai deixar.

**Lucas de Oliveira Mol Silva:** O assento agudo em qualquer lugar.

**Emerson Yamamoto:** Tu consegue?

**Lucas de Oliveira Mol Silva:** Uhum. Esse aqui apóstrof que acento já não deixaria aqui não. Isso não.

### 00:40:35

**Emerson Yamamoto:** É,

**Lucas de Oliveira Mol Silva:** O agudo o ass,

**Emerson Yamamoto:** ele já bloquei. Não é agudo, não. É esse aí mesmo. É o é o cras.

**Lucas de Oliveira Mol Silva:** né?

**Emerson Yamamoto:** É

**Lucas de Oliveira Mol Silva:** É o Cras já bloqueia aqui. Aqui também não deixaria passar.

**Emerson Yamamoto:** isso aí. Mas o botão ficou ativado. Se tu apertar o botão, o que que acontece?

**Lucas de Oliveira Mol Silva:** Bora testar.

**Emerson Yamamoto:** Ah, ele não deixa,

**Lucas de Oliveira Mol Silva:** Só não deixa passar mesmo.

**Emerson Yamamoto:** tá?

**Lucas de Oliveira Mol Silva:** Já com o a Post Sim deixou, mas como a gente falou, talvez já deixava antes, né?

**Emerson Yamamoto:** Mhm.

**Lucas de Oliveira Mol Silva:** Certo. Pode seguir algum teste a mais. Querem fazer algum teste a mais no nome?

**Emerson Yamamoto:** Acho que não,

**Felipe Martins Costa Brito:** Não.

**Emerson Yamamoto:** né?

**Lucas de Oliveira Mol Silva:** Tá. Certo? Para tela inicial, a gente já tá com usuário criado.

### 00:41:52

**Emerson Yamamoto:** Show.

**Lucas de Oliveira Mol Silva:** Não consigo ver os detalhes,

**Emerson Yamamoto:** Угуm.

**Lucas de Oliveira Mol Silva:** mas que ainda não verificou, né? Yeah.

**Emerson Yamamoto:** Beleza, é isso. Valeu, ma.

**Lucas de Oliveira Mol Silva:** É isso. Valeu,

**Emerson Yamamoto:** Agora,

**Lucas de Oliveira Mol Silva:** pessoal. M.

**Emerson Yamamoto:** agora a gente vai fechar o app com mais duas do Leonardo de Melo aí. Leonardo de Melo com Marcos que é 10689, 10626. Fluxo de ré liberto, verificando se assistido é o próprio réu e alterar encaminhamento para reaproveitar ou criar caso.

**Leonardo de Melo:** Boa tarde, pessoal. Vou compartilhar aqui. Eh, então, a primeira que eu vou apresentar aqui é essa aqui de alterar fluxo de R liberto, verificando se assistido é o próprio réu ou representante. Então, eh, deve ser verificado no processo seu se o assistido logado faz parte como réo, eh, como uma parte do processo. E se não for possível identificar, eh, deve ser solicitada confirmação de você é parte réo para o assistido poder informar.

### 00:43:13

**Leonardo de Melo:** E aí com as duas opções de sim, sou o R e não sou representante. E aí quando o assistido seleciona que ele é o R, a gente tenta pegar o RG do cadastro e se não tiver a gente tem que pedir pro assistido informar esse RG que vai também atualizar o cadastro do assistido. Quando é representante, ele vai informar o RG do R e vai prosseguir o fluxo normalmente, eh, mas sem salvar na observação e sem vincular a pessoa presa ao encaminhamento. Vai salvar, vai regir um novo campo que nós fizemos. Eh, e aí é isso. Então, vou pegar aqui um processo. Eu tô aqui com um roteiro montado. Pegar esse processo aqui, um processo seu. Esse daqui, eh, um probleminha que a gente tava tendo é que a gente não sabe por, mas essa versão não tá conseguindo recuperar as partes do processo de forma frequente. Isso é algo que a gente ainda vai investigar. Então, eu coloquei algumas partes aqui para retornar em outros processos, né?

### 00:44:34

**Leonardo de Melo:** Acho que esse aqui do prisional não tem, mas na outra na outra tarefa vai ter isso. Eh, e aí como ele não consegue recuperar as partes, ele vai perguntar aqui se direto se faz parte como réo. É, então, primeiro esse aviso se o réu encontra-se preso aqui, não, pra gente poder seguir como réu liberto. E aqui ele faz essa pergunta, né, que tá aqui na ISO. Eh, aqui clicando em Sim, sou R, ele vai pegar do cadastro RG. E aí a gente pode prosseguir pro atendimento. Então, atendimento inicial, por exemplo, que DP execuções penais. Aqui é o RG do assistido. Então a gente pode até bater aqui 3 com que tá aqui, ó. aqui esse RG aqui já estava nesse assistido. Deixa eu até pegar aqui o encaminhamento para poder mostrar esse D aqui. Aqui então Leonor Soares RG do assistido como como ele é o ré, né? Aí eu vou fazer o seguinte, eu vou tirar o RG do assistido.

### 00:46:00

**Leonardo de Melo:** Então vou pegar aqui pelo banco e tirar esse RG e vou entrar aqui novamente pra gente ver que o assedo está sem R. Então, quando ele for por esse fluxo novamente, ele deve solicitar.

**Emerson Yamamoto:** Sem RG, né?

**Leonardo de Melo:** Oi,

**Emerson Yamamoto:** Sem RG. Porque tu falou R.

**Leonardo de Melo:** isso é CRG. Ele tem que solicitar o RG novamente. até pegar aqui o regi aleatório aqui. Não se encontra preso e sim, sou o R. Agora ele pede pelo RG. Eh, e aí quando a gente avança, ele vai salvar esse RG no cadastro do assistido. Bom, a gente, se a gente verificar aqui novamente meus dados, vai tá aqui o RG que a gente informou, né? exatamente como tá aqui. E a último fluxo dessa tarefa é o de representante. Eh, vou seguir pelo mesmo processo. Quando a gente

**Emerson Yamamoto:** Acho que uma coisa que a gente não fez aí, Léo, foi armazenar o RG no campo separado, mas é porque isso a gente descobriu um pouco em cima da hora, né?

### 00:47:57

**Leonardo de Melo:** não, eu já tô consegu Faz,

**Emerson Yamamoto:** já tá salvando. Não, mas não tá exibindo no verde ainda, então, né? Que aí tem que alterar o verde, no caso, né?

**Leonardo de Melo:** Isso é exatamente.

**Emerson Yamamoto:** OK.

**Leonardo de Melo:** É, inclusive isso era uma dúvida que eu tava aqui ele diz para salvar só no caso de ser representante,

**Emerson Yamamoto:** Uhum.

**Leonardo de Melo:** né? Eh,

**Emerson Yamamoto:** Uhum.

**Leonardo de Melo:** este dado deve ser mencionado em Campo Novo. Eh, seria isso mesmo? Quando ele é o réu não não salva nesse campo

**Emerson Yamamoto:** Eu acho que tem tem que sempre salvar,

**Leonardo de Melo:** novo?

**Emerson Yamamoto:** né? Porque tô entendendo que eles vão sempre olhar desse campo, né?

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** Não sei.

**Leonardo de Melo:** Entendi.

**Felipe Martins Costa Brito:** é isso,

**Leonardo de Melo:** É.

**Felipe Martins Costa Brito:** é isso.

**Thaiana Lima:** Mas não precisa salvar porque já é o próprio cadastro do assistido. A gente não pede um campo a mais se ele for o real.

### 00:48:35

**Felipe Martins Costa Brito:** Mas se Mas se ele no cadastro não tiver RG,

**Thaiana Lima:** Aí a gente pede o RG guardando o campo de RG do cadastro.

**Felipe Martins Costa Brito:** ah, já faz isso hoje,

**Thaiana Lima:** Já faz isso dois hoje a gente já faz até a gente até pergunta

**Felipe Martins Costa Brito:** então tá bom. Yeah.

**Leonardo de Melo:** Eh,

**Thaiana Lima:** e bota no cadastro.

**Leonardo de Melo:** Yes.

**Thaiana Lima:** Só trocou aqui a ordem da pergunta. Só precisa do RG como um campo novo, avulso no encaminhamento se eu for representante, porque eu tenho um segundo RG que é o do R. Yeah.

**Emerson Yamamoto:** Entendi.

**Leonardo de Melo:** Eh, e prosseguindo com o representante, então vou pegar aqui um novo novo RG.

**Emerson Yamamoto:** Mas tem alguma situação, Léo,

**Leonardo de Melo:** Hum.

**Emerson Yamamoto:** que e a gente viu até na interna que gerava um descompasso ali na tela de detalhes do encaminhamento. Eu acho esse esse pessoal, ele não vai no CPEN, ele não busca o RG, não, né? Buusa,

**Leonardo de Melo:** Não, não. Acho que aqui até diz para

### 00:49:39

**Felipe Martins Costa Brito:** Não, em tese não é para ir.

**Thaiana Lima:** Ele vai nesse p se for o próprio cadastro normal,

**Leonardo de Melo:** Não.

**Thaiana Lima:** se for o representante aí não vai. Yeah.

**Felipe Martins Costa Brito:** Vai

**Emerson Yamamoto:** não, o próprio mesmo. É porque eu eu acho que o que gerou o problema foi quando ele vai ao CPEN, ou seja, quando ele é o próprio réu, ele e ele não tem o RG cadastrado na pessoa física, mas ele tem uma pessoa presa associada. Aí você informa o RG. Esse RG que você informa é um que é salvo, mas a pessoa presa que aparece associada ao agendamento é outro com outro RG. Eu não sei se esse caso é possível.

**Felipe Martins Costa Brito:** Ele tem um cadastro dele dissociado do cadastro de pessoa presa dele mesmo.

**Emerson Yamamoto:** Não, ele tem o cadastro da pessoa presa associado à pessoa física, mas por algum motivo alguém pode ter tirado o RG da pessoa física dele.

**Leonardo de Melo:** Что?

**Emerson Yamamoto:** Eu acho que nesse caso,

**Felipe Martins Costa Brito:** Não entendi.

### 00:50:33

**Emerson Yamamoto:** eh, a gente vai pedir o RG,

**Felipe Martins Costa Brito:** Yeah.

**Emerson Yamamoto:** vai salvar, vai aparecer na observação esse RG, mas é porque quer ver, volta lá no verde, Léo, só pra gente mostrar que tem dois lugares onde a gente mostra isso, ó. Tá vendo ali? Pessoa presa, nome e RG. Isso aí vem da da do apenado, da tabela de apenado nos pen. Então, se ele tiver uma pessoa presa associada a pessoa física, vai aparecer ali em pessoa presa. Só que se, no. cadastro de pessoa dele, que é diferente do cadastro de pessoa presa, né? Não tiver o RG mais por algum motivo e eu informar o RG que ele vai aparecer ali em cima na observação, ó, Leonardo de Melo Soares, RG tal, vai ser um e o que vai aparecendo pessoa presa vai ser outro.

**Leonardo de Melo:** Eu

**Emerson Yamamoto:** Aí provavelmente isso vai gerar uma boa confusão, porque você não vai saber qual é o correto. É uma situação de exceção, mas pode gerar problema, né?

**Leonardo de Melo:** acho que eu acho que nesse caso a gente tá pegando direto do assistido.

### 00:51:32

**Leonardo de Melo:** Aí ele pega da pessoa física.

**Emerson Yamamoto:** Então, mas eu tô falando, se não tiver a pessoa física, por exemplo, esse daí, esse daí, esse RG é um RG de pessoa presa mesmo, não, né?

**Leonardo de Melo:** Não, não. Eu peguei uma RG aleatória.

**Emerson Yamamoto:** É, eu vou ver se eu consigo pegar um de pessoa presa, só que aí teria que ir lá na pessoa física e tirar o RG. Mas eu tô falando isso porque o Alexandre fez esse teste e deu o problema.

**ICARO LUIZ ALBAR EDUARDO:** Você tá em homolog?

**Leonardo de Melo:** Mhm.

**Emerson Yamamoto:** Oi. Não, mas pode ser porque manda aí

**ICARO LUIZ ALBAR EDUARDO:** Eu acho, eu acho que eu tenho uns RG aqui que eu tô testando a pessoa presa.

**Emerson Yamamoto:** um então, por favor,

**ICARO LUIZ ALBAR EDUARDO:** Tá, pera aí. Yeah.

**Emerson Yamamoto:** porque se penção, então pode ser qualquer um.

**Thaiana Lima:** Isso então deve acontecer em produção, porque o fluxo de Real Liberto, ele já tem essa pergunta do do RG, caso a pessoa não tenha

**Emerson Yamamoto:** Ah, é, não sabia.

### 00:52:25

**Emerson Yamamoto:** Eu achei que a gente tava implementando isso agora.

**Thaiana Lima:** Não, acho que quando eu tava testando se f escrever aío, eu vi que ele já tinha essa pergunta que eu coloquei que a pergunta só que mudou de lugar.

**Emerson Yamamoto:** Ah,

**Thaiana Lima:** Ele vai vir somente depois da confirmação de ré.

**Emerson Yamamoto:** é, provavelmente não tá dando problema, então, porque não tem ninguém reclamando. Ou eles não, ou esse caso acontece muito pouco, talvez, né? Quer ver, Leonardo? Pega aí um RG desses que o Icaro passou, por favor, aí no chat.

**Leonardo de Melo:** OK.

**Emerson Yamamoto:** É,

**Leonardo de Melo:** Pegar esse aqui.

**Emerson Yamamoto:** busca ele no verde só para ver se Ah, não sei se dá para buscar por RG, né?

**Leonardo de Melo:** É, acho que não. Deixa eu ver.

**Emerson Yamamoto:** Busca ele no app mesmo para ver se a gente acha o nome da pessoa.

**Leonardo de Melo:** Tá.

**Emerson Yamamoto:** Só para ver para para ver pra gente ver se a gente consegue simular esse caso.

**Leonardo de Melo:** É, no caso acho que ele não vai para, deixa eu ver se talvez pelo pessoa presa.

### 00:53:14

**Emerson Yamamoto:** Ah, tá, entendi.

**Leonardo de Melo:** que no fluxo de Riberto ele não verifica o ap nada,

**Emerson Yamamoto:** Ah, entendi.

**Leonardo de Melo:** mas talvez pelo

**Emerson Yamamoto:** É só se for você mesmo, né? É, então não sei não se vai vai ser bem difícil acontecer isso. Enfim, só acho que a gente pode ter um certo problema aí. Aí não sei se talvez é porque a gente tá mostrando RG agora em em três lugares, né? Não, não em três ao mesmo tempo, mas são três lugares possíveis, né? que é na observação, nesse campo novo de RG e na aba de pessoa, na aba não, mas na sessãozinha ali de pessoa presa, que também mostra a pessoa presa e o RG dela. Então, meu medo é só que como tem três lugares diferentes, Então, eh,

**Leonardo de Melo:** Acho que aqui não,

**Emerson Yamamoto:** mas aí por

**Leonardo de Melo:** não era para aparecer isso aqui, né?

**Emerson Yamamoto:** quê?

**Leonardo de Melo:** É por porque eu fui pelo pelo pessoa presa, eu acho. Pera, eu informei que esse essa pessoa se encontra presa.

### 00:54:26

**Emerson Yamamoto:** Não entendia se ela tá presa ou

**Leonardo de Melo:** É que aparece o modal aqui de É.

**Emerson Yamamoto:** solta.

**Leonardo de Melo:** Aí esse aqui só é pro R liberto,

**Emerson Yamamoto:** Ah, tá sim.

**Leonardo de Melo:** né? E talvez isso entre como refinamento. Aí aqui, ó, o ré desse processo encontra-se preso.

**Emerson Yamamoto:** Mas tá certo, não tá não.

**Leonardo de Melo:** Eh, então,

**Emerson Yamamoto:** Se tu botar assim,

**Leonardo de Melo:** mas clicando em sim,

**Emerson Yamamoto:** ele aí ele vai pro fluxo de pessoa presa. É outro fluxo.

**Leonardo de Melo:** sim. E aí ele tinha aparecido aqui.

**Emerson Yamamoto:** Ah, ele apareceu nesse fluxo de pessoa presa também. Acho que não, né? Só no real.

**Thaiana Lima:** Esse RG aí é de uma pessoa solta de verdade. Pessoa presa é real.

**Emerson Yamamoto:** Presa, solta.

**Thaiana Lima:** É isso. Só presa da solta.

**Leonardo de Melo:** É,

**Thaiana Lima:** Então porque ele redireciona,

**Leonardo de Melo:** deixa eu ver aqui.

**Thaiana Lima:** ele redirecionou de um fluxo pro outro.

**Emerson Yamamoto:** Ah, tá.

### 00:55:14

**Thaiana Lima:** Quando ele verificou que o processo é seu e a pessoa desse RG foi encontrada no CPEN com liberto, foragido tal, ele joga pro real liberto,

**Emerson Yamamoto:** Hum.

**Leonardo de Melo:** Não faz sentido.

**Thaiana Lima:** entendeu?

**Emerson Yamamoto:** Pode ser.

**Thaiana Lima:** Aí você saiu do do fluxo de pessoa presa e voltou pro Roberto.

**Emerson Yamamoto:** Mas isso teria que ver no banco de produção, meu bando.

**Leonardo de Melo:** É, é. Ele tá como libertado aqui.

**Emerson Yamamoto:** Tá como libertado. Ah,

**Leonardo de Melo:** É.

**Emerson Yamamoto:** então pode ser isso.

**Leonardo de Melo:** Então é,

**Emerson Yamamoto:** Pode ser isso.

**Leonardo de Melo:** nossa, nem sabia desse desse fluxo. Ele redireciona, então

**Emerson Yamamoto:** Mas aí se tu botar que tu é o réu, já é já não faz sentido, né? Porque você não é essa pessoa,

**Leonardo de Melo:** é verdade,

**Emerson Yamamoto:** né?

**Leonardo de Melo:** ó.

**Emerson Yamamoto:** A gente não tem essa verificação, né, Taiana, para se dizer que é o ré bater com cadastro da pessoa do aplicativo, né?

**Thaiana Lima:** Se disser que é o réu, não,

### 00:56:09

**Emerson Yamamoto:** É.

**Thaiana Lima:** porque a gente só pergunta se ele é o réu se eu não conseguir encontrar ele no processo, né?

**Emerson Yamamoto:** Uhum. Mas pensa nesse caso, por exemplo, o Leonardo botou um RG qualquer, a pessoa tá solta, mandou pro fluxo de pessoa liberta,

**Thaiana Lima:** Uhum.

**Emerson Yamamoto:** pessoa em liberdade, que nesse fluxo até mudou. E aí ele colocou lá que é o réu, só que nitidamente ele não é o réu porque a pessoa dele do aplicativo é outra, né? Se bem que a não tem como saber, né? Não,

**Thaiana Lima:** É,

**Emerson Yamamoto:** até tem.

**Thaiana Lima:** vai depender se os dois vão ter RG cadastrado.

**Felipe Martins Costa Brito:** Não, ele pode ser real.

**Thaiana Lima:** Ah.

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** Eh,

**Felipe Martins Costa Brito:** ele pode ser real.

**Emerson Yamamoto:** oi.

**Felipe Martins Costa Brito:** Ele pode ser real.

**Emerson Yamamoto:** Não, não, ele pode ser ré, Felipe. Mas eu tô falando assim, imagina que esse cadastro é do Leonardo e o RG que ele colocou é de outro cara, que esse cara que ele viu aí no banco.

### 00:56:53

**Emerson Yamamoto:** Quando ele buscou e a gente identificou que ele é libertado, mandou pro fluxo de réu liberto. Aí ele pergunta: "Ó, você é a parte réu?" Se ele colocar que é o réu, a gente tem como saber que não é, né? Porque a pessoa do aplicativo é uma e a pessoa que tá na na pessoa presa é porque eu não sei se a gente sempre acha uma pessoa presa, né?

**Felipe Martins Costa Brito:** Acho ele pode estar representando a pessoa presa.

**Emerson Yamamoto:** Mas aí ele é o representante, não o réu, né?

**Felipe Martins Costa Brito:** Ah,

**Emerson Yamamoto:** Entendeu o que eu tô falando?

**Felipe Martins Costa Brito:** mas ele vai botar e mas a chance dele botar errada existe, né?

**Emerson Yamamoto:** Sim, sim. Só tô falando, bom, só tô falando que tem essa brecha, mas vai lá, segue aí, Léo. Bota aqui é o réu. O teu tá com RG no no cadastro.

**Leonardo de Melo:** Eh Sim, sim. Tá, sim.

**Emerson Yamamoto:** Tira lá para ver se ele vai se a gente vai conseguir chegar nesse caso.

### 00:57:35

**Leonardo de Melo:** Eh, eu queria ver na real como que ficaria o encaminhamento, se tipo vai ficar o RG do que eu me informei.

**Emerson Yamamoto:** Ah, tá. Então vai, segue aí, vê aí o que que vai acontecer. Então,

**Leonardo de Melo:** Deixa eu ver aqui,

**Emerson Yamamoto:** também não sei não.

**Leonardo de Melo:** ó. É esse F que eu não, eu não tinha visto aqui, ó.

**Emerson Yamamoto:** Ó, tá vendo, Margarete?

**Leonardo de Melo:** Ele pegou.

**Emerson Yamamoto:** Já deu outra pessoa. Exatamente.

**Leonardo de Melo:** É.

**Emerson Yamamoto:** E vai dar ruim isso aí. Vai ficar o teu RG num campo e o RG dele no outro.

**Leonardo de Melo:** Vamos ver.

**Emerson Yamamoto:** Porque ele pegou da pessoa, sei lá.

**Leonardo de Melo:** Eh, dá até deixar nossa tela pra gente poder comparar. Eu acho que é esse aqui, né? Deixa eu pegar aqui pelo banco. Mais recente, só para ter certeza. É esse aqui. Final quatro.

**Emerson Yamamoto:** Ó,

**Leonardo de Melo:** É,

**Emerson Yamamoto:** já deu ruim.

### 00:58:25

**Leonardo de Melo:** ficou

**Emerson Yamamoto:** E aí é bizarro porque ficou o teu nome, o que não faz menor sentido porque não é você essa pessoa presa, né? Margarete Peixoto. Ah, aí deu ruim porque eu Exato.

**Leonardo de Melo:** aqui ficou o RG que foi informado, né? E aqui é o RG do assistido.

**Emerson Yamamoto:** Não faz menor sentido isso aí. Isso aí tá tá totalmente errado.

**Leonardo de Melo:** อ

**Emerson Yamamoto:** Porque esse pessoa presa deveria ser a pessoa presa que ele achou,

**Thaiana Lima:** Mas por que que é que eu acho que a sensação de pessoa presa deve ter

**Emerson Yamamoto:** né?

**Thaiana Lima:** sido reaproveitada do nos liberto não fazia sentido, já que a gente sempre contava que ele era o próprio real,

**Emerson Yamamoto:** Uhum. Mas aí ficaria o quê? na observação.

**Thaiana Lima:** mas a gente criou um campo mais para isso, para Exibiu o RG do do informado do Real Liberto.

**Emerson Yamamoto:** Então agora, mas tô falando antes,

**Thaiana Lima:** Agora era antes era na observação.

**Emerson Yamamoto:** antes disso. Entendi. A gente vai continuar botando na observação também, né, Ta?

### 00:59:21

**Emerson Yamamoto:** Mesmo com campo a mais.

**Thaiana Lima:** Sim, só não vai ter nome porque quando ele é o representante a gente só pede o RG do réu. A gente não pede o nome do réu.

**Emerson Yamamoto:** Ah, tá. Eu não tenho, eu não busco esse RG,

**Leonardo de Melo:** Ah,

**Emerson Yamamoto:** né?

**Leonardo de Melo:** iso aí só tenho que modificar. Eu vou mostrar depois o do representante como é que tá.

**Emerson Yamamoto:** Caraca, deu um nó na minha cabeça.

**Leonardo de Melo:** Mas então,

**Emerson Yamamoto:** É muito campo, é muita, muito fluxo possível. Tá. Vai lá pro pro fluxo de representante,

**Leonardo de Melo:** eh,

**Emerson Yamamoto:** então, Léo.

**Leonardo de Melo:** tá, eu só fiquei em dúvida assim aqui. Então vai ficar o nome do apen. nada, né? Nesse caso.

**Thaiana Lima:** Se ele for o réu, porque se ele for representante, a gente só vai ter a regia da pessoa presa, a regia do réu,

**Leonardo de Melo:** Ah,

**Thaiana Lima:** ré liberto. M.

**Leonardo de Melo:** é, é um fluxo estranho, né?

### 01:00:13

**Leonardo de Melo:** Porque a pessoa informa um RG e depois diz que é o réu. Então não sei. Vou fazer aqui o fluxo de de representante, então.

**Yann Naylor Francisco:** É, eu não não sei se ajuda ou atrapalha. Eh, mas teve um uma homologação que eu tava fazendo aí que na parte de agendamento iria bloquear o próprio réu preso de fazer o agendamento dele, coisa que hoje não é bloqueado. Então, o FK da pessoa ser o mesmo, o ID da pessoa ser o mesmo ID do da pessoa presa, eh, não ia poder prosseguir com esse agendamento. Não sei se isso ajuda ou atrapalha ou não agreer. Não sei se o encaminhamento vai ter esse comportamento também,

**Leonardo de Melo:** Eh,

**Yann Naylor Francisco:** né?

**Leonardo de Melo:** é, nesse caso dessa ISO é o de agendamento, né?

**Yann Naylor Francisco:** O que eu passei foi o agendamento

**Leonardo de Melo:** Ah, sim. É, aí talvez

**Yann Naylor Francisco:** aí nesse fluxo que vocês estão passando, o próprio ré preso aí eh tá liberto, né?

### 01:01:37

**Leonardo de Melo:** Uhum.

**Yann Naylor Francisco:** Mas o próprio réu preso poderia passar por esse fluxo? Faria sentido ele passar para esse fluxo.

**Leonardo de Melo:** Acho que não, hein?

**Emerson Yamamoto:** Como é que é? Eu não entendi.

**Felipe Martins Costa Brito:** Não, não, não, não, não,

**Yann Naylor Francisco:** Não, né,

**Emerson Yamamoto:** Não faz sentido.

**Felipe Martins Costa Brito:** não,

**Yann Naylor Francisco:** Felipe?

**Felipe Martins Costa Brito:** não.

**Yann Naylor Francisco:** Não, mas o que eu tava dizendo é que eu

**Felipe Martins Costa Brito:** Porque se ele informar o RG dele, vai jogar ele pro fut.

**Yann Naylor Francisco:** fuxo não tem. Entendi.

**Emerson Yamamoto:** É, se for preso, ele vai para outro fluxo. Ele não entra nesse fluxo de pessoa em liberdade, não. É o fluxo de de Nospen mesmo.

**Yann Naylor Francisco:** Tá perfetto.

**Leonardo de Melo:** Pegar aqui mais um RG pra gente fazer esse de representantes. Entendimento inicial aquele até exiboris por causa de do mapeamento, né, do órgão, eh, que é esse aqui. Eh, cadê penúltimo dígito? É seis.

### 01:02:46

**Leonardo de Melo:** Então ele aparece o da quinta DP e o da terceira. Então ele tá de acordo com a regra

**Yann Naylor Francisco:** aparece o da quinta.

**Leonardo de Melo:** da quinta. M. Eh, eita. É justamente por causa dessa regra aqui. Eh, então esse órgão aparece quando o final de RG tem 6 0 antes do dígito. Eh, e esse RG tem o seis, né? aqui.

**Yann Naylor Francisco:** Cara, que eu não não tô vendo a tua não tá tão claro para mim ali. É uns se então, né? No quinto. Ah, tá show.

**Leonardo de Melo:** Isso é 6 9 0.

**Yann Naylor Francisco:** Agora ficou muito Tá, tá bom. Yeah.

**Leonardo de Melo:** Eh, daí prosseguindo, vamos selecionar da quinta DP. Esse aqui é o RG do réu. Então a gente tá salvando nesse caso no campo, no campo no banco, não tem como ver pelo verde ainda. Eh, número RG real liberto. Então esse esse também deve ser armazenado nos outros, né?

### 01:04:01

**Leonardo de Melo:** Imagino.

**Emerson Yamamoto:** Isso só vai servir para Real Liberto mesmo,

**Leonardo de Melo:** Quando é real.

**Emerson Yamamoto:** Taiana, esse esse campo.

**Thaiana Lima:** Só para reunierto que o ré preso obrigatoriamente são pessoas diferentes e eu tenho as duas pessoas identificadas

**Emerson Yamamoto:** Uhum.

**Thaiana Lima:** já. O problema é que o Real Liberto era obrigatoriamente a mesma pessoa e agora a gente tá mudando para ser duas pessoas diferentes. Só que eu não, a gente não fez a versão complexa como é o preso de ter uma pessoa física tudo mais.

**Emerson Yamamoto:** Aham.

**Thaiana Lima:** fez só capturar o RG para pegar o mapeamento do órgão.

**Emerson Yamamoto:** Tá. É, o que eu acho que a gente pode fazer é talvez tirar aquela sessão de pessoa presa quando for real liberto, né? Não sei se faz sentido aparecer aqui um no verde.

**Thaiana Lima:** É, acho que não deve ter sido aproveitado. Posso colocar isso na lista da CRC porque ainda não entrou no sprint. M.

**Emerson Yamamoto:** É, eu acho que é legal porque eu tô achando que esse campo é que tá gerando complexidade.

### 01:04:57

**Emerson Yamamoto:** tem esse campo,

**Leonardo de Melo:** Então,

**Emerson Yamamoto:** facilita bastante de Gel.

**Leonardo de Melo:** eh, quando ele é representante, eu coloquei aqui para ele tirar as informações. Então ele não tem a pessoa presa, ó. Esse aqui é o do na direita é o quando é representante e o da esquerda quando ele é réu. Então não tem a pessoa presa quando é representante e na observação ele só informa o processo. Eh

**Felipe Martins Costa Brito:** O que eu não tô entendendo o seguinte, por que que traz dado de pessoa presa se a pessoa não tá presa?

**Emerson Yamamoto:** Então é porque provavelmente ele identificou uma pessoa presa, pessoa presa no sentido de ter uma na existir na tabela de apenado e aí provavelmente ente ele tá

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** sempre mostrando, sempre foi assim, entendeu?

**Felipe Martins Costa Brito:** mas não pode.

**Emerson Yamamoto:** Eu sei, mas isso aí é é do verde da época desde sempre. Tem que alterar o verde para mudar isso.

**Felipe Martins Costa Brito:** Porque se ele tá na tabela penada, não, não pode que eu digo assim.

### 01:05:52

**Felipe Martins Costa Brito:** Se ele tá na tabela penada, não é para deixar ele fazer esse encaminhamento.

**Emerson Yamamoto:** Então, mas foi exata Isso que eu falei que a gente não bate essa informação em hora nenhuma. Quando a gente bota o RG da pessoa, ele busca lá, ele pode achar na tabela de apenado e ela tá em liberdade.

**Felipe Martins Costa Brito:** Eí, tudo bem. Agora se ela tiver fechado.

**Emerson Yamamoto:** Mas é isso.

**Felipe Martins Costa Brito:** E

**Emerson Yamamoto:** Mas se tiver fechado, ele não manda para esse fluxo de pessoa em liberdade, ele manda pro fluxo do Nospen.

**Felipe Martins Costa Brito:** então isso, isso não mudou.

**Emerson Yamamoto:** Não, isso não mudou. Isso é continua sempre assim. É porque como eu te falei, quando você bota o RG, ele busca, acha a pessoa e acha que ela tá em liberdade, eu jogo ela, eu jogo ela pro fluxo de pessoa em liberdade.

**Felipe Martins Costa Brito:** Para esse aí,

**Emerson Yamamoto:** Isso.

**Felipe Martins Costa Brito:** para esse aí onde a gente tá.

**Emerson Yamamoto:** Só que tem uma um FK pessoa presa.

### 01:06:40

**Emerson Yamamoto:** Como tem um FK pessoa presa,

**Felipe Martins Costa Brito:** É que não pode exibir.

**Emerson Yamamoto:** a gente salva. É exatamente isso que eu falei. O que eu acho que tem que acontecer é no verde a gente nunca exibir pessoa presa se for real em liberdade,

**Felipe Martins Costa Brito:** Ah,

**Emerson Yamamoto:** entendeu?

**Felipe Martins Costa Brito:** é. Não tá,

**Leonardo de Melo:** Então,

**Felipe Martins Costa Brito:** entendi.

**Leonardo de Melo:** eh, na verdade aqui não é apenado, tipo, ele pega o da assistido logado direto.

**Emerson Yamamoto:** É o que é pior ainda. Tá errado.

**Leonardo de Melo:** É,

**Emerson Yamamoto:** Tá totalmente errado esse campo aí.

**Leonardo de Melo:** ele não verifica se tem nem nada. Então, porque como ele informa que é o R, ele já vai direto. Acho que tem que rever esse fluxo mesmo. Acho que daí dessa ISO seria isso. Tá, ele armazenou aqui.

**Thaiana Lima:** Não, desculpa. Você pode voltar lá no começo depois quando você coloca o número de processo seu.

**Leonardo de Melo:** Uhum.

### 01:07:44

**Leonardo de Melo:** botar aqui

**Thaiana Lima:** Vamos ver o passo.

**Leonardo de Melo:** de processo esqueci aqui.

**Thaiana Lima:** A situação que você tá, o sea pessoa não é parte do processo, né?

**Leonardo de Melo:** É isso. Aí ele vai pedir essa pergunta.

**Thaiana Lima:** Então, mas aí não é,

**Leonardo de Melo:** Eh, então primeiro vem essa se o réu é está em liberdade,

**Thaiana Lima:** tá?

**Leonardo de Melo:** né? Eh, clicando em não, ali, exibir.

**Thaiana Lima:** Mas isso real liberdade assim, né?

**Leonardo de Melo:** Ah, então ele se encontra preso, no caso,

**Thaiana Lima:** Ah, tá.

**Leonardo de Melo:** tava escrito

**Thaiana Lima:** Libertar. Eu não li a pergunta contrária. Ah, tá bom. Ah, depois disso é que ele pediu o RG, né? Ele sempre passa por essa pergunta antes de pedir o RG.

**Leonardo de Melo:** isso.

**Thaiana Lima:** Entendi.

**Leonardo de Melo:** Depois disso que a gente pede Eu

**Thaiana Lima:** Obrigado.

**Leonardo de Melo:** acho que a gente mudou isso agora, inclusive antes. Acho que ele pediu a RG antes de perguntar se tava preso ou não.

### 01:09:12

**Leonardo de Melo:** M.

**Emerson Yamamoto:** Tá bom. O campo a gente tá salvando, o campo novo lá tá salvando nas situações certas. quando ele diz que é representante, isso aí para mim tá tranquilo e a gente tá colocando na observação e nesse campo o mesmo RG. O única coisa que tava diferindo realmente era o pessoa presa que não vai mais existir. Então acredito que com isso vai ficar certo. Pelo menos pelo que eu tô entendendo

**Leonardo de Melo:** É só realmente vai você vai tirar a pessoa presa e a observação também, né?

**Emerson Yamamoto:** na observação. Eu acho que tira o nome, né? Taiana, quando ele diz que é representante.

**Leonardo de Melo:** É, quando é representante eu eu tô tirando os dois assim, o o RG e o o Nel tem que ter,

**Emerson Yamamoto:** Ah, não, acho que tem que ter o RG, né? Mantém o RG.

**Leonardo de Melo:** tá?

**Emerson Yamamoto:** Tem na observação.

**Thaiana Lima:** Tem que ter o G, tem que ter.

**Emerson Yamamoto:** Sim.

**Thaiana Lima:** É, mas isso tá na eixo da CRC, tá?

### 01:10:16

**Thaiana Lima:** Precisa se preocupar com isso aqui não. Assim, você,

**Emerson Yamamoto:** Não,

**Thaiana Lima:** quer dizer, na hora de criar o encaminhamento,

**Emerson Yamamoto:** não é porque o campo a gente é o campo a gente tem que

**Thaiana Lima:** você tem que incluir. Aham. Observação é o RG permanece.

**Emerson Yamamoto:** incluir.

**Thaiana Lima:** Podear RG da do ré dois pontos.

**Leonardo de Melo:** OK.

**Emerson Yamamoto:** É o que então eu bato? Só para eu pegar aqui. É incluir RG

**Leonardo de Melo:** Eh, quando for quando for representante, inclui o RG na Isso.

**Emerson Yamamoto:** na observação. Apenas o RG. Vou botar apenas o RG do réu na observação quando for caso de representante. Beleza? Eh, OK. No caso que não é representante, tu não tá salvando então o naquele campo novo, né, Leardo, que é o certo,

**Leonardo de Melo:** Isso é não, não salva como novo.

**Emerson Yamamoto:** tá?

**Leonardo de Melo:** E aí tem o refinamento também quando eh assim o assistido informa que o réu se encontra preso, né? Mas ele diz que também é o réu.

### 01:11:28

**Leonardo de Melo:** Aí esse fica com o RG diferente.

**Emerson Yamamoto:** Mas esse caso não vai mais acontecer, né? porque não vai ter mais a sessão de pessoa presa.

**Leonardo de Melo:** Uhum.

**Emerson Yamamoto:** Então acho que esse caso tá resolvido. Vai aparecer o RG, aquele é o RG que você informou, né? Vai aparecer o RG, certo?

**Leonardo de Melo:** Isso. Tá.

**Emerson Yamamoto:** Mas aí tem um problema, né? Eh, o nome ali não é o nome da pessoa presa mesmo, é o seu nome meio vai vai ter,

**Leonardo de Melo:** M.

**Emerson Yamamoto:** entendeu? Esse caso, Felipe vai ter que meio que confiar na pessoa. Se ela falar eu sou o réu, a gente vai pegar o nome dela e o RG que ela informou. Mas no CPEN pode ser diferente.

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** Tudo bem? Isso tem uma verificação se a

**Felipe Martins Costa Brito:** qual é a outra alternativa?

**Emerson Yamamoto:** pessoa do aplicativo é a mesma pessoa do CPEN, né?

**Felipe Martins Costa Brito:** Não acho melhor, não.

### 01:12:27

**Emerson Yamamoto:** É porque para bater isso não é não tem como ter muita certeza.

**Felipe Martins Costa Brito:** É aí.

**Emerson Yamamoto:** Aí realmente pode bloquear, né? Tá bom. Então a gente deixa assim. Agora uma outra dúvida, ô Felipe, por que que esse eu eu entendi que esse campo ele só é útil quando a pessoa é representante, mas eu tô entendendo que quando não é representante, esse campo que eu digo é o campo novo de RG que vai existir, né? Eh, mas quando ela não é representante, isso só aparece na observação, como o Leonardo tá mostrando ali, ó, Leonardo de Melo Soares e o RG. Será que não seria ideal sempre ter o campo do RG se for Real Liberto?

**Felipe Martins Costa Brito:** Pode trazer,

**Emerson Yamamoto:** Porque então,

**Felipe Martins Costa Brito:** eu não vejo problema não.

**Emerson Yamamoto:** mas é porque isso muda isso, porque hoje a gente só tá salvando nesse campo novo quando é representante,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** mas em vez de mostrar só na observação,

**Felipe Martins Costa Brito:** eu não vejo.

**Emerson Yamamoto:** não deveria sempre mostrar nesse campus, já que esse é o campo do RG, do Real Liberto, alguma coisa assim.

### 01:13:23

**Felipe Martins Costa Brito:** Po, acho que sim.

**Emerson Yamamoto:** Mas não sei o que que você pensou, Taiana, em relação a isso de só mostrar esse campo se for o representante,

**Thaiana Lima:** É, eu pensei nisso, porque se ele não for representante, minha referência é o cadastro, é o RG do cadastro.

**Emerson Yamamoto:** mas é porque não aparece ali, né? Tipo,

**Thaiana Lima:** É,

**Emerson Yamamoto:** só aparece na observação,

**Thaiana Lima:** mas tem observação.

**Emerson Yamamoto:** entendeu?

**Thaiana Lima:** Hum.

**Emerson Yamamoto:** É, mas na observação vai aparecer o do outro também. Esse que é o ponto. Tipo, eu não eu não tô entendendo o motivo do campo novo,

**Felipe Martins Costa Brito:** Não,

**Emerson Yamamoto:** já que sempre vai estar na observação da mesma forma.

**Felipe Martins Costa Brito:** não. Padroniza, bota o RG, padroniza. Bota o RG no nos dois.

**Emerson Yamamoto:** Bota sempre no campo novo,

**Felipe Martins Costa Brito:** É,

**Emerson Yamamoto:** então tá.

**Felipe Martins Costa Brito:** é,

**Emerson Yamamoto:** E mantém na observação, né, Felipe? Do jeito que já era.

**Felipe Martins Costa Brito:** é.

### 01:14:03

**Felipe Martins Costa Brito:** Porque essa tela quem vê CRC e a e a observação acaba que o órgão consegue ver

**Emerson Yamamoto:** Uhum.

**Felipe Martins Costa Brito:** pela na pauta do dia lá.

**Emerson Yamamoto:** Tá. Então vamos fazer essa alteração. A gente sempre salva. Então, Leopardo, mesmo se for representante ou não, além de fazer o que já faz na observação, normal, vai manter, a gente sempre salva o no RG e R liberto.

**Leonardo de Melo:** Beleza, tranquilo.

**Emerson Yamamoto:** Eu eu acho que é melhor padronizar mesmo,

**Leonardo de Melo:** Uhum. mais sentido mesmo. M.

**Emerson Yamamoto:** botar aqui sempre salvar o RG no campo de no campo novo. Isso no fluxo de real liberto, claro, né? OK. Aí depois só tem que alterar o verde para para incluir esse campo, mas aí vai entrar na eixa do verde e tirar a parte da pessoa presa. Beleza.

**Leonardo de Melo:** Enfim, aí tem um movimento também, né? No caso ele tem o RG. Imagino que fique da melhor maneira, né?

### 01:15:11

**Leonardo de Melo:** Inclusive ele não reaproveita o o caso, então tá cheio de caso aqui. Eh, então é isso.

**Felipe Martins Costa Brito:** Podia reaproveitar o caso.

**Leonardo de Melo:** Acho que dessa tarefa

**Thaiana Lima:** É isso é estranho. Vou procurar.

**Leonardo de Melo:** acho que nessa tarefa é isso. Eh, seguir paraa próxima. Então, já terá encaminhamento processual para reaproveitar ou criar caso processual.

**Felipe Martins Costa Brito:** Será que não era para tá aí, Thaiana, nessa nessa

**Thaiana Lima:** Essa aí é outro fluxo que é a busca de processo pura assim.

**Felipe Martins Costa Brito:** então, mas de repente não era para botar nessa aí também essa regra

**Emerson Yamamoto:** Так.

**Thaiana Lima:** Ah, não sei porque é o mesmo critério.

**Felipe Martins Costa Brito:** seria mesma parte, mesmo processo, mesmo RG,

**Thaiana Lima:** Se ele for representante de Ros diferentes.

**Felipe Martins Costa Brito:** mas é o mesmo processo, nem é a mesma, nem o mesmo R,

**Thaiana Lima:** Ah, o execução penal é um só, né?

**Felipe Martins Costa Brito:** é um só,

**Thaiana Lima:** Uma pessoa sabe o processo.

**Felipe Martins Costa Brito:** né?

### 01:16:25

**Thaiana Lima:** É, fal com Catalita que ela escreveu a seis.

**Leonardo de Melo:** Tá, percebi então o nosso eixo.

**Thaiana Lima:** Ah, para aí só um minutinho.

**Leonardo de Melo:** Uhum.

**Thaiana Lima:** Na iso de da CRC, pelo menos que encontrei mais rápido do fluxo de Roberto, ele diz que depois que finaliza o encaminhamento verifica se pode reaproveitar um caso. Então, não sei se o app tá sem isso ou se faltou.

**Leonardo de Melo:** Hum. Aqui tem alterar fluxo processual. É esse aqui, né? O do app.

**Thaiana Lima:** É,

**Leonardo de Melo:** Ah,

**Thaiana Lima:** tem também.

**Leonardo de Melo:** não.

**Thaiana Lima:** Pode ser o item cinco da 6465.

**Leonardo de Melo:** Deixa eu ver. 465.

**Thaiana Lima:** É, é o critério cinco.

**Leonardo de Melo:** Hum. Sim.

**Thaiana Lima:** Verificar se pode ser aproveitado.

**Leonardo de Melo:** É, não, não, não sei por aqui não não foi. Acho que pode.

**Thaiana Lima:** Vou botar com refinamento para para vocês testarem. M.

**Leonardo de Melo:** É isso.

**Thaiana Lima:** Yeah.

**Emerson Yamamoto:** Verificar o reaproveitamento. Tá, mas é estranho.

### 01:17:51

**Emerson Yamamoto:** Você tá botando a mesma pessoa, Léo, porque nem poderia ter ter o mesmo caso processual com o mesmo número, com o mesmo personagem.

**Leonardo de Melo:** Sim é todo tudo igual assim. Не.

**Emerson Yamamoto:** estranho. Eu eu lembro que tinha uma questão que se mudasse o personagem mudava o caso, mas se fosse o mesmo, realmente tudo igual, eu acho que teria que aproveitar sim.

**Thaiana Lima:** É, teria

**Leonardo de Melo:** Tá, eu vou verificar isso depois. Prosseguir agora com essa eixo que é justamente no buscar processo e receber intimação, poder reaproveitar ou criar o caso processual para esses processos. Então, nesses dois fluxos, eh, vai ser criado o encaminhamento como um de urgência. E aí quando for para reaproveitar vai ser verificado se já existe um caso que seja aberto com o mesmo número de processo e mesmo origem MNI. E o usuário, né, o assistido é um personagem de mesmo tipo de assistido do caso ou um representante desse personagem, né? E aí, se existir mais de um caso, deve ser verificado o caso mais atualizado por medida dessas regras aqui, né?

### 01:19:16

**Leonardo de Melo:** atendimento remoto, andamento feito pela Defensoria, ocorrência resposta ao defensor ou anotação mais recente ou ID mais recente. E nesse caso de reaproveitamento vai ser vinculado o encaminhamento ao caso e vai ser criado um andamento com o título de encaminhamento assistido, nome assistido encaminhado para o órgão e a descrição se foi remoto ou presencial. Eh, se não existir o caso, ele vai ser criado e aí vai ser criado com essas regras aqui que eu vou passar depois. Eh, e vai ser criado um andamento também, né? Então vai ser dessa forma. Vou pegar aqui um caso que eu já tenho pra gente ver que ele vai reaproveitar. Então, esse processo aqui eh de final 025. Deixa eu pegar aqui esse curso de formação. A gente vai buscar aqui o processo pra gente ver certinho. Eh, mesmo tá aqui. Esse nesse processo ele vai tentar reaproveitar is aqui. Então, buscando aqui pelo pelo buscar processo. S. aqui ele pegou o órgão responsável pelo caso, eh, para o assunto também certinho.

### 01:21:12

**Leonardo de Melo:** E quando a gente bus, eh, fazer essa busca, a gente vai ver que ele gera um encaminhamento. Vou pegar aqui o caso pra gente ver. Esse daqui pegar aqui ficar a casa. Esse daqui, ó, aqui é o caso. Ele pela Ixo precisa fazer esse andamento aqui. Então foi o que ele fez. Encaminhamento assistido a Leonardo de Melo Soares, encaminhado para o DP junto aos juizados especiais cíveis de Campo Grande, atendimento presencial. Eh, então ele conseguiu reaproveitar esse caso. Eh, e o encaminhamento foi associado, né? Então, se a gente for aqui para esse encaminhamento, ele vai nos levar até esse caso.

**Emerson Yamamoto:** Uma

**Leonardo de Melo:** Eh, aqui ver caso, ele leva justamente para esse aqui, ó, é o mesmo, né? 645 64. Então, me levou pro mesmo caso. Eh,

**Emerson Yamamoto:** dúvida, Léo, ali no app, eu não eu não vou direto pro caso não. Depois que eu encaminho ali quando tu dá OK,

**Leonardo de Melo:** depois encaminhar.

### 01:23:01

**Emerson Yamamoto:** não, né?

**Leonardo de Melo:** Não, não, aqui não.

**Emerson Yamamoto:** É porque eu lembro que tem algum fluxo que tem o eh depois depois de um de um encaminhamento, não sei se é de encaminhamento,

**Leonardo de Melo:** Sim,

**Emerson Yamamoto:** mas que que vai pro caso

**Leonardo de Melo:** sim. ou de pessoa presa, se eu não me engano, ele vai aparece um botão para você acompanhar o atendimento.

**Emerson Yamamoto:** acompanhar o atendimento. É isso, é esse o botão,

**Leonardo de Melo:** Isso aí ele leva pro caso direto.

**Emerson Yamamoto:** tá? É, aqui não, não tem isso, né?

**Thaiana Lima:** Eu acho que é por conta do presencial, não, que a gente encaminha para atendimento no remoto.

**Emerson Yamamoto:** Ah, sim, pode ser,

**Leonardo de Melo:** É,

**Emerson Yamamoto:** pode ser.

**Leonardo de Melo:** talvez seja isso. Posso até fazer esse fluxo também. aqui para verificar se aparece atendimento remoto. Co? Aqui ele já vai paraa mensagem, né? Então comunicar que ele já envia mensagem direto.

**Thaiana Lima:** É que ele já tinha um caso, ele joga para lá.

### 01:24:20

**Thaiana Lima:** Se não tivesse um caso,

**Emerson Yamamoto:** Yeah.

**Thaiana Lima:** aí ele tinha feito o encaminhamento.

**Leonardo de Melo:** Uhum. Isso aí esse caso aqui, né? Eu vou fazer o seguinte agora, eu vou fechar esse caso para ele deixar de ser aproveitável. Inclusive a gente pode ver que vai surgir um encaminhamento aqui, né? Porque como peso remoto, ele agora aparece. Acho que agora ele tá tá errado aqui, né?

**Emerson Yamamoto:** É verdade, ficou atendimento presencial.

**Leonardo de Melo:** É.

**Emerson Yamamoto:** Vou anotar aqui. Nie.

**Leonardo de Melo:** Tá, eu vou encerrar esse caso para já deixar de ser aproveitável que agora ele vai começar a criar o caso, né? processo novamente. Prosseguir aqui com o atendimento. Aquele já foi direto. Eh, vamos ver aqui se ele criou o casa. aqui, caso criado automaticamente pelo aplicativo. Eh, e aí o andamento que ele pede aqui é diferente. Então, andamento com o caso criado automaticamente pelo aplicativo e informando por qual fluxo que foi, né?

### 01:26:13

**Leonardo de Melo:** Então, consultou o processo ou informou o recebimento de intimação.

**Felipe Martins Costa Brito:** Daana, por que que precisa ter esse título caso criado automaticamente pelo aplicativo?

**Thaiana Lima:** Não lembro. Felipe estava no eixo.

**Emerson Yamamoto:** Eu

**Felipe Martins Costa Brito:** Tava o o Leonardo acabou de ler aí.

**Thaiana Lima:** Foi mal. Ah, foi Talita que que definiu.

**Felipe Martins Costa Brito:** É, tem que não vejo, né? Eu não vejo necessidade,

**Thaiana Lima:** Eu não sei se já existe isso em outros.

**Felipe Martins Costa Brito:** porque os outros não têm isso,

**Emerson Yamamoto:** acho, eu acho que é só para informar mesmo que foi um caso criado automático e não por uma pessoa.

**Felipe Martins Costa Brito:** mas não não vejo qual é o é a relevância

**Emerson Yamamoto:** A vantagem, né?

**Felipe Martins Costa Brito:** dessa informação.

**Emerson Yamamoto:** A gente pode tirar,

**Felipe Martins Costa Brito:** No.

**Emerson Yamamoto:** não tem problema. M.

**Felipe Martins Costa Brito:** É porque fica um título feião.

**Leonardo de Melo:** Угуm.

**Emerson Yamamoto:** Não achei não, mas a gente pode tirar, tanto faz, sem problema.

### 01:27:07

**Emerson Yamamoto:** Já fica ali na origem que ele foi criado pelo app,

**Thaiana Lima:** Tiramento.

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** Sim,

**Emerson Yamamoto:** Volta ali, ô Léo, rapidinho. Ali, ali. App, ali já dá para saber que foi o que essa casa tem origem app.

**Felipe Martins Costa Brito:** exatamente.

**Emerson Yamamoto:** É, pode ser. Tem, não tem problema não. É,

**Thaiana Lima:** Casa é tirar o andamento,

**Emerson Yamamoto:** se foi criado pelo app automático,

**Thaiana Lima:** né? Não é mesmo um título.

**Emerson Yamamoto:** né? Oi. Oi.

**Thaiana Lima:** Assim, no caso,

**Emerson Yamamoto:** Tá indo remover o andamento.

**Thaiana Lima:** não é não é alterar o título, é remover o andamento em si,

**Felipe Martins Costa Brito:** Sim,

**Emerson Yamamoto:** Isso,

**Felipe Martins Costa Brito:** sim,

**Emerson Yamamoto:** exato.

**Felipe Martins Costa Brito:** sim,

**Thaiana Lima:** tá? M.

**Felipe Martins Costa Brito:** sim.

**Emerson Yamamoto:** Só que aí não vai ter esse negócio do fluxo aí também é desnecessário. Felipe assistido, consultou o processo.

**Felipe Martins Costa Brito:** também não não sei porque que tem que ter no

### 01:27:39

**Emerson Yamamoto:** Assistiu desnecessário.

**Felipe Martins Costa Brito:** senão vão ficar vários andamentos lá que o cara entra todo dia para ver o processo.

**Emerson Yamamoto:** Não, mas aí não vai criar o caso de novo. Isso é só quando cria o caso, entendeu?

**Felipe Martins Costa Brito:** Entendi, mas eu acho não vejo necessidade mesmo.

**Emerson Yamamoto:** Não tem necessidade, tá?

**Felipe Martins Costa Brito:** M.

**Emerson Yamamoto:** Beleza? Então vou vou mudar aqui, vou vou anotar aqui. É não criar andamento de criação automática de caso. Beleza? Eu acho que nenhum lugar tem isso mesmo,

**Leonardo de Melo:** Eh É,

**Emerson Yamamoto:** esse andamento. Acho que só aqui mesmo. Beleza. Segue aí, Léo.

**Leonardo de Melo:** mostrar também o encaminhamento. Fica dessa forma, né? Eh, tudo certinho. Aí essa criação de causa tem algumas regras, né? Então acho que não tem como mostrar pelo pelo verde, mas prestação judicial vinculado com processo do fluxo, tipo de assistido do CP, ter que verificar se o usuário é parte do processo. Ess inclusive a gente tava com probleminha em recuperar as partes, daí eu coloquei algumas partes direto pelo código só nessa versão mesmo.

### 01:29:06

**Leonardo de Melo:** Isso aqui não vai ter. Então esse assistido que eu tô logado, ele tá como réadestrou aqui como ré também o caso. Eh, os personagens do caso, né? Então, todas as pessoas do processo judicial têm que ser cadastradas eh como personagens.

**Emerson Yamamoto:** T

**Leonardo de Melo:** E aí tipos de polo de TJ que não tem tipo de personagem correspondente no verde deve ser tratado como terceiro. Se a gente for pegar aqui os personagens desse caso, eh, estão todos que eu coloquei aqui via código. Então, esses daqui, esses três, corretamente, inclusive o assistido que tá como ré. Eh, assunto também tá corretamente pegando O o assunto TJ do processo.

**Emerson Yamamoto:** Esses personagens vieram da onde mesmo? Não.

**Leonardo de Melo:** Eu coloquei via código mesmo,

**Emerson Yamamoto:** Ah, tá.

**Leonardo de Melo:** porque a gente tava com probleminha na hora de consultar o MN.

**Emerson Yamamoto:** Ah, sim. Saquei. Saquei. Mas isso aí vai vir do da das partes do processo.

**Leonardo de Melo:** Isso é, inclusive tem uma alteração de app nessa ISO para poder passar dessa consulta e buscar processo para levar essas partes pro end point de confirmar encaminhamento, que são duas partes diferentes, né?

### 01:30:31

**Leonardo de Melo:** Então, se eu tivesse que pegar essas partes na hora de fazer o encaminhamento e criar o caso, eu teria que fazer outra consulta no processo e aí seria mais custoso. Eh,

**Emerson Yamamoto:** Só um ponto aí. Entendi. Eh, Taiana, eu lembro que eu não sei se hoje em dia isso já melhorou, mas lá muito lá atrás, na época que eu ainda era só do Nuspen, eh, a gente tinha muito problema com personagem que vinha do TJ. Eh, às vezes o o personagem ou documento, não tinha documento, alguma coisa assim. Meu medo é só gerar muita duplicidade, talvez, de cadastro. Não sei se isso é um problema aqui. Eh, a gente quer mesmo cadastrar todas as partes do processo como personagem ali. Só uma preocupação mesmo de talvez não flodar o sistema.

**Thaiana Lima:** Ó, eu acho que que a ideia era adiantar para deixar o caso mais completo, ter todos os outros personagens, mas realmente isso pode acontecer.

**Emerson Yamamoto:** Uhum. Não dá para tá feito, mas só só vi essa preocupação porque eu lembro que a gente salvava até as partes dos processos,

### 01:31:41

**Thaiana Lima:** Hum.

**Emerson Yamamoto:** salvava mesmo como personagem sempre e a gente deixou de salvar porque, enfim, às vezes era empresa, aí fica um nome meio maluco, sei lá. Não sei se isso pode trazer algum problema dos dos casos ficarem meio poluídos assim, mas tudo bem,

**Thaiana Lima:** É, não sei como tá em produção,

**Emerson Yamamoto:** a gente pode Uhum.

**Thaiana Lima:** porque o verde já faz isso, né? Quando a gente busca um processo, a gente já cadastra as partes para poder criar o caso.

**Emerson Yamamoto:** Por onde? Pelo verde, tem que ser manual. Não, tu não tem que clicar ali para criar ou não?

**Leonardo de Melo:** Não, acho que ele na consulta do processo

**Thaiana Lima:** alguns lugares.

**Emerson Yamamoto:** Ele já cria. Ah, tá.

**Felipe Martins Costa Brito:** É, mas aí eu acho que tem que ser a mesma regra, padronizando. O que vem do App com vários casos que vem do verde não, vários casos não, vários personagens.

**Emerson Yamamoto:** Mas o verde já cria, pelo que a Taiana falou, né? Eu não sabia.

**Felipe Martins Costa Brito:** Acho com todos.

### 01:32:37

**Thaiana Lima:** Não sei se Ш.

**Felipe Martins Costa Brito:** É só confirmar. Se no verde faz, mantém. Se o verde não faz,

**Emerson Yamamoto:** É,

**Felipe Martins Costa Brito:** descarta.

**Emerson Yamamoto:** eu sei que o verde não cria se faltar alguma informação, que aí ele mostra ali um negócio para você criar manualmente. Ele não cria para todos os casos, não. Mas talvez se tiver completo, tem uma regra para isso. Não sei se aqui não é pra gente tá aplicando essa regra também ou se a gente tá sempre criando, né?

**Leonardo de Melo:** É, eu eu assim falando de código, eu só troquei uma flag no buscar processo que é de com cadastro pessoa.

**Emerson Yamamoto:** Ah, tá. Ele já cria, então, né?

**Leonardo de Melo:** Isso.

**Emerson Yamamoto:** Ah, saquei.

**Leonardo de Melo:** E aí ele deve fazer internamente igual ao verde, né?

**Emerson Yamamoto:** Ah, entendi.

**Leonardo de Melo:** Inclusive para criar os personagens eu só tô pegando os que tem de pessoa. Então se ele não tem a pessoa, ele não cadastra com personagem, né?

### 01:33:26

**Leonardo de Melo:** que imagino que não conseguiu fazer a pessoa na hora de buscar o

**Emerson Yamamoto:** Entendi. Mas ele cria pessoa.

**Leonardo de Melo:** processo.

**Emerson Yamamoto:** Se não existir,

**Leonardo de Melo:** Isso é assim,

**Emerson Yamamoto:** tenta criar,

**Leonardo de Melo:** não consegui testar por causa da É,

**Emerson Yamamoto:** né? Aham. Sim.

**Leonardo de Melo:** exato.

**Emerson Yamamoto:** Não, tudo bem. A gente pode manter só alertando que a gente é porque no app nunca faz isso, né? A gente nunca cria caso fora o personagem que tá no app. Seria a primeira vez, não tem problema. Só pode gerar algum tipo de Mas se a gente já faz isso no verde, tá ótimo.

**Leonardo de Melo:** É, inclusive outra coisa que eu fiquei em dúvida, que eu não consegui verificar, é essa parte aqui de qualquer tipo de polo do TJ que não tenha tipo de personagem correspondente no verde. Eh, isso aqui também vem na consulta de processo, tipo,

**Emerson Yamamoto:** Vem o tipo de polo.

**Leonardo de Melo:** ele automaticamente,

**Emerson Yamamoto:** Tem ativooivo.

**Leonardo de Melo:** então, mas ele ele já coloca como terceiro, se ele não consegue identificar.

### 01:34:24

**Emerson Yamamoto:** Ah, tá. Ah, ele já faz isso hoje.

**Leonardo de Melo:** Então, essa é a minha dúvida.

**Emerson Yamamoto:** Ah, tá.

**Leonardo de Melo:** Seria

**Emerson Yamamoto:** Cara, não sei também. A gente precisaria de um processo para testar.

**Leonardo de Melo:** Uhum. Que é uma coisa que eu não consigo testar também.

**Emerson Yamamoto:** É, vamos ter que verificar.

**Leonardo de Melo:** Eh,

**Emerson Yamamoto:** Não sei também.

**Leonardo de Melo:** e todo o resto tá de acordo, né? Então, pega a matéria, não tem sigilo, é o órgão, o mesmo órgão que aparece na consulta do processo, origem app e tudo mais, né? Eh, então acho que seria isso. Tem também o fluxo de recebo intimação, eu posso fazer também.

**Emerson Yamamoto:** É a mesma coisa, né?

**Leonardo de Melo:** É sem nem não muda nada assim.

**Emerson Yamamoto:** Eu

**Leonardo de Melo:** Tem esse esse processo aqui.

**Emerson Yamamoto:** jurava que esse esse fluxo de receber intimação já criava caso.

**Leonardo de Melo:** É, ele ele usa um caso quando já tem, né?

**Emerson Yamamoto:** É, quando já tem,

### 01:35:32

**Leonardo de Melo:** Acho que ele já reaproveita.

**Emerson Yamamoto:** eu sei. Mas eu achei que criava mesmo.

**Thaiana Lima:** A gente não criava por conta do encaminhamento não ter verificação do tabelar ou natural. Agora que ele tem, a gente possa criar o caso que a gente acerta mais.

**Emerson Yamamoto:** Ah,

**Thaiana Lima:** Sì. Yeah.

**Emerson Yamamoto:** entendi. Ja. Era

**Leonardo de Melo:** buscar o atendimento. Got. que ele criou um encaminho metodo de urgência por ser examente uma ação. Vou pegar aqui o caso.

**Emerson Yamamoto:** tua chance de botar o remoto. Aí tu botou presencial.

**Leonardo de Melo:** É verdade. Eu não lembro se já tinha casa. É, já tinha em casa, então ele reaproveitou. Aqui é o mais recente. Ele tá trocado, não sei porque ele tá como remoto.

**Emerson Yamamoto:** É, tá meio bugado isso aí.

**Leonardo de Melo:** É,

**Emerson Yamamoto:** Botar aqui.

**Leonardo de Melo:** é só no andamento mesmo.

**Emerson Yamamoto:** Uhum.

**Leonardo de Melo:** Vou encerrar o caso aqui só pra gente ver que ele vai criar agora pelo recebção também.

### 01:36:56

**Leonardo de Melo:** eh, mostrar também o encaminhamento. Não, tá aqui certinho. Aqui tá presencial como deveria ser, encammento de urgência e tudo mais,

**Emerson Yamamoto:** Essa é uma que a gente vai ter que testar com cuidado, que tem bastante coisa.

**Leonardo de Melo:** né? Aqu ele já foi direto. Eh, cadê? Ele criou um outro caso. Então, ele criou isso aqui com caso criado automaticamente pelo aplicativo que a gente vai tirar, né? informando que recebeu intimação e o encaminhamento que também foi criado devidamente.

**Emerson Yamamoto:** Tu número de processo, por isso que ele criou o caso.

**Leonardo de Melo:** Não, eu encerrei o caso que que tava antes,

**Emerson Yamamoto:** Ah, tá, encerrou. Aham, entendi.

**Leonardo de Melo:** aí ele não reaproveitou.

**Emerson Yamamoto:** Depois, não, agora,

**Leonardo de Melo:** aqui.

**Emerson Yamamoto:** mas que a gente pode vai ter que testar depois é, por exemplo, se existia um caso com os mesmos personagens, mas sei lá, de outro tipo de assistido, sei lá, em vez de ser autor, ser de ré, ele não deveria reaproveitar, por exemplo,

### 01:38:21

**Leonardo de Melo:** Hum. Sim.

**Emerson Yamamoto:** situações assim mais ambíguas que que podem gerar problema. Entendeu?

**Leonardo de Melo:** É,

**Emerson Yamamoto:** Porque se for o caso foi de réutor, ele não deveria aproveitar.

**Leonardo de Melo:** sim.

**Emerson Yamamoto:** No caso

**Leonardo de Melo:** Talvez dê para testar isso aqui agora. Tem como dar pelo verde? Não, né?

**Emerson Yamamoto:** tem clica ali em editar ali em cima. Ali

**Leonardo de Melo:** Ah, sim. Assistor que ele não

**Emerson Yamamoto:** ele vai mandar, vai pedir para mudar os personagens, eu acho. Salva aí. É lá ele ele altera.

**Leonardo de Melo:** Ah, sim. M.

**Emerson Yamamoto:** Altera aí,

**Leonardo de Melo:** É, aí ele esse sentido tá como,

**Emerson Yamamoto:** tá? Como ré,

**Leonardo de Melo:** tá como o réu,

**Emerson Yamamoto:** né?

**Leonardo de Melo:** ele vai virar autora.

**Emerson Yamamoto:** Então, mas muda ali isso, faz o contrário. Você tá como ré, né? Bota você como ré, o caso é de autor.

**Leonardo de Melo:** Uhum.

**Emerson Yamamoto:** É, aí tá certo, porque eu você tá como ré, mas esse caso é de autor, então ele não deveria reaproveitar.

### 01:39:27

**Leonardo de Melo:** Isso. Daí fazendo isso, ele deve criar um caso, né?

**Emerson Yamamoto:** Sim, deveria.

**Leonardo de Melo:** buscar atendimento aqui. Ele foi direto. Vamos ver aqui. É criar o caso. Sim.

**Emerson Yamamoto:** Show.

**Leonardo de Melo:** aqui se che do réu ca caso criada pela essa intimação

**Emerson Yamamoto:** É isso. Criou certinho. Beleza. É isso.

**Leonardo de Melo:** aí. É isso. Nossa iso começou,

**Emerson Yamamoto:** Essa é bem bem trabalhosa.

**Leonardo de Melo:** né? É, tem uma coisa que eu alterei aqui, porque pode acontecer do assistir do não fazer parte do processo,

**Emerson Yamamoto:** Hum.

**Leonardo de Melo:** né? Daí o que eu fiz foi colocar um modal eh informando isso. Para isso eu vou ter que mudar o nome da da pessoa física. Eu vou colocar aqui mudando o nome para não fazer parte do processo. Então pegar aqui a pessoa, vou tirar os aqui, ó. processo que aí nesse caso, como ele não faz parte do processo, não vai deixar reaproveitar nem criar o caso.

### 01:41:34

**Leonardo de Melo:** Isso é algo que não tá dito na ISO, mas é algo que eu tinha perguntado paraa API e aí eu fiz dessa

**Emerson Yamamoto:** Sì.

**Leonardo de Melo:** forma. Não foi possível identificar seu usuário como parte do processo. Entre em contato conosco pela 129. Aí queria só confirmar se essa mensagem tá correta.

**Felipe Martins Costa Brito:** Já podia usar a nova, né?

**Thaiana Lima:** M. É, mas aí não vai ter o botão ainda de vir para WhatsApp porque a funcionalidade não print

**Felipe Martins Costa Brito:** Aí, aí vai lançar lá e depois vai ter que alterar aqui, né?

**Thaiana Lima:** não. Quando a gente fizer vai ser depois dessa. Então essa já vai tá feita,

**Felipe Martins Costa Brito:** Hã.

**Thaiana Lima:** a gente altera aqui.

**Felipe Martins Costa Brito:** Ah, então tá bom. Então, beleza.

**Thaiana Lima:** Tá faltando o botão de ligar um 29, né?

**Felipe Martins Costa Brito:** Tá. Não. Beleza. Se dá para alterar depois, tranquilo.

**Thaiana Lima:** Eu só não sei se assim o Zória vai achar que o encammentamento não foi feito aqui, porque oamento vai ser feito, né?

### 01:42:36

**Thaiana Lima:** O que não tem é o a criação do caso,

**Leonardo de Melo:** É, não, nesse caso ele não deixa prosseguir.

**Felipe Martins Costa Brito:** Não fez nem nenhum encaminhamento.

**Leonardo de Melo:** Não.

**Thaiana Lima:** mas eu acho que o encaminhamento era para ser feito, não?

**Felipe Martins Costa Brito:** Eu acho que sim.

**Thaiana Lima:** Eu acho que sim.

**Felipe Martins Costa Brito:** Só não cria o caso.

**Thaiana Lima:** Acho que tem tudo para fazer.

**Felipe Martins Costa Brito:** E pensando agora, tá? A questão foi só não não criar o caso, nem precisa da da dar erro.

**Thaiana Lima:** É porque o encammento tem todas as informações,

**Leonardo de Melo:** Não.

**Thaiana Lima:** né? A gente achou o órgão, tudo certo.

**Leonardo de Melo:** Sim, sim. É, não,

**Thaiana Lima:** É.

**Leonardo de Melo:** não tem nada impedindo para fazer o encaminhamento.

**Thaiana Lima:** Então é isso,

**Leonardo de Melo:** Posso?

**Thaiana Lima:** prossegue e tira mensagem de erro nessa situação.

**Felipe Martins Costa Brito:** Isso.

**Leonardo de Melo:** Beleza? E aí seria isso. Essas foram minhas minha som.

### 01:43:45

**Leonardo de Melo:** M.

**Alexandre Donnelly Vaz:** Boa tarde, pessoal. Eu vou esperar o Anderson voltar para apresentar, mas vou só adiantar aqui.

**Emerson Yamamoto:** Já voltei, Alexandre. Pode seguir só,

**Alexandre Donnelly Vaz:** Beleza.

**Emerson Yamamoto:** só rapidinho.

**Alexandre Donnelly Vaz:** Eh,

**Emerson Yamamoto:** Alexandre, como é que ficou? Desculpa que eu tive que sair rapidinho a questão lá de ele não não encaminhar que você tinha falado.

**Thaiana Lima:** A gente sempre encaminha. Se não conseguir criar o caso, é só não criar o caso e nem dar mensagem de erro. Fica no encaminhamento.

**Emerson Yamamoto:** Ah, tá. Então não mostra mensagem de erro nenhuma, só não vai criar o caso, né?

**Thaiana Lima:** Isso não vai criar o caso. chegar só no final do encammento com sucesso. F.

**Emerson Yamamoto:** Tá, vou anotar aqui então. Valeu. Vai lá, Alexandre.

**Alexandre Donnelly Vaz:** Beleza. A primeira que eu vou apresentar é essa de alterar a consulta de órgão eh de liberto para agora. Agora vai ter o parâmetro de RG. Então, antes só tinha o identificador da pessoa presa que é o IDCAP, né?

### 01:45:21

**Alexandre Donnelly Vaz:** Agora a gente vai poder passar o próprio RG direto na consulta. Eh, vou mostrar aqui como ficou. Não tem esse parâmetro aqui que já existia de DCAP, agora existe o de RG. Então aqui eu já tinha montado, a gente mudou a documentação também para explicar tudo isso. Eh, tem esse RG aqui fictício. Basicamente ele usa o penúltimo caractere, né? para identificar para qual órgão eh o assistido vai ser encaminhado. Então, essa regra tá definida em uma eixo antiga que fala verificar o órgão para atendimento segundo a regia da pessoa presa. O órgão a ser retornado deve ser selecionado de acordo com o número anterior ao dito da RG, é o penúltimo distito, né? Então, por exemplo, nesse RG aqui, penúltimo, eh, set, aí segue o mapeamento de órgão em RG. No exemplo que eu tô usando, tem o dígito C, então ele cai nessa regra aqui de terceira DP de execuções penais. Se eu rodar a consulta, ele vai paraa terceira DP de execuções penais.

### 01:46:51

**Emerson Yamamoto:** Uma coisa que eu notei,

**Alexandre Donnelly Vaz:** Esse é o parâmetro novo.

**Emerson Yamamoto:** Alexandre, é que lá no appetorna os dois órgãos e aqui a regra diz para não retornar nenhum se tiver empate, né? No caso do seis ali do final seis.

**Alexandre Donnelly Vaz:** Ja.

**Emerson Yamamoto:** Isso é meio estranho, não é não, Taiana? Porque se for seis nunca vai ter atendimento para esse cara.

**Thaiana Lima:** Como assim? Nunca vai ter. Tem tem dois órgãos aqui, né?

**Emerson Yamamoto:** É só que tá dizendo ali que se houver mais de um órgão não retornar resultado.

**Thaiana Lima:** Tipo, a gente perdi essa de onde vocês vieram.

**Felipe Martins Costa Brito:** Mas é um órgão só, não é?

**Emerson Yamamoto:** Não, porque o terceira DP atende final seis e a quinta DP também.

**Alexandre Donnelly Vaz:** Isso daqui já tá em produção, mas eu eu não lembro o motivo, mas a gente desculpa.

**Felipe Martins Costa Brito:** Deixa eu só confirmar. Acho que essa regra mudou. Pode, pode seguindo aí. Depois eu eu falo se for o caso.

### 01:47:53

**Felipe Martins Costa Brito:** A Taiana vai reescreve alguma coisa.

**Emerson Yamamoto:** Tá.

**Felipe Martins Costa Brito:** Só olha

**Emerson Yamamoto:** É porque é estranho assim em produção são hoje se o cara tiver RG6 não tem atendimento para ele porque vão

**Alexandre Donnelly Vaz:** É, eu passo

**Emerson Yamamoto:** selecionar mais de um órgão que até o Alexandre até pode fazer esse teste aí. Se ele botar seis aí vai dar ruim, vai dizer que não tem atendimento,

**Alexandre Donnelly Vaz:** é, não tem.

**Emerson Yamamoto:** vai. Não faz menor sentido,

**Alexandre Donnelly Vaz:** É, se eu pegar outro ambiente.

**Emerson Yamamoto:** né?

**Alexandre Donnelly Vaz:** Não sei se aqui vai. Isso aqui é uma homologação. Vamos ver. Ah, mas eu teria que pegar pelo IDC.

**Emerson Yamamoto:** É, não dá. Teria que ter pelo DCAP.

**Alexandre Donnelly Vaz:** É, demoraria um pouquinho para eu montar esse exemplo, mas sim, ele já tá assim em produção. A única mudança foi adicionar esse parâmetro de RG.

**Felipe Martins Costa Brito:** Não, veja bem, não acho ruim a regra. A regra eu acho que tá certa e não vai transbordar pro

### 01:48:39

**Emerson Yamamoto:** Mas nunca teria atendimento para ele, ô Felipe.

**Alexandre Donnelly Vaz:** M.

**Felipe Martins Costa Brito:** humano,

**Emerson Yamamoto:** Ah, tá,

**Felipe Martins Costa Brito:** mas eu acho que essa regra da mudou da execução penal.

**Emerson Yamamoto:** entendi. Já são outros números.

**Felipe Martins Costa Brito:** Eu acho que sim.

**Emerson Yamamoto:** E no app faz sentido? Tentão retornar os dois e ele escolher ali aleatório, Felipe.

**Felipe Martins Costa Brito:** Porque não tem com quem ele falar no app, né?

**Emerson Yamamoto:** Ah, entendi. É, mandaria para 29, né?

**Felipe Martins Costa Brito:** Não, não, não. Esquece.

**Emerson Yamamoto:** Aí já é demais,

**Felipe Martins Costa Brito:** É.

**Emerson Yamamoto:** saquei. Tá bom. Não, só só surgi essa dúvida porque o comportamento é diferente, mas tranquilo. Então, vai lá, Alexandre, segue aí.

**Alexandre Donnelly Vaz:** Beleza. Aí aqui eu tenho o exemplo de um assistido com RG certificado no verde, cujo penúltimo disco é um. Vou copiar aqui o IDCAP dele. Vai ser apenado. O penúltimo dígará um.

### 01:49:43

**Alexandre Donnelly Vaz:** Se eu vier aqui na nessa eixo atendimento aos com final de RG1 e 2 é na primeira DP de execuções penais, então tá correto. E aí se eu passar um RG, é, esses parâmetros são eh mutuamente exclusivos. Então se eu preencher os dois parâmetros, ele informa que os parâmetros são mutuamente exclusivos. É isso. Essa isso cobre todos os cenários dessa tarefa aqui. Eh, a outra que eu tenho também relacionada ao RG do Riberto é alterar o encaminhamento armazenando RG do Ru liberto. Eh, basicamente a gente tem um novo parâmetro no fluxo de encaminhar no de encaminhamento prisional. E se parâmetro for informado, a gente armaena essa informação diretamente no encaminhamento e também na observação do encaminhamento. Então,

**Felipe Martins Costa Brito:** Eh, desculpa, Alexandre. Achei aqui a regra. Taiana, minha filha, mudou mesmo, hein?

**Thaiana Lima:** mapeamento mudou.

**Felipe Martins Costa Brito:** Mudou. Meio que excluiu a sexta.

**Thaiana Lima:** É, então tem que trocar. Ah, em todas as os canais

### 01:51:00

**Felipe Martins Costa Brito:** É, tá assim.

**Emerson Yamamoto:** excluiu o dígito seis ou ah,

**Felipe Martins Costa Brito:** Não, não excluiu a sexta DP. Ficou assim. Primeira DP 1 e 2, segunda 3 e 4, terceira 5 e 6, quarta 78 e quinta 90. O que é?

**Emerson Yamamoto:** excluiu seis na quinta.

**Felipe Martins Costa Brito:** Eh,

**Emerson Yamamoto:** Entendi. É, faz mais sentido,

**Thaiana Lima:** Isso,

**Felipe Martins Costa Brito:** tá assistindo.

**Emerson Yamamoto:** né?

**Felipe Martins Costa Brito:** Exatamente.

**Thaiana Lima:** isso não é unificado, né? Mas cada lugar tá com seu mapeamento guardado.

**Emerson Yamamoto:** Ah, com certeza não.

**Felipe Martins Costa Brito:** Isso é o que?

**Thaiana Lima:** Certeza.

**Felipe Martins Costa Brito:** Fala aí.

**Thaiana Lima:** Não é unificado.

**Emerson Yamamoto:** Oi.

**Thaiana Lima:** Cada lugar vai ter que alterar.

**Emerson Yamamoto:** Carrega.

**Felipe Martins Costa Brito:** É,

**Thaiana Lima:** ou a gente passa a unificar de alguma forma configuração,

**Felipe Martins Costa Brito:** é. Não, que que eu acho é acho que a gente tem que unificar, mas agora a gente já podia corrigir essa is

### 01:51:41

**Emerson Yamamoto:** Sim. Tá bom.

**Thaiana Lima:** tá? M.

**Emerson Yamamoto:** As duas, né? Eu acho que a do a do do app também, né? Ô, Leobardo, a gente faz isso também, né?

**Leonardo de Melo:** Sim, mas acho que não é porque a gente retorna os dois.

**Emerson Yamamoto:** retorna. Ah, é no app retorna os dois, mas mesmo assim tem que deixar de retornar quando for seis e ele retornar a quinta, né?

**Felipe Martins Costa Brito:** se se tiver oportunidade de já mexer nisso, já mexe. Eu até botei aí como é que tá

**Emerson Yamamoto:** Tá.

**Thaiana Lima:** Então o final é já perguntar o final seis ele saiu da quinta,

**Felipe Martins Costa Brito:** isso.

**Thaiana Lima:** ficou só na na terceira,

**Emerson Yamamoto:** Eu

**Felipe Martins Costa Brito:** É.

**Thaiana Lima:** tá? Yeah.

**Felipe Martins Costa Brito:** E aí, Tina com muita calma, faz uma revisão de tudo. Так.

**Emerson Yamamoto:** vou botar aqui, tá, Alexandre? Remover final 6 da quinta DP. Acho que dá para entender, né?

**Alexandre Donnelly Vaz:** Sim, sim.

### 01:52:41

**Emerson Yamamoto:** Beleza.

**Alexandre Donnelly Vaz:** Eh, beleza. Agora isso que eu ia tava apresentando é de incluir parâmetro de RG no fluxo prisional de encaminhamento. Então, já tenho uma um exemplo pronto aqui. Eh, a gente também melhorou a documentação aqui. Seria o fluxo prisional. Eh, agora tem parâmetro opcional de RG. E na ausência de um RG informado num corpo da requisição é utilizado o RG informado no cadastro da sua presa no verde,

**Emerson Yamamoto:** Так.

**Alexandre Donnelly Vaz:** que é algo que já acontecia, né? Se se a gente não identificar diretamente o RG do Reiberto, é usado o RG formado na eh na no cadastro da pessoa presa, tá? Então eu vou fazer um encaminhamento aqui informando o RG de Re Liberto, terminando em 0,90. Eh, gerou um encaminhamento com esse identificador aqui. Copiar e colar na visualização de encaminhamento. Aqui nós podemos observar que o Zorg RG que eu informei aqui terminando em 0,90 no na observação do encaminhamento. E ah, Emerson, tem aquela questão da discrepância na

### 01:54:30

**Emerson Yamamoto:** É, eu falei sobre isso já eh ficou decidido que o verde vai remover a parte de pessoa presa quando for real liberto.

**Alexandre Donnelly Vaz:** tá,

**Emerson Yamamoto:** Então não vai dar mais esse problema.

**Alexandre Donnelly Vaz:** tá, mas no encaminhamento, se eu pegar aqui, eh, Tô consultando pelo caminamento que eu acabei de gerar. Agora tá salvando esse no RG Real Liberto, um campo novo, salvando direitinho. E se eu fazer o a mesma requisição sem passar

**Emerson Yamamoto:** О.

**Alexandre Donnelly Vaz:** esse eh parâmetro opcional de RG do R liberto também funciona. Gerou outro encaminhamento. É assim que já tá em produção, né? gerou outro encaminhamento. Eh, vou mostrar aqui que o RG eu tenho nesse cadastro de assistido que eu usei termina em 0,50, né? E o da sua empresa é é esse aqui. Terminando observação, tá usando o RG da pessoa presa mesmo, como já era feito e o encaminhamento ele não salva. Salva só se eu passar o parâmetro lá na requisição

### 01:56:37

**Emerson Yamamoto:** Então, mas tô achando que a gente vai salvar sempre agora, Alexandre. Foi isso que foi decidido no app. Eu acho que aqui a gente vai ter que fazer isso também.

**Alexandre Donnelly Vaz:** também,

**Emerson Yamamoto:** É,

**Alexandre Donnelly Vaz:** mesmo que não seja. É, tá,

**Emerson Yamamoto:** mesmo que não seja representante, que aí esse campo fica centralizado, entendeu? Ok.

**Alexandre Donnelly Vaz:** tá bom. É isso. Alguma dúvida da?

**Thaiana Lima:** Deixa eu só lembrar, Felipe, que a solução pro chatbot passa uma parte na API, uma parte no fluxo. Como a gente não tem controle do fluxo, a Tik vai ter que alterar para consultar parte do processo, fazer a pergunta lá, ver se ele é R, fazer a pergunta se ele é representante, capturar esse RG e passar pra gente por API. Então, depois que a API tiver eh liberada, a gente tem que conversar com a TI para ela alterar o fluxo,

**Felipe Martins Costa Brito:** Tá. E aí tu nota isso aí em algum lugar,

**Thaiana Lima:** tá?

### 01:57:46

**Felipe Martins Costa Brito:** né? Para gente não

**Thaiana Lima:** É, você tem que saber quando quando foi liberado.

**Emerson Yamamoto:** Quando subir, né?

**Thaiana Lima:** É,

**Emerson Yamamoto:** Quando subir a gente vai sa quando não quando subir,

**Thaiana Lima:** quando subir

**Emerson Yamamoto:** né? Mas antes de subir a gente vai saber. Ah, isso aqui afeta ti,

**Felipe Martins Costa Brito:** tá.

**Emerson Yamamoto:** tem que passar para ele.

**Thaiana Lima:** tem que me avis me avisar para para eu falar com Pode.

**Emerson Yamamoto:** Sim. Inclusive, Felipe, foi até bom ter falado isso, a gente vai subir uma versão, tá preparando, né? Uma subida de versão grande da Integra, com bastante coisa que foi desenvolvida. E aí, provavelmente vai acontecer isso. Eu vou, eu tô avaliando aqui o que que afeta ou não aik vai ter que mudar fluxo.

**Felipe Martins Costa Brito:** Deve ter que mudar fluxo, né?

**Emerson Yamamoto:** Exatamente. Tem bastante coisa. Depois eu vou passar essa lista lá pro pessoal da Defensoria e para você, pra gente ver o que que vai precisar ser alterado.

### 01:58:27

**Felipe Martins Costa Brito:** Não.

**Emerson Yamamoto:** Beleza. Acho que agora só falta o Farias, né, Farias? Vamos lá.

**Lucas Farias:** Isso. Boa tarde, pessoal. Vou começar pela 10717, que é de alterar a consulta de processo da Integra API para verificar o tipo da parte. Então, no end point de processo que a gente tem atualmente, agora tem um campo novo, que é esse de pessoa aqui, e a gente vai verificar eh se essa pessoa ela é parte do processo e se for retornar qual é o tipo da parte dela entre autor e ré. Então, vou mostrar aqui primeiro consultar um processo sem enviar esse campo, só pra gente ver que o campo de tipo da parte ele não é retornado nesses casos. Ele só possa ser retornado quando quando eu informo esse campo de ID pessoa, que nesse caso aqui ele não trouxe nenhum campo de tipo parte. Essa é a consulta normal que a gente já tem hoje em produção, né? E agora eu vou passar uma pessoa, um ID de pessoa, só que essa pessoa ela não é parte do processo.

### 01:59:58

**Lucas Farias:** Então, nesse caso, a gente retorna não encontrado como no campo tipo parte. aqui ele ficou como não encontrado. É, vou passar agora uma pessoa que é autor, autora.

**Emerson Yamamoto:** Isso foi até uma coisa que a gente mudou por conta, Thaiana, que é a questão de quando ela não é autora R. A gente não tá colocando exatamente o nome, a gente tá colocando outro. Será que é importante colocar? É porque não necessariamente esses tipos batem com os tipos do verde, né?

**Lucas Farias:** É, é na is foi pedido só autor e ré e aí a gente acabou colocando outros quando não é nenhum desses tipos.

**Emerson Yamamoto:** É quando é outros.

**Thaiana Lima:** Não, porque negócio flexível depois pode usar para outra coisa, mas faz sentido só pra gente nesse momento ser outros. Yeah.

**Emerson Yamamoto:** Caraca, eu ouvi, mas deu uma bugadona aqui para mim.

**Lucas Farias:** aqui também, mas deu para entender.

**Emerson Yamamoto:** Deu para entender. Deu para entender. Valeu.

**Lucas Farias:** É,

**Emerson Yamamoto:** Obrigado,

**Lucas Farias:** beleza. Aqui nesse caso eu posso ser um autor, então ele retornou o autor aqui como tipo da parte.

### 02:01:27

**Lucas Farias:** E agora eu vou passar um réu. Agora ele retornou o ré aqui. E por eh por último vou passar um um processo que ele não é consultado com sucesso, só pra gente ver que a gente decidiu não deixar o não encontrado aqui nesses casos, porque pode ser que ele a pessoa seja de fato uma parte no processo, mas ele não foi consultado com sucesso e o não encontrado poderia eh acabar gerando um uma confusão, né? Então, nesses casos, a gente deixou esse erro consulta retornando, só pra gente saber que foi eh o processo não foi consultado, então por isso não foi possível identificar qual é o tipo da parte da pessoa informada, que nesses casos a gente até retorna o processo aqui, como a gente pode ver, mas é porque ele já existe no nosso banco, né? Então a gente retorna as informações que a gente tem no banco, mas como ele não foi consultado, a gente não consegue consultar as partes também. Então, deixamos esse erro consulta aqui do tipo da parte.

**Emerson Yamamoto:** Show. Mais uma dúvida, Faria.

### 02:02:48

**Emerson Yamamoto:** Se eu não passar, ele não traz tipo de parte, né? Tipo, se eu não passar a pessoa.

**Lucas Farias:** É,

**Emerson Yamamoto:** Ah, tá.

**Lucas Farias:** ess é se não informar o ID pessoa ele não retorna.

**Emerson Yamamoto:** Saquei.

**Lucas Farias:** E aí, Por eh por último não tem um exemplo que é bem difícil de encontrar, mas eu ia falar só isso que o Emerson comentou, que quando a pessoa for um outro tipo que não seja ator e ré, né, se for vítima, testemunha, alguma coisa assim, a gente deixou esse outros aqui retornando, só pra gente não ter um não encontrado, né, porque a pessoa é de fato uma parte do processo. Então a gente retornou esse outros.

**Emerson Yamamoto:** Show.

**Lucas Farias:** Beleza?

**Emerson Yamamoto:** Maravilha. Tranquilo, pessoal. Show de bola. Aí vamos paraa última agora que é da Verde API, né?

**Lucas Farias:** É cidadão é PI, na verdade.

**Emerson Yamamoto:** Ah, é. Caraca, verdade.

**Lucas Farias:** Eh, é essa é a da rotina, né, que chamam o end point de de criar um encaminhamento e de encaminhamento comum e enviar o e-mail pro usuário.

### 02:04:02

**Lucas Farias:** Aqui a gente fez umas modificações no e-mail desse end point. Então agora foi removido o modelo que era utilizado antes pro e-mail e foi criado um novo com esse texto aqui.

**Emerson Yamamoto:** Вот.

**Lucas Farias:** Eh, vou mostrar para vocês melhor quando eu enviar o e-mail e algumas regras a mais. Então eu vou chamar esse end point, né? Primeiro, ele, uma das regras, inclusive é sobre o horário de atendimento comum, né? Quando houver horário para aquele órgão, horário de atendimento para aquele órgão, ele vai passar a mostrar o ele vai mostrar o o dia de atendimento do horário de atendimento comum e caso não tenha, ele mostra os de urgência, né? Se houver também. Então eu preparei primeiro um exemplo passando aqui um imóvel que ele possui horário de atendimento comum e não de urgência. Então eu vou mostrar aqui como fica inicialmente. Vou chamar o end point. Beleza? Ele gerou o encaminhamento, enviou a mensagem. Aí eu vou no e-mail aqui que eu preparei aqui. Chegou e ficou dessa forma, né?

### 02:05:22

**Lucas Farias:** O cabeçalho e o rodapé são os mesmos do e-mail. Opa. O cabeçá e o rodapé são os mesmos do e-mail. O que mudou foi apenas o corpo. Aqui a gente passou a mostrar agora. Considerando que não houve resposta à sua solicitação pelo núcleo digital de petições iniciais, que foi o órgão que eu enviei na end point, solicitamos que compareça a Defensoria Pública no seguinte endereço. Aí aqui a gente apresenta o endereço do órgão e o G.

**Emerson Yamamoto:** Esse não é um bom exemplo, porque só só explicando, né?

**Lucas Farias:** Hum.

**Emerson Yamamoto:** Porque eu acho que esse ócul não recebe mos mensagem,

**Lucas Farias:** É,

**Emerson Yamamoto:** mas é só é só um exemplo mesmo,

**Lucas Farias:** eu peguei um aleatório.

**Emerson Yamamoto:** tá, pessoal? Pode ser o seria outro órgão, no caso.

**Lucas Farias:** Sim, sim. É, eu peguei o encontrei o primeiro o primeiro órgão que retornasse um um horário e eu pudesse usar como outros exemplos e aí acabei usando ele.

**Emerson Yamamoto:** Sim, sim. Ah, de boa.

**Lucas Farias:** Mas é isso.

### 02:06:18

**Lucas Farias:** E aí a gente mostrou aqui o dias, os dias e horários de atendimento também. Aqui ele mostrou o horário de funcionamento, que é um de atendimento comum, e o resto do e-mail é da mesma forma que os outros do app, né, como eu falei. Agora eu vou preparar um, vou mostrar um outro exemplo. Eh, vou tirar esse ID, escolher o ID do imóvel. Aí ele vai passar a olhar pro endereço do órgão. E nesse caso, o endereço do órgão, ele não tem horários de atendimento comuns, né? Então ele vai enviar só os urgentes usando o mesmo órgão. Aqui agora ele já ele mudou o endereço, passou a olhar o endereço do órgão mesmo e nos dias horários de atendimento ele passou a retornar aqui os horários urgentes, né, como foi pedido. E uma outra regra é que quando a gente não houver um endereço associado ao órgão, a gente vai alterar essa mensagem para, considerando que não houve resposta à sua solicitação pelo órgão, solicitamos que entre em contato com a central de relaçamento com o cidadão, ligando os 29 para verificar a possibilidade do seu atendimento presencial.

### 02:07:45

**Lucas Farias:** Então aqui eu peguei um outro órgão que ele não tem endereço cadastrado, então é o que vai cair, fazer cair naquela mensagem ali que eu mostrei. Beleza? Aqui nesse caso, ele já mandou uma mensagem agora. aquela eh solicitando para entrar em contato contato com a CRC, ligando um 29. E uma outra regra também da ISS é que o encaminhamento deve ser criado com tipo de atendimento presencial, só que esse tipo, na verdade, ele já está sendo setado no encaminhamento. Os encaminhamentos já estão desse ind point, né? já estão sendo criados com esse tipo. Então, essa parte aqui a gente não chegou a alterar, mas eu posso mostrar aqui para vocês, só para ter certeza. Vou buscar esse caso no verde. E aqui dá para ver quando ele cria o movimento, né, que ele coloca o tipo do encaminhamento aqui. Esse encaminhamento de hoje, encaminhamento presencial. Beleza? Aí acho que é isso dessa ISS.

**Emerson Yamamoto:** Basicamente aí o e-mail ele não era específico, né? Eu acho que era um e-mail reaproveitado do encaminhamento comum.

### 02:09:16

**Emerson Yamamoto:** Então acho que não tinha essa questão de dizendo que não houve resposta. Não sei se a Taiana tá aí, mas eu acho que era isso a mudança desse meio principal, né?

**Lucas Farias:** É, era o mesmo e-mail utilizado nos dois.

**Emerson Yamamoto:** no encaminhamento normal, né? E e nesse aí,

**Lucas Farias:** Isso,

**Emerson Yamamoto:** né?

**Lucas Farias:** isso.

**Emerson Yamamoto:** Entendi. Beleza. Acho que é isso, né?

**Lucas Farias:** É, fechou.

**Emerson Yamamoto:** Show. Então, fechou, pessoal. Bom, fechamos nossa apresentação. Acho que o principal ponto aí de atenção, eh, realmente foi aquela issues que que a gente pergunta ali o tipo de atendimento remoto presencial que a gente realmente vai ter que mudar bastante para passar isso para depois da escolha do órgão, como é no primeiro atendimento. Então, fluxo de real liberto eh prisional e violência doméstica, a gente vai ter que fazer essa alteração, tá? Então vai ser uma alteração maiorzinha, mas vamos lá. Eu acho que vai dar para abrir do jeito que a Taiana pensou, só vai ficar um pouco apertado.

### 02:10:21

**Emerson Yamamoto:** Vamos ver como é que vai ser. E eu estarei de férias nessa apresentação aí, então conto com minha equipe.

**Thaiana Lima:** Vamos lá então. M.

**Yann Naylor Francisco:** Quando quando quando é a próxima

**Emerson Yamamoto:** Eu acho que vai ser dia 8, né? 1 2 3. Acredito que seja seja por ali.

**Yann Naylor Francisco:** 5 7 8 15 dias,

**Emerson Yamamoto:** Eu não sei se é o dia da nossa fraternização.

**Yann Naylor Francisco:** né? 8 9,

**Emerson Yamamoto:** Tu lembra, Tan, no dia da confraternização?

**Yann Naylor Francisco:** né?

**Emerson Yamamoto:** Não lembro.

**Thaiana Lima:** Acho que é dia 7.

**Emerson Yamamoto:** Ah, tá. Nossa, que dia, hein? De o pós o dia seguinte. Beleza, pode ser.

**Yann Naylor Francisco:** Oit,

**Emerson Yamamoto:** Mas vamos fazer a abertura.

**Yann Naylor Francisco:** oito. Tá livre, tá? Eh, só abertura. Eu não sei se a Taiana tava quando eu comentei, Camila não conseguiu participar porque ela tá voltando de viagens, mas ela, acho que ela já até adiantou com o Gustavo, não sei se o Gustavo adiantou com você, tá, né?

### 02:11:30

**Yann Naylor Francisco:** sobre o principal foco em relação ao pré-atendimento, eh, pré-atendimento varas e principalmente na nas que o Braida tá precisando. Ne.

**Thaiana Lima:** Então eu eh eu não participei dessa parte, mas é que a Talita colocou aqui issues de Maria Atendimento. Então tô entendendo que seria o que o BR tá precisando,

**Emerson Yamamoto:** Ja.

**Thaiana Lima:** porque a Integra PIP Maria atendimento.

**Emerson Yamamoto:** É isso sim.

**Thaiana Lima:** Então eu selecionei todas elas, todas que a criou, essas aqui mais essa do WhatsApp já estão selecionadas. Eh, assim, a gente tem volta de 30 até 40 pontos, dependendo do que a gente selecionar aqui, né? com todas essas selecionadas, mas essas primeiras aqui que eu já tinha conversado com o Felipe, mais ou menos a ordem de de prioridade dele, essas três elas travam a isto do verde. O verde não consegue fazer com alteração de endereço,

**Emerson Yamamoto:** M.

**Thaiana Lima:** é porque ele não consegue notificar as pessoas. Então, alterar o endereço de um ajendamento sem presencial, né, sem avisar as pessoas é perigoso. Então, tem que fazer isso aqui primeiro para liberar o verde.

### 02:12:47

**Thaiana Lima:** E aí a seguinte não vai caber, né, que são oito pontos, então selecionei essa aqui de dois pra gente iniciar. Então, dariam 35 pontos essas três notificações, e-mail, notificação aplicativo e notificação WhatsApp. exibir o link do Google Meet no agendamento interno, caso o órgão coloque. Aí vem as as todas da Talita, dão 35 pontos pra gente completar, eh, eu coloquei essas três que foi algo que a tinha esquecido de colocar fora da CRC, né? A CRC já foi feita, que é aquela questão do queamento da corregedoria. né? Acho que foi, você que passou na reunião de quarta ou Dr. Anderson, que a corregedoria não quer receber encaminhamento, né,

**Yann Naylor Francisco:** Угуm.

**Thaiana Lima:** por ela estar associada ao caso.

**Yann Naylor Francisco:** Yeah.

**Thaiana Lima:** Então, CRC foi resolvido, mas ficou faltando aqui e API. Como são coisas parecidas que a gente já fez com os PEN, com outras questões, eu coloquei aqui pra gente fazer de bônus. Então, completando máximo 40, eh, a gente pegaria isso aqui, tá?

**Yann Naylor Francisco:** Beleza.

**Thaiana Lima:** Então, só ficaria de fora essa aqui que é mandar do do aplicativo para o WhatsApp do do da CRC.

### 02:14:00

**Thaiana Lima:** É bom que a gente tem mais um tempo para atender se a Luna pegou certinho que a gente queria. E essa aqui da de atualização da da PI que a Luna também tinha pedido um tempo atrás. Tudo bem, Felipe Ian?

**Yann Naylor Francisco:** Tudo bem? Tudo bem. Você tem como me passar? Eu eu quero ver. Eu vou tirar um print. Na verdade, na tela tá exibindo todas.

**Thaiana Lima:** Então deixa não,

**Emerson Yamamoto:** Tu tem o link,

**Thaiana Lima:** deixa só.

**Emerson Yamamoto:** pô?

**Thaiana Lima:** É,

**Emerson Yamamoto:** Tu tem o link dessa planilha?

**Thaiana Lima:** tô tem um link te passar

**Emerson Yamamoto:** Entra nela lá.

**Yann Naylor Francisco:** É, eu tenho.

**Emerson Yamamoto:** Não tem não.

**Yann Naylor Francisco:** É só eu achar.

**Thaiana Lima:** aqui.

**Yann Naylor Francisco:** Eu sempre acesso quando eu vou Molagar,

**Thaiana Lima:** Vou te passar aqui,

**Emerson Yamamoto:** Manda aqui no A gente manda aqui.

**Yann Naylor Francisco:** entendeu? Mas manda aí.

**Emerson Yamamoto:** Aí tu já vai ver direto lá.

**Thaiana Lima:** ó.

### 02:14:40

**Thaiana Lima:** Mandei aí.

**Yann Naylor Francisco:** Valeu. Melhor ainda.

**Thaiana Lima:** Essas estão sem números.

**Yann Naylor Francisco:** Obrigado.

**Thaiana Lima:** Acho que ela vai cadastrar no Git ainda, mas então os títulos estão aqui,

**Yann Naylor Francisco:** Certo. Para mim tá certo.

**Thaiana Lima:** tá?

**Yann Naylor Francisco:** confirmado que essas eh, de baixo, Acho que a Talita incluiu são as do Braida,

**Emerson Yamamoto:** Sim,

**Yann Naylor Francisco:** né?

**Emerson Yamamoto:** com certeza.

**Yann Naylor Francisco:** Ô, então Emerson falou, tá assim, tá assinando em B.

**Thaiana Lima:** Estamos todos confiados.

**Emerson Yamamoto:** Não foi porque a gente discutiu isso,

**Yann Naylor Francisco:** Tô confiando de fechado.

**Emerson Yamamoto:** pô. Eu discuti com a Talita. Isso foi sim.

**Yann Naylor Francisco:** Beleza, então. Tranquilo,

**Thaiana Lima:** Tá beleza.

**Yann Naylor Francisco:** tudo certo. Vamos para pra data então, dia 8 mesmo.

**Emerson Yamamoto:** Acho que é oito, né? Uma semana depois da sprint do verde.

**Felipe Martins Costa Brito:** oito. Pode ser que a gente não tem expediente,

**Yann Naylor Francisco:** Dia 8 na dia 8 não tem expediente.

### 02:15:40

**Felipe Martins Costa Brito:** pode ser,

**Yann Naylor Francisco:** Por quê?

**Felipe Martins Costa Brito:** porque geralmente é dia da justiça, cada ano é de um jeito. Tem ano que a gente funciona só a parte administrativa,

**Emerson Yamamoto:** Ah,

**Felipe Martins Costa Brito:** tem ano que não funciona nada.

**Emerson Yamamoto:** joga nove, então aí, ó.

**Yann Naylor Francisco:** É sempre bom ter um cara aí, ó, que cuida dos feriados. Sempre é bom. O Lucas tá com fala aí,

**Emerson Yamamoto:** Lucas.

**Lucas de Oliveira Mol Silva:** Eu acho que pode valer a pena comentar, Emerson, que eu também vou estar de férias nesse período e aí talvez papi,

**Emerson Yamamoto:** Ah,

**Lucas de Oliveira Mol Silva:** fica puxado,

**Emerson Yamamoto:** não.

**Lucas de Oliveira Mol Silva:** só o Leo Bardo ficar sozinho aí da parte do app, não sei, talvez.

**Emerson Yamamoto:** É verdade. Tu entra dia 7, pelo que eu tô vendo aqui, né?

**Lucas de Oliveira Mol Silva:** Exatamente.

**Emerson Yamamoto:** É, mas não vai ter muito jeito não, porque senão a gente teria que trazer para antes. Vai perder,

**Lucas de Oliveira Mol Silva:** Éí, tá tá bastante coisa,

### 02:16:24

**Emerson Yamamoto:** vai perder dia,

**Lucas de Oliveira Mol Silva:** né?

**Emerson Yamamoto:** tem muita coisa. É, não vai ter jeito não. O tu a gente a vê com Leobardo aí com o pessoal de apresentar tuas issas, porque como tu entra só dia 7, tu vai participar da sprint inteira praticamente.

**Lucas de Oliveira Mol Silva:** Sim, é só na só entrega aqui.

**Emerson Yamamoto:** É, não, aí é de boa a gente vê pessoal de apresentar tua parte aí.

**Lucas de Oliveira Mol Silva:** Tá beleza.

**Emerson Yamamoto:** Até tu passa pro pessoal de talvez Gabriel, Marcos, eles ajudam também. Então pode ser dia 9 an, se for o caso. Aí é mesmo horário de

**Yann Naylor Francisco:** Fechou. Dia 9 na parte da tarde.

**Emerson Yamamoto:** sempre.

**Yann Naylor Francisco:** Show de bola. Tô então remarcando aqui, pessoal. 2 Oi.

**Emerson Yamamoto:** Maravilha.

**Yann Naylor Francisco:** Enviado, pessoal. Obrigado. Parabéns aí,

**Emerson Yamamoto:** É isso.

**Yann Naylor Francisco:** viu?

**Emerson Yamamoto:** Valeu, pessoal.

**Leonardo de Melo:** pessoal.

**Emerson Yamamoto:** Eh, Ian e Felipe, depois eu mando para vocês eh a seleção que eu fiz de issues da Integra P, o que que vai afetar, enfim, teve issue do Felipe, teve issue que o Ícaro tinha pedido também, tem uma uma seleção aqui, eu vou só organizar e mando para vocês, beleza? É isso. Valeu, pessoal. Obrigado também.

**Yann Naylor Francisco:** Valeu,

**Lucas de Oliveira Mol Silva:** Valeu,

**Emerson Yamamoto:** Ciao. Ciao.

**Lucas de Oliveira Mol Silva:** pessoal. M. Yeah.

**Thaiana Lima:** Ciao ciao.

**Yann Naylor Francisco:** valeu, valeu,

**Thaiana Lima:** M.

**Yann Naylor Francisco:** pessoal.

**Alexandre Donnelly Vaz:** Поче Что?

**Yann Naylor Francisco:** na hora.
