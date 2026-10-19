---
tipo: reuniao
data: 2026-10-15
hora: "13:59"
convidados:
  - Diogo Leite Mesquita
  - ICARO LUIZ ALBAR EDUARDO
  - CAMILA MAURA MOREIRA DA SILVA
  - IRAN TEIXEIRA DE OLIVEIRA
  - Frederico Medeiros De Paiva
falaram:
  - IRAN TEIXEIRA DE OLIVEIRA
  - CAMILA MAURA MOREIRA DA SILVA
  - ICARO LUIZ ALBAR EDUARDO
  - Frederico Medeiros De Paiva
  - Diogo Leite Mesquita
projeto: "[[Compartilhamento da MarIA com a Bahia]]"
fonte: https://docs.google.com/document/d/1EtveLAz5I6Q-mqmRdAnlZdoHPUufYX-DwGFbErodUlQ/edit
gravacao: https://drive.google.com/file/d/1v_OHZatpjYT_tXO9m1mrCQvcqzsno5rm/view?usp=drive_web
origem: anotações automáticas do Gemini (Google Meet)
tags:
  - reuniao
  - maria
---

# Compartilhamento MarIA - Melhores práticas (15/10)

> Ata gerada automaticamente pelo Gemini no Google Meet; pode conter erros de nomes e termos. Transcrição completa em [[2026-10-15 - Compartilhamento MarIA - Melhores práticas (transcrição)]].

## Resumo

Reunião analisou compartilhamento do sistema MarIA com a Bahia, avaliando modelos de licenciamento e governança de código e riscos técnicos.

**Compartilhamento do sistema MarIA**
Discussão inicial abordou o compartilhamento da solução MarIA com outras Defensorias Públicas, focando no modelo de cessão e licenciamento de código-fonte.

**Desafios técnicos e governança**
Equipe debateu divergências tecnológicas, segurança de repositórios no GitLab e integração com sistemas locais para evitar sobrecarga operacional.

**Alinhamento e próximos passos**
Definida a necessidade de estimativas de esforço e estruturação de reuniões de apoio técnico para garantir o sucesso inicial do projeto.

## Decisões

### Precisa de mais conversa

  - **Modelo de compartilhamento do sistema MarIA** O compartilhamento do código-fonte da MarIA com outras defensorias foi debatido, mas os critérios de governança, suporte e desenvolvimento colaborativo permanecem sob análise e dependem de estimativas de esforço técnico.

### Alinhada

  - **Migração do fluxo de divórcio para o novo motor** A equipe alinhou que o fluxo de divórcio em diante será integrado diretamente ao novo motor da Maria, mantendo temporariamente o fluxo de alimentos para migração posterior.

## Próximas etapas (sugeridas pelo Gemini)

  - [Gustavo, Braida] Estimar Esforço Implantação: Realizar o levantamento estimado de esforço para a implantação da MarIA na Defensoria da Bahia.
  - [COP] Analisar Esforço: Analisar o esforço necessário para a implantação do sistema MarIA na Defensoria da Bahia.
  - [Frederico Medeiros De Paiva, Diogo Leite Mesquita] Atualizar Contrato: Realizar a contagem estimada de impacto de Pontos de Função e Unidades de Serviço Técnico no aditivo do contrato para 2024.
  - [Diogo Leite Mesquita] Revisar Convênio: Verificar as cláusulas do convênio assinado entre as Defensorias sobre o compartilhamento de ferramentas e código fonte.
  - [ICARO LUIZ ALBAR EDUARDO] Pesquisar governança: Realizar estudo sobre governança de repositórios, controle de acesso e versionamento de código. Compartilhar os resultados das pesquisas com o Iran.
  - [IRAN TEIXEIRA DE OLIVEIRA] Mapear requisitos: Elaborar documentação detalhando os recursos de recursos humanos, tecnologia da informação, inteligência artificial, suporte e fluxos necessários para a implantação do sistema.
  - [CAMILA MAURA MOREIRA DA SILVA] Analisar estratégia: Avaliar os impactos estratégicos e de negócio para a Defensoria Pública resultantes da futura expansão do projeto.
  - [Diogo Leite Mesquita] Reunião técnica: Realizar reunião com Braider e Gustavo para definir cenários de implantação e estimar o esforço técnico necessário da equipe.
  - [CAMILA MAURA MOREIRA DA SILVA] Antecipar reunião: Antecipar a reunião com Braida e Gustavo em 30 minutos para alinhar detalhes antes do encontro sobre crédista.
  - [CAMILA MAURA MOREIRA DA SILVA] Alinhar com Anderson: Apresentar o panorama atual e os impactos projetados do projeto para Anderson na próxima segunda-feira.
  - [Diogo Leite Mesquita] Alinhar com Ricardo: Realizar uma conversa com Ricardo para solicitar que ele forneça feedback à equipe sobre o status dos fluxos.
  - [CAMILA MAURA MOREIRA DA SILVA] Responder e-mail: Enviar resposta oficial ao e-mail encaminhado por Ricardo.
  - [IRAN TEIXEIRA DE OLIVEIRA] Refinar propostas: Atualizar as ideias e refinar as imagens enviadas anteriormente através da ferramenta Geminar.
  - [CAMILA MAURA MOREIRA DA SILVA] Compartilhar transcrição: Disponibilizar a transcrição desta reunião para todos os participantes assim que o arquivo estiver pronto.

## Detalhes

**Compartilhamento do Sistema MarIA com Outras Defensorias**: CAMILA MAURA MOREIRA DA SILVA inicia a discussão sobre a demanda de outras Defensorias Públicas, com destaque para a Defensoria da Bahia, pelo acesso à solução MarIA (especificamente o módulo oliasta). O principal problema levantado é como operacionalizar o compartilhamento do código-fonte e da solução de forma sustentável, garantindo que outras instituições colaborem com novas funcionalidades sem apenas capitalizar politicamente sobre o desenvolvimento da Defensoria do Rio de Janeiro (00:01:46).

**Expectativas de Suporte e Governança Colaborativa**: ICARO LUIZ ALBAR EDUARDO questiona se haverá exigência de suporte técnico para as Defensorias receptoras, ao que CAMILA MAURA MOREIRA DA SILVA responde que eximir-se totalmente da responsabilidade é impossível, sendo necessário estruturar um modelo que fortaleça nacionalmente o sistema de forma colaborativa, exigindo possivelmente uma equipe ou área centralizada de suporte (00:05:17).

**Padrões Tecnológicos e Riscos de Engenharia Reversa**: ICARO LUIZ ALBAR EDUARDO aponta a divergência de pilhas tecnológicas (como TypeScript versus Python) entre as Defensorias, exigindo documentação detalhada ou refatoração interna. Discussões adicionais entre CAMILA MAURA MOREIRA DA SILVA, ICARO LUIZ ALBAR EDUARDO e IRAN TEIXEIRA DE OLIVEIRA abordam os riscos de clonagem de código, engenharia reversa e a necessidade de salvaguardas burocráticas e contratuais (00:07:48).

**Restrições Comerciais e Convênio Interinstitucional**: ICARO LUIZ ALBAR EDUARDO e CAMILA MAURA MOREIRA DA SILVA destacam a necessidade de salvaguardas legais para impedir o uso comercial do código por terceiros ou outras Defensorias. Diogo Leite Mesquita lembra da existência de um convênio pré-assinado entre as Defensorias que regulamenta o compartilhamento de ferramentas e códigos, sugerindo alinhar o processo a esse acordo (00:11:33).

**Modelos de Compartilhamento e Licenciamento**: Frederico Medeiros De Paiva apresenta quatro modelos de compartilhamento (sistema centralizado, cessão e licenciamento de código-fonte, API e cooperação institucional). Frederico Medeiros De Paiva avalia que a cessão e o licenciamento do código-fonte com definição de regras é o modelo mais viável atualmente, evitando a alta complexidade de uma governança cooperativa contínua gerida pela COP (00:15:49).

**Perspectivas Futuras de Consórcios e Órgãos Centralizadores**: IRAN TEIXEIRA DE OLIVEIRA e CAMILA MAURA MOREIRA DA SILVA debatem a possibilidade de criação de um órgão centralizador ou consórcios e organizações não governamentais de direito privado (semelhantes a fundações estaduais) para gerenciar compras e desenvolvimentos centralizados no futuro, quando houver maior maturidade institucional (00:20:44).

**Escopo do Compartilhamento com a Defensoria da Bahia**: CAMILA MAURA MOREIRA DA SILVA esclarece que a Defensoria da Bahia solicitou não apenas a tecnologia (oliasta), mas todo o conhecimento de negócio, incluindo fluxos de atendimento, balcão de atendimento, núcleo de atendimento, PAR e CRC. A autenticação GovBR fica a critério da Defensoria da Bahia adotar ou não em seu cronograma (00:23:45).

**Demanda de Esforço da COP e Envolvimento de Braida**: IRAN TEIXEIRA DE OLIVEIRA e CAMILA MAURA MOREIRA DA SILVA apontam que a personalização de fluxos e o novo motor de conversa implementado por Braida exigirão suporte técnico direto e horas de consultoria da COP, visto que o conhecimento técnico detalhado está centralizado em Braida (00:26:43) (00:28:33).

**Impacto Orçamentário e Saldo de USTs/PFs no Contrato**: Frederico Medeiros De Paiva e Diogo Leite Mesquita discutem o impacto nos saldos de Pontos de Função (PF) e Unidades de Serviço Técnico (UST) do contrato vigente com a COP. Frederico Medeiros De Paiva sugere realizar uma estimativa detalhada de esforço junto a Gustavo e Braida para avaliar a viabilidade de atendimento à Bahia sem comprometer outros projetos (00:30:42).

**Desafios de Integração com o Solar e Sistemas Locais**: Diogo Leite Mesquita, CAMILA MAURA MOREIRA DA SILVA e IRAN TEIXEIRA DE OLIVEIRA debatem as dificuldades técnicas na integração do MarIA com o sistema Solar e com a ferramenta Tike/WhatsApp contratada pela Bahia, ressaltando que o esforço inicial de adaptação recairá pesadamente sobre a equipe técnica do Rio de Janeiro (00:34:12).

**Capacidade Operacional da Equipe da Bahia**: Diogo Leite Mesquita informa que a Defensoria da Bahia conta com uma equipe de doze analistas para dar suporte a legados, implantar o Solar, o novo broker de WhatsApp e o MarIA. CAMILA MAURA MOREIRA DA SILVA alerta para o risco de explosão de demanda e forte pressão política da Defensoria Geral da Bahia sobre a equipe técnica (00:39:54).

**Estratégia de Apoio Inicial e Reuniões de Alinhamento**: Diogo Leite Mesquita sugere estabelecer uma reunião quinzenal de apoio técnico com a Defensoria da Bahia, direcionando-os a realizar as adaptações essenciais de API e peticionamento, visando garantir o sucesso inicial do projeto sem sobrecarregar excessivamente a equipe do Rio de Janeiro (00:44:22).

**Governança de Repositórios de Código**: ICARO LUIZ ALBAR EDUARDO propõe utilizar o GitLab para monitorar puxadas de código, restringir o acesso a contas oficiais de Defensorias através de repositórios privados e aplicar verificações automatizadas de segurança e padrões para novas funcionalidades (00:45:23).

**Levantamento de Requisitos e Macrozona de Impacto**: IRAN TEIXEIRA DE OLIVEIRA propõe a criação de uma documentação detalhada listando os pré-requisitos necessários para a implementação do MarIA (recursos humanos, TI, inteligência artificial, suporte, integrações e fluxos), focando na visão macro antes de detalhar o controle de repositórios (00:46:26).

**Viabilidade Temporal de Contribuições Colaborativas**: IRAN TEIXEIRA DE OLIVEIRA e Diogo Leite Mesquita concordam que eventuais contribuições ou melhorias desenvolvidas pela Bahia demorarão a retornar para o projeto central, devido à prioridade na estabilização da implementação inicial e das adaptações locais (00:48:47).

**Possibilidade de Operação Inicial Manual**: CAMILA MAURA MOREIRA DA SILVA sugere que a Defensoria da Bahia poderá iniciar a operação do MarIA de forma descentralizada ou sem integrações profundas automatizadas em um primeiro momento — tal como operou o NAD no Rio de Janeiro —, realizando cadastros e registros manualmente antes de investir em grandes integrações com o Solar (00:50:59).

**Escopo de Atendimento e Autoatendimento solicitado**: CAMILA MAURA MOREIRA DA SILVA observa que a Defensoria Geral da Bahia solicitou todos os fluxos, incluindo autoatendimento e agendamento, o que inevitavelmente exigirá integrações complexas que precisam ser avaliadas como um produto mínimo viável (00:54:14).

**Próximos Passos e Reuniões de Alinhamento**: Diogo Leite Mesquita e CAMILA MAURA MOREIRA DA SILVA definem os próximos passos para a reunião com Anderson na segunda-feira, incluindo a estimativa de esforço pela COP e Braida, a verificação do convênio interinstitucional e o alinhamento das etapas de entrega do código e suporte (00:56:10).

**Implantação em Ondas e Abordagem Piloto**: CAMILA MAURA MOREIRA DA SILVA expressa preocupação de que outra defensoria pública possa tentar uma implementação em larga escala sem a devida preparação, gerando uma crise de suporte inesperada. Para mitigar esse risco, CAMILA sugere conversar com mais pessoas, além de Ricardo e de seu secretário, para propor uma visão de implantação em ondas e um modelo piloto que permita o controle do sucesso. Diogo Leite Mesquita demonstra concordância com a sugestão de adotar essa precaução. O consenso estabelecido é buscar esse alinhamento ampliado com os responsáveis externos antes de iniciar a adoção completa (01:00:27).

**Gestão de Versões e Incompatibilidade de Código**: Diogo Leite Mesquita levanta dúvidas sobre possíveis incompatibilidades de código caso a outra instituição realize alterações diretamente no código-fonte enquanto a equipe principal desenvolve novas versões, como a Maria 2.3. ICARO LUIZ ALBAR EDUARDO avalia que eles provavelmente não adotarão novas versões de imediato por falta de familiaridade, mas que atualizações e notificações podem ser enviadas pelo repositório (01:01:14). Diogo e IRAN TEIXEIRA DE OLIVEIRA discutem a possibilidade de o desenvolvimento externo ser feito por meio de solicitações de pull request para aprovação (01:02:02). O consenso aponta que notificações no repositório e processos de mesclagem (merge) serão necessários para lidar com essas alterações (01:01:14).

**Governança de Código, Testes Automatizados e Padrões de Qualidade**: O grupo debate o fluxo técnico para garantir a segurança e a limpeza do código integrado de outras defensorias. ICARO LUIZ ALBAR EDUARDO explica que esteiras de teste automatizado podem validar o código, mas ressalta que as entregas devem seguir rigorosamente padrões de mercado, como metodologias SOLID, linting, indentação e camadas de segurança (01:02:59). Diogo Leite Mesquita sugere um fluxo em que uma versão base é enviada, adaptada localmente (removendo componentes específicos como o NAD ou ajustando para instituições como IF Bahia e IF Rio), e depois enviada para aprovação do código unificado (01:03:45). ICARO aponta que manter ramificações (branches) separadas para cada defensoria apresenta complexidades operacionais e discute a governança com CAMILA MAURA MOREIRA DA SILVA (01:04:35). O consenso é que a viabilidade técnica e a governança do repositório Git ou GitLab precisam ser formalmente estruturadas (01:05:26).

**Questões Éticas sobre Premiações e Soluções Derivadas**: ICARO LUIZ ALBAR EDUARDO questiona se outras instituições poderiam concorrer a premiações utilizando o projeto desenvolvido contra a equipe original (01:05:26). CAMILA MAURA MOREIRA DA SILVA argumenta que, eticamente, não seria adequado concorrer aos mesmos prêmios utilizando a mesma solução base, embora engenharia reversa ou repaginação possam tecnicamente ocorrer (01:06:36). Diogo Leite Mesquita sugere uma conversa prévia para alinhar que disputar o mesmo prêmio não é ideal, mas apoia totalmente que concorram em premiações estaduais regionais (como inovação no estado da Bahia) utilizando a base da Maria. CAMILA e Diogo destacam que a tecnologia já é utilizada por cerca de 200 instituições no Brasil e que o motor principal é compartilhado (01:07:38). O consenso é estabelecer um alinhamento ético transparente com as defensorias parceiras, permitindo premiações regionais, mas evitando conflitos diretos em premiações idênticas (01:06:36).

**Preparação de Documentação e Alinhamentos com a Administração**: CAMILA MAURA MOREIRA DA SILVA informa que a reunião está sendo gravada e transcrita para servir de consulta e mapeamento de riscos. A expectativa é estruturar uma conversa na segunda-feira com Anderson para apresentar os riscos, os níveis de esforço considerável da equipe e as decisões necessárias (01:09:50). ICARO LUIZ ALBAR EDUARDO e IRAN TEIXEIRA DE OLIVEIRA definem como tarefa pesquisar e trocar ideias sobre versionamento e tipos de governança de código (01:10:48). O consenso é utilizar o material transcrito e o alinhamento técnico para fundamentar a reunião com a administração na segunda-feira (01:09:50).

**Integrações com Solar, Blip e Cronograma com Parceiros**: Diogo Leite Mesquita e CAMILA MAURA MOREIRA DA SILVA discutem a necessidade de antecipar uma conversa com Braida e Gustavo para avaliar cenários e estimativas de esforço (01:11:50). IRAN TEIXEIRA DE OLIVEIRA aponta que a aplicação se comunica de forma plugável via API com o Solar. Contudo, CAMILA demonstra maior preocupação com a governança da empresa Blip, apontando que o Solar pode demorar devido a filas de desenvolvimento internas, enquanto a outra empresa possui grande ímpeto de execução (01:13:32). O consenso é tentar antecipar a reunião com Braida e Gustavo para o dia seguinte para esclarecer o impacto operacional dessas integrações (01:12:44) (01:17:37).

**Status de Migração de Fluxos no Motor Maria**: CAMILA MAURA MOREIRA DA SILVA relata o andamento das construções feitas por Braida dentro do novo motor da Maria, mencionando que os fluxos de divórcio, crédito cesta e alimentos já foram estruturados, embora alimentos ainda dependa de testes com a Tribunal. ICARO LUIZ ALBAR EDUARDO e CAMILA confirmam que as novas demandas a partir do divórcio iniciam diretamente no motor (01:14:59). CAMILA observa que a parte do chatbot ainda não foi totalmente liberada em homologação por Braida e reforça que as integrações com o Blip exigirão atenção. O consenso é focar nos fluxos atuais sem sobrecarregar a equipe com problemas imprevistos em módulos complexos nesta fase (01:15:48).

**Próximos Passos e Encerramento das Atividades**: CAMILA MAURA MOREIRA DA SILVA ressalta a importância de apoiar a estruturação interna da outra defensoria e gerenciar a migração de código simultaneamente. Para os próximos encaminhamentos, CAMILA tentará realocar a reunião com Braida e Gustavo para o dia seguinte, e Diogo Leite Mesquita acompanhará o envio de respostas aos e-mails de Ricardo (01:17:37). IRAN TEIXEIRA DE OLIVEIRA menciona que utilizará ferramentas de inteligência artificial para estruturar e refinar suas ideias técnicas. O encerramento ocorre com o alinhamento geral das tarefas e compromissos assumidos pela equipe (01:19:21).

## Relacionado
- [[Compartilhamento da MarIA com a Bahia]]
- [[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]]
- [[Maria - atendimento automatizado]]
- [[2026-10-15 - Compartilhamento MarIA - Melhores práticas (transcrição)]]
