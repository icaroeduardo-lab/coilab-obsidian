---
tipo: reuniao
data: 2026-10-16
hora: "16:01"
convidados:
  - Diogo Leite Mesquita
  - ICARO LUIZ ALBAR EDUARDO
  - Frederico Medeiros De Paiva
  - CAMILA MAURA MOREIRA DA SILVA
  - IRAN TEIXEIRA DE OLIVEIRA
projeto: "[[Maria - atendimento automatizado]]"
fonte: https://docs.google.com/document/d/1lP8Wd8ouGzb3yUorPanQdSgM4rkAxHkqUtFfGdG6v3Q/edit
gravacao: https://drive.google.com/file/d/130uNKh5KVLuM6Jpze83D7d7pWJfVBcRX/view?usp=drive_web
origem: anotações automáticas do Gemini (Google Meet)
tags:
  - reuniao
  - maria
---

# Compartilhamento MarIA (16/10)

> Ata gerada automaticamente pelo Gemini no Google Meet; pode conter erros de nomes e termos. Transcrição completa em [[2026-10-16 - Compartilhamento MarIA (transcrição)]].

## Resumo

Reunião abordou expansão com demandas técnicas e viabilidade contratual.

**Interesse e Demanda Técnica**
Defesa da Bahia solicitou adoção do sistema exigindo transferência tecnológica e suporte.

**Viabilidade e Custos Contratuais**
Equipe avaliou limites de pontos de função e custos de implantação.

**Modelo de Governança e Ações**
Filipe listará melhorias e Gustavo calculará os esforços correspondentes.

## Decisões

### Precisa de mais conversa

  - **Estimativa de USTs e ordem de serviço** A definição do volume de USTs a ser consumido e a respectiva abertura de ordem de serviço para a implantação na Bahia foram debatidas, mas deixadas em aberto devido à falta de visibilidade inicial do ambiente.
  - **Modelo técnico de compartilhamento de software** A escolha entre o modelo arquitetônico centralizado, segregado ou híbrido para o compartilhamento de código e governança com a Bahia foi discutida, sem consenso definitivo estabelecido.

### Alinhada

  - **Cessão do código fonte do MarIA** Ficou estabelecido entre os participantes que a Defensoria do Rio de Janeiro cederá o código do sistema MarIA para a atuação da Defensoria da Bahia.
  - **Elaboração de lista e estimativa** Filipe Braida elaborará a lista de tarefas para a generalização do sistema Maria, e Gustavo Pinto usará essa lista para estimar os pontos de função (PF) e unidades de serviço técnico (UST).
  - **Aguardar contato da Bahia** A equipe aguardará o contato da Bahia após o estudo da documentação enviada para realizar a próxima reunião de alinhamento.

## Próximas etapas (sugeridas pelo Gemini)

  - [O grupo] Alinhar com Bahia: Estabelecer contato com a equipe da Defensoria da Bahia para definir o papel da Defensoria do Rio, requisitos de negócio e modelo de compartilhamento. Identificar se é possível manter uma versão única do sistema ou se serão necessárias adaptações específicas.
  - [COP] Estimar esforço inicial: Realizar um levantamento macro da estimativa de pontos de função e unidades de serviço técnico necessárias para a implantação na Bahia. Subsidiar a tomada de decisão da Defensoria quanto ao consumo de recursos contratuais.
  - [CAMILA MAURA MOREIRA DA SILVA] Reportar status: Apresentar o cenário de implantação e os impactos previstos para a Dra. Anderson na segunda-feira.
  - [Filipe Braida do Carmo] Listar melhorias técnicas: Mapear as tarefas necessárias para generalizar o sistema, incluindo alterações como a flexibilização de logos e nomes.
  - [Gustavo Pinto] Estimar implantação Bahia: Criar estimativas de esforço e tickets para a implementação do projeto com base na lista de melhorias definida.
  - [Filipe Braida do Carmo] Ajustar requisito GovBR: Alterar o código para permitir que o fluxo funcione sem o GovBR configurado como um requisito obrigatório.
  - [O grupo] Reunir equipe Bahia: Realizar uma conversa técnica com a equipe da Bahia para validar limitações e entender o cenário técnico deles.
  - [Filipe Braida do Carmo] Planejar tickets: Elaborar planejamento de tickets para definir escopo de trabalho.
  - [Gustavo Pinto] Estimar esforço: Estimar o esforço necessário de PF e realizar estimativa de unidades de serviço técnico com base na lista de tickets preparada.

## Detalhes

**Contexto e Interesse da Defensoria da Bahia no Sistema Maria**: CAMILA MAURA MOREIRA DA SILVA explicou que a Defensoria da Bahia demonstrou forte interesse em adotar o sistema Maria, solicitando acesso não apenas à solução tecnológica, mas também ao código-fonte, à lógica negocial e à inteligência de inovação por trás da ferramenta. O assunto escalou para o nível das lideranças máximas, envolvendo a Defensora Pública Geral e Dr. Paulo, e o consenso inicial é de apoio institucional à expansão (00:02:00) (00:05:40).

**Demandas de Esforço Técnico e Administrativo**: CAMILA MAURA MOREIRA DA SILVA apontou que a transferência tecnológica exigirá esforço administrativo e técnico considerável, gerando prováveis reuniões, esclarecimentos e adaptações do sistema que envolverão diretamente Filipe Braida do Carmo (00:04:27). Frederico Medeiros De Paiva e IRAN TEIXEIRA DE OLIVEIRA expressaram preocupação prévia sobre como esse suporte poderá sobrecarregar a equipe técnica e impactar a esteira de desenvolvimento interna (00:05:40).

**Viabilidade Financeira e Alinhamento com a Diretoria**: Gustavo Pinto questionou se a Defensoria do Rio de Janeiro planeja aportar recursos financeiros para bancar o esforço de implantação na Bahia, destacando o impacto nos projetos prioritários (00:07:53). CAMILA MAURA MOREIRA DA SILVA respondeu parcialmente, indicando que Dr. Paulo vê o sucesso da implantação na Bahia como benéfico para a instituição, mas reconheceu que o impacto na equipe precisa ser avaliado antes de ser apresentado a Dra. Anderson (00:10:33) (00:12:20).

**Restrições Contratuais e Consumo de USTs**: Frederico Medeiros De Paiva destacou que o contrato atual possui limites de 5.700 pontos de função e 16.200 USTs, com uma linha base de consumo mensal de 1.350 USTs, da qual projetos como o Verde consomem entre 500 e 600 USTs (00:15:25) (00:20:20). Frederico Medeiros De Paiva sugeriu estimar um consumo inicial, como 200 USTs mensais para a implantação na Bahia, para que a Defensoria possa decidir a alocação de recursos diante das restrições contratuais (00:16:35) (00:20:20). Gustavo Pinto ponderou que é difícil fazer uma estimativa exata no momento devido ao desconhecimento do ambiente da Bahia (00:17:48).

**Modelos de Compartilhamento de Software e Papéis**: Filipe Braida do Carmo questionou qual será o papel efetivo da equipe do Rio no processo, se focado em transferência de conhecimento ou em apoio conjunto (00:22:41). Frederico Medeiros De Paiva apresentou modelos de compartilhamento, como cessão ou cooperação técnica com governança centralizada, embora a Defensoria da Bahia careça de uma estrutura dedicada equivalente (00:23:39). Diogo Leite Mesquita propôs dividir o problema entre aspectos burocráticos e técnicos, sugerindo uma abordagem em ondas (como um primeiro mês com 5 encontros e limite de USTs) para mitigar impactos (00:26:10).

**Arquitetura e Modelos de Governança de Código**: Diogo Leite Mesquita, Filipe Braida do Carmo, Gustavo Pinto e ICARO LUIZ ALBAR EDUARDO discutiram os modelos técnicos de compartilhamento, avaliando entre um modelo centralizado (onde a equipe do Rio gerencia o núcleo e homologa versões) e um modelo segregado (com instâncias separadas) (00:28:07) (00:32:28). Filipe Braida do Carmo propôs uma abordagem híbrida inspirada em comunidades de código, permitindo que a equipe da Bahia faça \*fork\* e alterações sob restrições, mas exigindo validação e governança central da Defensoria do Rio para atualizações (00:37:29).

**Flexibilidade de Regras de Negócio, Fluxos e Petições**: Filipe Braida do Carmo esclareceu que o Maria possui arquitetura flexível baseada em banco de dados e um novo motor de conversa programável, permitindo criar fluxos específicos (como um fluxo para a Bahia) sem interferir diretamente no núcleo do sistema do Rio (00:45:36) (00:47:25). Diogo Leite Mesquita e Gustavo Pinto concordaram que a equipe da Bahia deve tentar adotar o Maria padrão quanto possível, mas ajustes pontuais em sumários, campos e petições podem ser acomodados no nível de banco de dados (00:41:23) (00:45:36).

**Integração com Inteligência Artificial e Chaves de API**: CAMILA MAURA MOREIRA DA SILVA e Filipe Braida do Carmo discutiram o uso de inteligência artificial baseada em GPT, apontando que a Defensoria da Bahia precisará utilizar chaves de API próprias inseridas diretamente no banco de dados (00:52:54). Filipe Braida do Carmo informou que as chaves atuais vencerão em janeiro e precisarão ser desativadas/atualizadas, havendo flexibilidade para testes com outros modelos, embora o GPT seja o recomendado inicialmente (00:53:49).

**Requisitos de Infraestrutura e Implantação**: IRAN TEIXEIRA DE OLIVEIRA questionou sobre a obrigatoriedade da AWS para a arquitetura do Maria. Filipe Braida do Carmo, CAMILA MAURA MOREIRA DA SILVA e ICARO LUIZ ALBAR EDUARDO esclareceram que o sistema pode rodar em infraestrutura local ou em qualquer provedor, utilizando Node.js orquestrado por PM2, Nginx na entrada, Redis para cache do \*broker\*, banco de dados PostgreSQL e armazenamento em S3, R2 ou disco, viabilizando uma instalação simples por meio de construção Docker (00:56:18).

**Armazenamento e Ambientes de Homologação**: Filipe Braida do Carmo aborda o uso de serviços de armazenamento como Amazon S3, MinIO ou Cloudflare R2, explicando que o sistema Maria utiliza o S3 principalmente pela eficiência de custos, sem necessidade de grande porte de máquina (00:58:56). ICARO LUIZ ALBAR EDUARDO participa da discussão sobre arquivos assistidos, enquanto Camila Maura Moreira da Silva questiona a estruturação para ambientes de homologação, produção e desenvolvimento. Filipe Braida do Carmo responde que a definição do local de hospedagem ficará a cargo da equipe externa por meio de variáveis de ambiente, desde que respeitem o fluxo estabelecido (00:59:42).

**Adaptações de Código e Cenário Técnico**: Filipe Braida do Carmo aponta a necessidade de generalizar elementos no código para uso da Defensoria Pública da Bahia, como ajustes em logotipos e nomenclaturas. Camila Maura Moreira da Silva sugere realizar uma conversa técnica com a equipe da Bahia para mapear débitos técnicos e entender o impacto no esforço da Defensoria do Rio de Janeiro. IRAN TEIXEIRA DE OLIVEIRA argumenta que as adaptações mais pesadas envolvem a criação de adaptadores para trocar ferramentas como ta por blip e verde por solar, além de lidar com a remoção temporária do acesso GovBR (01:00:42). Filipe Braida do Carmo propõe atualizar o sistema para verificar automaticamente se o GovBR está configurado antes de solicitar a foto, e comenta sobre a complexidade dos modelos programáveis de petição (01:01:56).

**Flexibilização de Módulos e Integração com o Solar**: Camila Maura Moreira da Silva e Filipe Braida do Carmo discutem que a complexa integração com o sistema Solar não será priorizada inicialmente pela Bahia. Filipe Braida do Carmo sugere flexibilizar o sistema para ocultar partes relacionadas ao GovBR ou à distribuição do Solar caso não estejam habilitadas, facilitando a implantação em outras defensorias (01:03:48). Sobre os brokers de WhatsApp, Filipe Braida do Carmo relata conversas com contatos externos e explica que a implementação de chamadas para a API do broker exige proteções contra perda de mensagens, mas documentações padronizadas resolverão a integração (01:05:42).

**Impacto Contratual e Levantamento de Tarefas**: IRAN TEIXEIRA DE OLIVEIRA questiona se o volume de pequenas personalizações poderá encarecer o contrato, preocupação compartilhada por Diogo Leite Mesquita e Camila Maura Moreira da Silva em relação ao controle de custos (01:07:39). Filipe Braida do Carmo compromete-se a listar as tarefas e pontos de melhoria necessários, como a remoção de IDs fixos de NAD e Pormai (01:08:29). Camila Maura Moreira da Silva solicita que Talita Vieira Ribeiro e Gustavo Pinto auxiliem Filipe Braida do Carmo a transformar o levantamento em estimativas de Pontos de Função (PF) e Service Tickets (ST) (01:09:34).

**Estimativas de Esforço Burocrático e Treinamento**: Gustavo Pinto e Diogo Leite Mesquita discutem a precificação de itens burocráticos, incluindo reuniões, criação de documentação técnica, sessões de treinamento e repasse de tecnologia (01:10:37). Frederico Medeiros De Paiva sugere associar alterações a histórias de usuário (UST) por ticket (01:11:35). Diogo Leite Mesquita propõe um pacote inicial de implantação contendo cinco reuniões, dois treinamentos, eixos de requisitos e alterações pontuais de código, com Gustavo Pinto confirmando a viabilidade de estimar os custos a partir dos tickets criados por Filipe Braida do Carmo (01:13:16).

**Planejamento de Sprints e Prioridades de Execução**: Filipe Braida do Carmo propõe gerenciar as melhorias gerais por meio de uma lista de prioridades incorporada gradualmente durante o expediente, evitando a execução de duas sprints simultâneas para o projeto da Bahia e novas funcionalidades (01:14:22). Diogo Leite Mesquita pondera sobre a gestão paralela do projeto de implantação e novas demandas (01:15:12). Ao final, o grupo consolida o direcionamento de que Filipe Braida do Carmo elaborará os tickets de melhoria e Gustavo Pinto calculará os esforços correspondentes (01:17:08).

**Cronograma e Ambiente de Homologação via Telegram**: Camila Maura Moreira da Silva informa que a documentação técnica foi enviada a Ricardo da Bahia há dois dias, prevendo que discussões mais aprofundadas sobre NAD, Pormai e CRC ocorrerão no próximo período devido a recessos (01:18:22). Diogo Leite Mesquita sugere disponibilizar um ambiente de homologação para reduzir a ansiedade da equipe externa (01:19:19). Filipe Braida do Carmo aponta dificuldades com o WhatsApp em homologação e propõe utilizar um bot de Telegram disponível na Tike conectado a um novo servidor apontado para o ambiente verde de homologação (01:20:23). O grupo decide aguardar o retorno da equipe da Bahia após a avaliação técnica (01:23:12).

**Encerramento e Compartilhamento de Documentos**: Diogo Leite Mesquita reforça a importância de manter reuniões de alinhamento caso surjam demandas irredutíveis da parte externa (01:25:23). Camila Maura Moreira da Silva confirma o recebimento do fluxo aprovado pela Dr. Suan e o envio da listagem de documentos de pré-atendimento para Filipe Braida do Carmo, Talita Vieira Ribeiro, Gustavo Pinto e ICARO LUIZ ALBAR EDUARDO (01:26:23). Filipe Braida do Carmo relata que o sistema já está gerando a petição com sucesso, encerrando a reunião com cumprimentos de fim de semana entre todas as pessoas participantes (01:27:18).

## Relacionado
- [[Maria - atendimento automatizado]]
- [[2026-10-16 - Compartilhamento MarIA (transcrição)]]
