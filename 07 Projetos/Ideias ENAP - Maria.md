---
tipo: ideias
status: ativo
origem: Repositório ENAP (DSpace), metadados de 8.055 obras; resumos lidos em 2026-11-24
envolve_ia: sim
tags:
  - ideias
---

# Ideias ENAP - Maria

> Ideias para a [[Maria - atendimento automatizado]] tiradas de obras do repositório da ENAP. São hipóteses para triagem, não decisões. Refeita em 2026-11-24 a partir dos resumos completos; a versão anterior partia de títulos e trechos. Ideias para a Defensoria fora da Maria: [[Ideias ENAP - Defensoria]].

## Como ler
- **Da obra:** só o que o resumo da obra diz. O handle abre a página da obra no repositório.
- **Nossa interpretação:** leitura do COILAB para a Maria. Precisa ser validada com quem opera o fluxo.
- **Viabilidade:** alta (dá para fazer com o que já temos), média (depende de outra área, da Tykhe ou de um dado que não conferimos), baixa (depende de norma, contrato ou parceiro externo).
- **Esforço:** P (dias), M (semanas), G (meses).

## Resumo
| # | Ideia | Viabilidade | Esforço | Obras |
|---|---|---|---|---|
| 1 | Mensagens que levam a pessoa a agir, testadas em A/B | alta | P | 1/5221, 1/5220 |
| 2 | Linguagem simples medida em cada texto do catálogo | alta | P | 1/6756, 1/5258, 1/7805 |
| 3 | Mapa de atritos (sludges) de cada fluxo | alta | P a M | 1/9972, 1/9973, 1/9227 |
| 4 | Painel de barreiras: por que o atendimento vai para humano ou para no meio | alta | M | 1/9840, 1/3538 |
| 5 | Teste de acerto e de viés do orquestrador | alta | M | 1/8089, 1/7397, 1/7716 |
| 6 | Implantação no NAD pensada por perfis de servidores | alta | P a M | 1/5222, 1/3404 |
| 7 | Prioridade por critérios explícitos na fila humana | média | M | 1/535, 1/7376 |
| 8 | Plano de saúde: orientar a reclamação na ANS sem tirar o caso do humano | média | P a M | 1/2141, 1/2345, 1/2723 |
| 9 | Indicar o serviço da rede de proteção mais perto | média | M | 1/4146, 1/10131, 1/10141 |
| 10 | Pessoa presa: orientação para a família desde o primeiro contato | média | P a M | 1/6005 |
| 11 | Pesquisa de satisfação curta no fim, com apoio da CINCO/Enap | média | M | 1/9976, 1/9979, 1/9975 |
| 12 | Atendimento por áudio para quem tem dificuldade com texto | média | M a G | 1/9227, 1/8053, 1/3273 |
| 13 | Atendimento em outros idiomas para imigrantes | média | M | 1/3633 |

## Ideias

### 1. Mensagens que levam a pessoa a agir, testadas em A/B
- **Da obra:** [1/5221](https://repositorio.enap.gov.br/handle/1/5221) (2019, relato do (011).lab): o Hospital do Servidor Público Municipal de São Paulo reescreveu, com ciências comportamentais, os roteiros de agendamento e de confirmação de consultas feitos pela central SP156. Uma das versões reduziu as faltas em 12% em média (1,8 ponto percentual). [1/5220](https://repositorio.enap.gov.br/handle/1/5220) (2019): a carta de cobrança do IPTU parcelado foi redesenhada com nudges e testada em experimento aleatório controlado com 15.178 contribuintes. A melhor de cinco versões aumentou a regularização em 8,4%.
- **Nossa interpretação:** aplicar o mesmo método às mensagens da Maria que pedem documento pendente e aos lembretes de agendamento do NAD. Bom ponto de partida: o comprovante de residência, apontado como a causa mais comum de reabertura nos casos de alimentos ([[2026-10-16 - Serviços MarIA - CREDCESTA]]). Sortear quem recebe cada versão do texto e comparar o desfecho, que o sistema já registra.
- **Viabilidade:** alta. Muda texto; falta sortear a versão e guardar qual foi enviada. Lembrete fora da janela de 24 horas do WhatsApp depende da Tykhe (não conferimos).
- **Esforço:** P.

### 2. Linguagem simples medida em cada texto do catálogo
- **Da obra:** [1/6756](https://repositorio.enap.gov.br/handle/1/6756) (2021): caso do Programa Linguagem Simples da Prefeitura de São Paulo, descrito como a primeira política pública brasileira de simplificação da linguagem do governo. [1/5258](https://repositorio.enap.gov.br/handle/1/5258) e [1/5259](https://repositorio.enap.gov.br/handle/1/5259) (2019): guia em 4 passos e 10 dicas para simplificar documentos. [1/7696](https://repositorio.enap.gov.br/handle/1/7696) e [1/7697](https://repositorio.enap.gov.br/handle/1/7697) (2023): passo a passo para oficinas de linguagem simples, virtuais e presenciais. [1/7805](https://repositorio.enap.gov.br/handle/1/7805) (2023): o RegBR calcula métricas sobre normas, entre elas o quanto são linguisticamente complexas.
- **Nossa interpretação:** desde 2026-08-31 as perguntas da Maria têm texto fixo, porque a reescrita por IA foi desligada. Então dá para medir cada texto do catálogo com uma régua simples (tamanho da frase, palavras longas, voz passiva) a cada mudança de fluxo, e mandar para revisão humana o que passar do limite. A régua é nossa: o resumo do RegBR não diz qual métrica usa. Combina com a tarefa [[Guia de Linguagem simples]] e com a revisão de linguagem que o ILEB já fez em fluxos como o do CredCesta ([[2026-10-16 - Serviços MarIA - CREDCESTA]]). As oficinas servem para formar quem escreve fluxo.
- **Viabilidade:** alta. Não precisa de IA nem de dado pessoal.
- **Esforço:** P.

### 3. Mapa de atritos (sludges) de cada fluxo
- **Da obra:** [1/9972](https://repositorio.enap.gov.br/handle/1/9972) (2025) e [1/9973](https://repositorio.enap.gov.br/handle/1/9973) (2026): a CINCO/Enap aplicou o método FCINCO, que identifica e elimina barreiras comportamentais (sludges) em serviços públicos digitais, em duas jornadas do Contrata+Brasil: o cadastro do MEI e a seleção do fornecedor MEI. [1/9227](https://repositorio.enap.gov.br/handle/1/9227) (2025): em 30 entrevistas sobre serviços digitais do governo, os usuários elogiaram a praticidade e não precisar se deslocar, mas apontaram complexidade de navegação, burocracia digital e limites de acessibilidade.
- **Nossa interpretação:** percorrer cada fluxo da Maria (pessoa presa, violência doméstica, padrão e os novos) contando perguntas, pedidos de documento, idas a outro sistema e pontos onde a pessoa desiste. Cortar o que não muda o encaminhamento. Os resumos não descrevem os passos do FCINCO; seria preciso ler os relatórios ou falar com a CINCO.
- **Viabilidade:** alta. O sistema já registra o desfecho de cada atendimento e tem painéis no Grafana.
- **Esforço:** P para mapear, M para mudar os fluxos.

### 4. Painel de barreiras: por que o atendimento vai para humano ou para no meio
- **Da obra:** [1/9840](https://repositorio.enap.gov.br/handle/1/9840) (2026, dissertação): uma amostra de 379 reclamações à Ouvidoria da CAIXA sobre o Auxílio Emergencial foi codificada em categorias de dificuldade de acesso. As barreiras vieram de como o arranjo institucional chegava ao cidadão, dos limites das bases de dados do governo, das validações de segurança e das pendências cadastrais. [1/3538](https://repositorio.enap.gov.br/handle/1/3538) (2018): cada manifestação recebida pela Ouvidoria do STJ em 2017 foi classificada por tema, objeto e sentimento, e os cruzamentos mostraram as causas da insatisfação.
- **Nossa interpretação:** usar categorias parecidas para os motivos de transferência para humano, os abandonos e as reclamações sobre a Maria. Exemplos: Verde fora do ar, dado que não bate com a base, documento faltando, pedido fora do escopo. A IA pode sugerir a categoria do texto livre, com amostra revisada por pessoa; se entrar, atualizar o cadastro da [[Maria]] no inventário. O painel mostra só números agregados, sem relato nem dado pessoal.
- **Viabilidade:** alta. O motivo da transferência já é registrado (não conferimos se todos os fluxos usam as mesmas categorias).
- **Esforço:** M.

### 5. Teste de acerto e de viés do orquestrador
- **Da obra:** [1/8089](https://repositorio.enap.gov.br/handle/1/8089) (2024, policy paper): trata de equidade em IA, isto é, modelos que não discriminem por raça, gênero, idade ou outros atributos sensíveis, e buscou as métricas adequadas para avaliar a equidade de modelos preditivos na saúde materna em São Paulo. [1/7397](https://repositorio.enap.gov.br/handle/1/7397) (2022): a ferramenta Alice, da CGU, classificou itens de editais com taxa de acerto de 99,22% e F1 de 0,92. [1/7716](https://repositorio.enap.gov.br/handle/1/7716) (2023): um modelo BERT ajustado com trechos de leis brasileiras classificou dispositivos de normas do terceiro setor com 94% de precisão.
- **Nossa interpretação:** montar um conjunto de relatos fictícios com o fluxo certo marcado e medir, a cada mudança, quanto o orquestrador acerta, por fluxo e por tipo de escrita (informal, com erro de digitação, curta ou longa). As obras da CGU e do RegBR mostram como reportar acerto; a 1/8089 ajuda a escolher a métrica de equidade. O resultado alimenta o que falta no inventário da [[Maria]]: a Avaliação de Impacto Algorítmico está pendente, e o nível III exige testes formais de mitigação de vieses (art. 6º, III da [[Resolução DPRJ - Política de IA]]). Também dá base para responder a quem contestar uma triagem feita com IA (art. 17).
- **Viabilidade:** alta. O código é nosso e os relatos podem ser fictícios.
- **Esforço:** M.

### 6. Implantação no NAD pensada por perfis de servidores
- **Da obra:** [1/5222](https://repositorio.enap.gov.br/handle/1/5222) (2019): em quatro anos de implantação do processo eletrônico na Prefeitura de São Paulo, a equipe e o (011).lab identificaram 8 perfis de comportamento de servidores diante da mudança e mapearam estratégias para reduzir a resistência e engajar cada perfil. [1/3404](https://repositorio.enap.gov.br/handle/1/3404) (2017, GNova): no SICAF, a gestão depois da implantação foi insuficiente em capacitação, comunicação, controle e monitoramento, engajamento e transparência, e o desenho do sistema não considerava a diversidade dos usuários.
- **Nossa interpretação:** a implantação do NAD encontrou resistência e pedidos de customização individual de petições e ofícios ([[2026-10-16 - Serviços MarIA - CREDCESTA]]). Mapear os perfis de quem recebe o trabalho da Maria (defensores e analistas), ter uma estratégia para cada um e manter a gestão depois da implantação. Conversa com a tarefa [[Curso para o NAD]].
- **Viabilidade:** alta.
- **Esforço:** P para mapear, M para acompanhar.

### 7. Prioridade por critérios explícitos na fila humana
- **Da obra:** [1/535](https://repositorio.enap.gov.br/handle/1/535) (2007, relato premiado): a emergência do Hospital de Clínicas de Porto Alegre implantou protocolo de classificação de risco e criou áreas de acolhimento e de triagem. Com isso, passou a priorizar pacientes graves, com melhora nos indicadores de qualidade. [1/7376](https://repositorio.enap.gov.br/handle/1/7376) (2022): comparação de instrumentos de identificação e avaliação de risco familiar usados no Brasil e fora (SDM, Eligibility Spectrum, Valórame, CTSPC e CAP).
- **Nossa interpretação:** definir com cada núcleo uma tabela curta de sinais de urgência que marca o caso como prioritário na fila humana. Exemplos a validar: cirurgia negada no plano de saúde, ameaça recente na violência doméstica, prisão recente. A regra é fixa e escrita pelo núcleo; a IA não decide prioridade. A cartilha de violência doméstica da Defensoria, que lista sinais de alerta, é uma base ([[2026-10-28 - Reunião MarIA - Violência doméstica]]). Os instrumentos da 1/7376 são de risco familiar e infantil: servem de referência de método, não para copiar.
- **Viabilidade:** média. Não conferimos se a Tykhe ou o atendimento humano conseguem ordenar a fila por prioridade.
- **Esforço:** M.

### 8. Plano de saúde: orientar a reclamação na ANS sem tirar o caso do humano
- **Da obra:** [1/2141](https://repositorio.enap.gov.br/handle/1/2141) (2014, relato premiado) e [1/2345](https://repositorio.enap.gov.br/handle/1/2345) (2015, entrevista): a Notificação de Intermediação Preliminar (NIP) da ANS trata reclamações por negativa de cobertura de plano de saúde. Sem abrir processo administrativo, resolveu 65%, 68,8% e 78,4% das reclamações em 2010, 2011 e 2012. [1/2723](https://repositorio.enap.gov.br/handle/1/2723) (2016, relato premiado): no Consumidor.gov.br, monitorado pela Senacon, Procons, Defensorias e Ministérios Públicos, 80% das reclamações eram solucionadas pelas empresas, em prazo médio de 7 dias; havia 273 empresas, entre elas planos de saúde.
- **Nossa interpretação:** no fluxo de saúde do NUDECON, perguntar se a pessoa já reclamou na ANS e anotar o protocolo para o defensor. Nos casos sem urgência, a Maria também pode explicar como reclamar. É informação a mais: o encaminhamento do fluxo continua igual, e qualquer erro ou falha continua indo para atendimento humano, como já está decidido. O texto precisa ser validado pelo NUDECON ([[Fluxo de saúde do NUDECON]]). Os números são de 2010 a 2016; os atuais não foram conferidos.
- **Viabilidade:** média. Depende do NUDECON.
- **Esforço:** P para o texto, M se o protocolo virar campo do caso.

### 9. Indicar o serviço da rede de proteção mais perto
- **Da obra:** [1/4146](https://repositorio.enap.gov.br/handle/1/4146) (2019, relato premiado): o MOPS, do então MDS, reuniu em mapas os equipamentos públicos (postos de saúde, conselhos tutelares, centros de atendimento à população de rua, entre outros). Antes, o agente do CRAS ou do CREAS precisava manter uma lista atualizada desses locais. Com os dados georreferenciados do Cadastro Único e do Censo, os acessos mensais dobraram (78 mil em junho de 2017). [1/10131](https://repositorio.enap.gov.br/handle/1/10131) (2026): mapeou 137 serviços estaduais de denúncia e acolhimento de vítimas de racismo, com 26 características de cada um e planilha anexa; a maioria fica no Sudeste e no Sul, e o acesso mais comum é presencial. [1/10141](https://repositorio.enap.gov.br/handle/1/10141) (2026): na Casa da Mulher Brasileira de Ceilândia, faltavam responsabilidades e fluxos formalizados entre os órgãos, e as articulações eram informais.
- **Nossa interpretação:** no fluxo de saúde, a Maria já recebe o endereço e confere o município no Verde. Se o endereço chegar também nos outros fluxos (não conferimos), nos casos de violência doméstica e em outros temas em que a Defensoria orienta a rede ela poderia indicar o serviço mais perto (CRAS, CREAS, delegacia especializada, centro de referência) a partir de uma lista oficial mantida por um núcleo, nunca gerada por IA. A 1/10141 e as limitações da 1/10131 (busca na internet, sem visita aos serviços) mostram o risco: lista desatualizada manda a pessoa para o lugar errado. Precisa de dono e de rotina de atualização.
- **Viabilidade:** média. Depende de quem mantém a lista. Não conferimos se o MOPS ainda está no ar.
- **Esforço:** M.

### 10. Pessoa presa: orientação para a família desde o primeiro contato
- **Da obra:** [1/6005](https://repositorio.enap.gov.br/handle/1/6005) (2020, GNova): no projeto Perséfone, sobre busca de pessoas desaparecidas, o momento do registro se mostrou a etapa crucial para intervir. O novo serviço incluiu checklist para o profissional, materiais de orientação e uma estratégia de acompanhamento do caso, com foco no acolhimento dos familiares.
- **Nossa interpretação:** quem usa o fluxo de pessoa presa geralmente é alguém da família. Como no registro do desaparecimento, a primeira conversa é a hora de orientar: o que acontece agora, o que levar, como acompanhar. Isso pode virar uma mensagem final fixa, revisada pelo núcleo. Avisar a família quando o caso andar depende de integração com o Verde. O atendimento por vídeo à pessoa presa está nas [[Ideias ENAP - Defensoria]].
- **Viabilidade:** média. O texto é simples; o acompanhamento depende do Verde.
- **Esforço:** P para a orientação, M para o acompanhamento.

### 11. Pesquisa de satisfação curta no fim, com apoio da CINCO/Enap
- **Da obra:** [1/9976](https://repositorio.enap.gov.br/handle/1/9976) (2025): na Jornada de Investigação Comportamental de 2024, a CINCO fez o diagnóstico das barreiras e motivações para responder, ou não, à pesquisa de satisfação no fim dos atendimentos da Central de Atendimento da SEGES. [1/9979](https://repositorio.enap.gov.br/handle/1/9979) (2024): na 1ª Jornada, a RJPREV testou com 257 pessoas um formulário eletrônico simplificado com escolha padrão, que levou a escolhas mais adequadas. [1/9975](https://repositorio.enap.gov.br/handle/1/9975) (2025): outro projeto da Jornada testou mensagens para o pagamento em dia do DAS do Simples Nacional.
- **Nossa interpretação:** uma pergunta de satisfação no fim do atendimento, concluído ou transferido, daria o indicador de resultado que a nota da Maria ainda não tem. A 1/9976 ajuda a desenhar a pergunta para que as pessoas respondam. A RJPREV é a previdência complementar dos servidores do estado do Rio, o que sugere que órgão estadual pode entrar na Jornada; daria para inscrever um desafio da Maria, como as ideias 1 e 3. Não conferimos se há chamada aberta nem as regras.
- **Viabilidade:** média. A pergunta é simples; a parceria depende da CINCO.
- **Esforço:** M.

### 12. Atendimento por áudio para quem tem dificuldade com texto
- **Da obra:** [1/9227](https://repositorio.enap.gov.br/handle/1/9227) (2025): entre os problemas que os usuários apontam nos serviços digitais estão a complexidade de navegação, a burocracia digital e os limites de acessibilidade. [1/8053](https://repositorio.enap.gov.br/handle/1/8053) (2024): revisão da literatura sobre fatores tecnológicos e sociais que facilitam ou barram o uso desses serviços por pessoas idosas. [1/3273](https://repositorio.enap.gov.br/handle/1/3273) (2018): poucos aplicativos estaduais usavam recursos do celular como GPS, câmera e avisos por push.
- **Nossa interpretação:** muita gente prefere mandar áudio no WhatsApp. Transcrever o áudio deixaria a Maria atender quem tem dificuldade para escrever. Seria um uso novo de IA: entra no inventário, a voz é dado pessoal e o relato pode ter dado sensível. As obras falam de barreiras em geral, não de áudio; essa ligação é nossa.
- **Viabilidade:** média. Não conferimos se a Tykhe repassa áudio para a Maria.
- **Esforço:** M a G.

### 13. Atendimento em outros idiomas para imigrantes
- **Da obra:** [1/3633](https://repositorio.enap.gov.br/handle/1/3633) (2018): o CRAI, em São Paulo, oferece atendimento direto, multilíngue, especializado e gratuito a imigrantes, refugiados e apátridas, qualquer que seja a nacionalidade ou a situação migratória e documental.
- **Nossa interpretação:** a Maria poderia reconhecer um relato em outro idioma (espanhol, inglês, francês) e responder ao menos a abertura nesse idioma, ou transferir para humano já com essa marca. Antes, falta saber se há demanda de imigrantes na Defensoria.
- **Viabilidade:** média. Não temos dado de demanda.
- **Esforço:** M.

## O que mudou em relação à versão anterior
- A versão anterior foi feita a partir de títulos e trechos. Esta parte dos resumos completos e separa o que a obra diz do que é interpretação nossa.
- [1/9281](https://repositorio.enap.gov.br/handle/1/9281) não diz que emoção é sinal de prioridade. O estudo faz uma avaliação de valores da política de atendimento da Polícia Civil do DF, conclui que as emoções e o trabalho emocional são centrais na qualidade do atendimento e recomenda levar essa dimensão ao planejamento e à formação. Serve para a formação de quem atende, não para a triagem; saiu da lista.
- [1/7929](https://repositorio.enap.gov.br/handle/1/7929) (WhatsApp na administração pública) só cita desafios, como privacidade e responsabilidade pela informação divulgada, diz que o uso não é formalizado e que o trabalho produziu um manual de boas práticas. O resumo não sustenta uma ideia própria.
- [1/7716](https://repositorio.enap.gov.br/handle/1/7716) classifica dispositivos de normas do terceiro setor, não pedidos de cidadãos. Ficou só como referência de método na ideia 5, junto da [1/7397](https://repositorio.enap.gov.br/handle/1/7397).
- Saíram os módulos de curso de ouvidoria (1/3147, 1/3156, 1/3157), os casos de experiência do usuário sem resultado no resumo (1/6758, 1/6357), as metodologias de acessibilidade sem resultado medido (1/8945, 1/9905, 1/9429) e os estudos de regulação e governança de IA (1/7419, 1/8764). O resumo deles não traz achado que se aplique à Maria.

## Método e limites
- Base: metadados públicos de 8.055 obras do repositório da ENAP. Busca por frases em título, assunto, resumo e nota de prêmio; cerca de 240 resumos lidos por inteiro.
- O site da ENAP não abriu deste ambiente, então nenhum texto completo foi lido. Cada número citado foi conferido no resumo.
- Nenhuma obra da base trata da Defensoria do Rio; as mais próximas são da DPU.

## Como buscar mais
Base e script em `enap/v2/` na pasta do projeto:
- `python3 buscar.py '"linguagem simples"'` busca a frase exata. Sem aspas, todas as palavras precisam aparecer.
- `python3 buscar.py '"plano de saúde" negativa' 15` combina frase e palavra e mostra 15 resultados.
- `python3 buscar.py ler 1/5221` mostra o resumo completo e a nota de prêmio da obra.

A base v2 guarda todos os resumos, inclusive traduções, e marca as iniciativas premiadas. A busca antiga (`enap/enap_base.py`) junta as palavras com OU e deixa de fora manuais e modelos, como os guias de linguagem simples.
