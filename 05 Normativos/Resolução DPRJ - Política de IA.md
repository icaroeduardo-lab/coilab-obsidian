---
tipo: normativo
orgao: DPRJ
assunto: Política de Governança, Gestão e Uso de Inteligência Artificial
numero: 
data_publicacao: 
processo: E-20/001.006034/2025
status: vigente
tags:
  - normativo
  - ia
  - governança
---

# Resolução DPRJ - Política de Governança, Gestão e Uso de IA

> Número e data de publicação ainda não preenchidos. Texto integral abaixo do resumo.

## Resumo
- **O que institui:** a Política de Governança, Gestão e Uso de IA da Defensoria Pública do RJ (art. 1º). Vale para todos que desenvolvem, contratam, usam ou interagem com IA na DPRJ, incluindo terceirizados e fornecedores.
- **IA institucional x comercial (art. 2º):** a institucional é homologada e isolada, sem uso dos dados para treinar modelos comerciais; a comercial é qualquer plataforma pública de terceiros.
- **Princípios (art. 3º):** centralidade da pessoa humana, transparência e explicabilidade, não discriminação, responsabilidade, privacidade (LGPD), segurança da informação, finalidade pública.
- **Classificação de risco (arts. 5º a 7º):**

| Nível | Risco | Exigência |
|---|---|---|
| I | Baixo | Documentação simplificada e aviso de uso de IA |
| II | Médio | Documentação completa, validação de segurança e supervisão humana documentada |
| III | Alto | Avaliação de Impacto Algorítmico prévia, testes de viés, homologação no CGTI e auditoria periódica |
| IV | Excessivo | **Proibido** |

- **Quem classifica o risco:** a unidade requisitante junto com a **Coordenação do Laboratório de Inovação e IA (COILAB)**, no início do projeto, com reavaliação periódica (art. 5º, § 1º).
- **Deveres dos usuários (arts. 8º e 9º):** validação humana obrigatória de tudo que a IA gerar; **proibido inserir dados pessoais, sigilosos ou de assistidos em IA comercial**; dados protegidos só na IA institucional; a responsabilidade é sempre do signatário, sem desculpa de "alucinação".
- **Incidentes (art. 10):** reportar imediatamente ao Encarregado de Proteção de Dados (EPD), seguindo o Plano de Resposta a Incidentes do CGSI.
- **Governança (arts. 11 a 13):** o **CGTI** governa e homologa; o **CGSI** analisa segurança dos sistemas de risco médio e alto; a **DGD, por meio do COILAB**, dá suporte técnico de conformidade antes da implantação e mantém o **inventário centralizado de IA**; o EPD é consultado quando houver dados pessoais.
- **Soberania tecnológica (arts. 14 e 15):** IA como camada intercambiável; prompts e bases de ajuste fino são patrimônio da DPRJ; preferência por modelos open-source; nenhum fluxo pode ter lógica conhecida só pelo algoritmo.
- **Letramento em IA (art. 16):** capacitação continuada; treinamento obrigatório para novos agentes em até **60 dias** após a admissão.
- **Direito à contestação (art. 17):** canal no site para pedir revisão humana de decisões apoiadas em IA.
- **Contratos (art. 18):** cláusulas de LGPD, auditoria, documentação dos algoritmos e **portabilidade** de dados, logs e parametrizações em formatos abertos.

## O que cabe ao COILAB
- [ ] Classificar o risco de cada sistema de IA com a unidade requisitante (art. 5º, § 1º)
- [ ] Dar suporte técnico de conformidade, acurácia e robustez antes da implantação (art. 12, I)
- [ ] Manter o inventário centralizado de aplicações de IA (art. 12, II)
- [ ] Apoiar a trilha de letramento em IA para novos agentes, em até 60 dias da admissão (art. 16)

## Relacionado
- [[Resolução DPRJ - Laboratório para Inovação e IA (2025)]]
- [[Gestão da Inovação (WeGov)]]
- [[IA no Setor Público]]
- [[Marco Legal de CT&I]]

---

## Texto integral

O DEFENSOR PÚBLICO GERAL DO ESTADO DO RIO DE JANEIRO, no exercício de suas atribuições legais, nos termos do art. 8º, IV da Lei Complementar Estadual nº 06/77, e do art. 100 da Lei Complementar nº 80/94,

CONSIDERANDO a importância estratégica da Inteligência Artificial (IA) para o aprimoramento dos serviços prestados pela Defensoria Pública do Estado do Rio de Janeiro, garantindo maior eficiência, celeridade e alcance na prestação da assistência jurídica integral e gratuita aos cidadãos;

CONSIDERANDO a necessidade de assegurar o uso eficiente, eficaz, ético, seguro, transparente e responsável das soluções e serviços de Inteligência Artificial, em consonância com as garantias fundamentais, os princípios da Administração Pública, as diretrizes da Lei Geral de Proteção de Dados Pessoais (LGPD - Lei nº 13.709/2018) e as melhores práticas de governança de Tecnologia da Informação;

CONSIDERANDO as diretrizes e competências do Comitê Gestor de Segurança da Informação (CGSI), instituído pela Resolução DPRJ nº 1363, de 14 de agosto de 2025, ao qual compete a governança da segurança da informação, a gestão de riscos e a proteção dos ativos informacionais da Instituição;

CONSIDERANDO o papel indispensável da governança de Inteligência Artificial na mitigação de riscos de viés algorítmico, na proteção de dados institucionais e pessoais, bem como na prevenção de incidentes de segurança cibernética;

CONSIDERANDO as diretrizes consolidadas no âmbito nacional para o uso de tecnologias emergentes no Sistema de Justiça e a conveniência de centralizar a governança tecnológica no Comitê de Governança de Tecnologia da Informação (CGTI), sem prejuízo das competências de segurança da informação atribuídas ao CGSI;

CONSIDERANDO o que consta do processo administrativo n° E-20/001.006034/2025.

RESOLVE:

### TÍTULO I - DAS DISPOSIÇÕES PRELIMINARES E DEFINIÇÕES

**Art. 1º** Fica instituída a Política de Governança, Gestão e Uso de Inteligência Artificial no âmbito da Defensoria Pública do Estado do Rio de Janeiro (DPRJ).

Parágrafo único. As disposições desta Resolução aplicam-se a todos os órgãos, unidades administrativas, Defensores(as) Públicos(as), Servidores(as), Residentes, Estagiários(as), prestadores de serviço e fornecedores externos que desenvolvam, contratem, utilizem ou interajam com sistemas de Inteligência Artificial sob a égide da DPRJ.

**Art. 2º** Para os efeitos desta Resolução, adotam-se as seguintes definições:

I - Sistema de Inteligência Artificial (IA): sistema baseado em máquina que processa dados e informações recebidos para gerar previsões, recomendações, conteúdos ou decisões que possam influenciar ambientes virtuais ou reais, operando com diferentes níveis de autonomia;

II - Inteligência Artificial Generativa (IA Generativa): classe de sistemas de IA projetada e treinada com vastos volumes de dados para gerar novos conteúdos originais, tais como textos estruturados, imagens, áudio, vídeo ou código de software;

III - IA Institucional/Interna (Ambiente Homologado): plataforma de Inteligência Artificial cujos dados de entrada (prompts), processamento e saídas são mantidos de forma isolada, em infraestrutura sob controle direto ou contratual restrito da DPRJ, sendo vedado o uso das interações internas para o treinamento público de modelos comerciais;

IV - IA Comercial/Pública (Plataforma Externa): plataformas genéricas de IA acessíveis via web para o público geral, de propriedade de terceiros, não desenvolvidas, homologadas ou contratadas pela DPRJ, onde não há garantias estritas de isolamento e cujos termos de uso permitem a utilização dos dados inseridos para treinamento de modelos globais;

V - Ciclo de Vida da IA: sequência de fases que compreende a concepção, o planejamento, a modelagem, o desenvolvimento, o treinamento, a testagem, a validação, a implantação, a operação, o monitoramento e a eventual descontinuação do sistema de IA;

VI - Curadoria de Dados: processo de organizar, selecionar, limpar, catalogar e proteger o conjunto de dados destinado ao treinamento, teste e validação de modelos de IA, visando garantir que as bases sejam seguras, íntegras, representativas e livres de vieses discriminatórios, e estejam de acordo com as políticas de TI, de Segurança da Informação, Privacidade e Proteção de Dados da DPRJ;

VII - Avaliação de Impacto Algorítmico (AIA): análise sistemática e documentada dos potenciais impactos gerados por um sistema de IA sobre os direitos fundamentais, privacidade dos dados e processos de tomada de decisão, identificando medidas mitigadoras de riscos;

VIII - Viés Algorítmico: erro sistemático e injusto no modelo de decisão da IA que gera resultados desproporcionalmente desfavoráveis ou discriminatórios a determinados grupos ou indivíduos, decorrente de dados de treinamento desbalanceados ou falhas de modelagem;

IX - Explicabilidade: capacidade técnica de descrever ou traduzir, em linguagem acessível e compreensível ao ser humano, a lógica interna, os critérios e o funcionamento do algoritmo que fundamentou determinada sugestão, classificação ou recomendação gerada pela IA;

X - Supervisão Humana: mecanismo de controle contínuo que assegura a intervenção ativa de profissionais capacitados em todas as fases relevantes do funcionamento da IA, garantindo que o sistema não tome decisões finais e autônomas sem a possibilidade de revisão ou cancelamento por um agente humano;

XI - Anonimização: utilizar meios técnicos razoáveis e disponíveis no momento do tratamento, por meio dos quais um dado perde a possibilidade de associação, direta ou indireta, a um indivíduo;

XII - Agentes internos: todos aqueles que integram a DPRJ, seja a título efetivo ou precário, estatutário ou contratual, como defensores, servidores do quadro, extraquadros e cedidos, residentes, estagiários e terceirizados.

### TÍTULO II - DOS FUNDAMENTOS, PRINCÍPIOS E DIRETRIZES GERAIS

**Art. 3º** O desenvolvimento, a governança, a gestão e o uso de sistemas de IA na DPRJ observarão os seguintes princípios fundamentais:

I - Centralidade da Pessoa Humana: a IA deve atuar como ferramenta de apoio e ampliação das capacidades humanas, preservando a dignidade, a autonomia e a garantia dos direitos fundamentais;

II - Transparência e Explicabilidade: garantia de que os critérios utilizados pelos sistemas de IA sejam compreensíveis e passíveis de escrutínio pelos assistidos e autoridades, vedada a adoção de critérios puramente opacos para decisões que afetem direitos fundamentais;

III - Não Discriminação e Equidade: dever de identificar e mitigar ativamente vieses algorítmicos que possam reforçar preconceitos estruturais ou desigualdades sociais;

IV - Responsabilidade e Prestação de Contas: responsabilização continuada dos agentes públicos pelas decisões sugeridas ou fundamentadas com o apoio da tecnologia;

V - Privacidade e Proteção de Dados: garantia de conformidade com a Lei Federal nº 13.709/2018, aplicando-se os princípios de minimização dos dados, limitação das finalidades, privacidade por padrão e segurança desde a concepção do sistema;

VI - Segurança da Informação e Segurança Cibernética: adoção de controles técnicos robustos, incluindo criptografia e isolamento de ambientes, em conformidade com as diretrizes da Política de Segurança da Informação (PSI) e com as deliberações do Comitê Gestor de Segurança da Informação (CGSI) da DPRJ;

VII - Finalidade Pública e Interesse Social: direcionamento prioritário da tecnologia para otimizar o acesso à justiça e a eficiência dos serviços da DPRJ.

**Art. 4º** Constituem objetivos específicos da Política:

I - Otimizar a rotina de trabalho dos agentes internos através da automação de tarefas repetitivas de análise e elaboração de documentos, desde que sob estrita revisão humana, e facilitar o acesso dos assistidos aos serviços prestados pela DPRJ;

II - Garantir que as soluções tecnológicas contratadas pela instituição possuam código auditável ou conformidade explícita com os padrões éticos e de segurança cibernética exigidos nesta Resolução;

III - Estabelecer regras claras sobre as responsabilidades de desenvolvimento e fiscalização das instâncias administrativas de tecnologia da DPRJ.

### TÍTULO III - DA CLASSIFICAÇÃO DE RISCO E AVALIAÇÃO DE IMPACTO ALGORÍTMICO

**Art. 5º** Todo sistema de IA utilizado ou desenvolvido na DPRJ deverá ser classificado de acordo com o grau de risco associado à sua operação, observando-se os seguintes níveis:

I - Nível I - Risco Baixo: sistemas de apoio administrativo secundário que não oferecem impacto significativo ou direto ao mérito de direitos fundamentais de assistidos ou agentes internos;

II - Nível II - Risco Médio: sistemas que influenciam fluxos de trabalho e processos jurídicos, administrativos ou gerenciais, mas que não possuem caráter decisório autônomo final;

III - Nível III - Risco Alto: sistemas que auxiliam de forma determinante na elaboração de decisões automatizadas, ou que interfiram diretamente na esfera de direitos e garantias fundamentais dos assistidos;

IV - Nível IV - Risco Excessivo (PROIBIDO): sistemas com potencial de causar danos sociais irreversíveis, que operem de forma totalmente autônoma sem supervisão humana viável, ou que gerem discriminação sistêmica, preconceitos e graves ameaças à dignidade humana, à privacidade de dados ou a qualquer outro direito fundamental.

§ 1º. A classificação de risco será realizada conjuntamente pela unidade requisitante e pela Coordenação do Laboratório de Inovação e Inteligência Artificial no início do ciclo de vida do projeto, devendo ser periodicamente reavaliada após a implantação do sistema de IA.

§ 2º A reavaliação ocorrerá sempre que houver mudanças na classificação de riscos ou quando houver alteração na avaliação de impacto algorítmico.

**Art. 6º** Conforme a classificação de risco homologada, os requisitos de conformidade documental, técnica e de auditoria observarão a seguinte gradação de exigências operacionais:

I - Para sistemas de Risco Baixo: exigência exclusiva de documentação técnica simplificada e aviso visual ao usuário de que a atividade conta com auxílio de IA;

II - Para sistemas de Risco Médio: exigência de documentação técnica completa, validação de segurança interna quanto à integridade dos dados e garantia documentada de controle e supervisão humana;

III - Para sistemas de Risco Alto: exigência de confecção prévia de Avaliação de Impacto Algorítmico, testes formais de mitigação de vieses, homologação prévia no CGTI e auditoria técnica interna periódica de segurança;

IV - Para sistemas de Risco Excessivo: checagem anterior do risco excessivo para subsidiar a decisão de não adoção do sistema de IA pela DPRJ.

Parágrafo único. Os aspectos de segurança da informação e proteção de dados das auditorias de sistemas de IA de Risco Alto deverão observar as diretrizes, a periodicidade e o escopo definidos pelo Comitê Gestor de Segurança da Informação (CGSI), nos termos do Art. 4º, IX da Resolução DPRJ nº 1363/2025.

**Art. 7º** Fica proibido o desenvolvimento, contratação, implementação e utilização de sistemas de IA classificados no nível de Risco Excessivo (Nível IV), compreendendo:

I - Sistemas que tomem decisões jurídicas e/ou administrativas autônomas com impacto em direitos fundamentais sem possibilidade de revisão humana ou veto imediato;

II - Soluções cujo funcionamento interno seja tecnicamente inauditável ou que impeça a explicabilidade;

III - Ferramentas concebidas para induzir comportamentos nocivos à dignidade humana, discriminar grupos protegidos por lei, violar a privacidade de dados de forma massiva ou infringir direitos autorais e de propriedade intelectual.

### TÍTULO IV - DOS DEVERES E RESPONSABILIDADES DOS AGENTES INTERNOS E GESTÃO DE INCIDENTES

**Art. 8º** Os usuários internos da DPRJ que utilizarem ferramentas de IA Generativa ou sistemas inteligentes de apoio devem atuar com diligência, ética e profissionalismo, observando os seguintes deveres de segurança e conduta:

I - Validação Humana Obrigatória: o agente interno deve conferir e verificar de forma rigorosa a exatidão lógica, jurídica, factual e gramatical de qualquer conteúdo gerado por IA antes de sua utilização formal, assinatura ou juntada processual;

II - Vedação de Inserção de Dados Sensíveis em IA Comercial: é expressamente proibida a inserção de dados pessoais (sensíveis ou não), dados sob segredo de justiça, dados de identificação de assistidos, dados protegidos por sigilo legal ou segredos institucionais em sistemas de IA de uso comercial externo ou público não homologados pela DPRJ, ou sem a devida anonimização irreversível;

III - Uso de IA Institucional: para o processamento de textos, petições ou relatórios que envolvam dados institucionais protegidos, os agentes internos deverão utilizar unicamente o ecossistema de IA Institucional homologado e mantido pela DPRJ, cujos canais garantem o isolamento cibernético e a impossibilidade de vazamento de dados corporativos para treinamento externo de algoritmos.

**Art. 9º** A utilização de sistemas de IA para auxiliar a elaboração de pareceres, relatórios, peças processuais ou manifestações não afasta nem atenua a responsabilidade do subscritor do documento.

§ 1º A autoria e a responsabilidade técnica e jurídica pelo conteúdo das manifestações permanecem integralmente atribuídas ao agente interno signatário, devendo este garantir que as conclusões ou dados sugeridos pela ferramenta correspondam à melhor técnica jurídica e à veracidade factual.

§ 2º É vedada a limitação de responsabilidade do agente interno sob pretexto de falha tecnológica, erro do modelo ou "alucinação" do sistema de IA.

**Art. 10.** Qualquer incidente de segurança da informação envolvendo sistemas ou aplicações de Inteligência Artificial, incluindo vazamento de dados de prompts, mau funcionamento crítico com vazamento de dados de assistidos, ou exploração de vulnerabilidades cibernéticas das ferramentas deve ser reportado imediatamente à(ao) Encarregada(o) de Proteção de Dados (EPD).

Parágrafo único. O tratamento, a contenção e a resposta a tais episódios observarão os ritos e prazos estabelecidos no Plano de Resposta a Incidentes (PRI) institucional gerenciado pelo CGSI, conforme a Resolução DPGERJ nº 1142/2022 e a Resolução DPGERJ nº 1363/2025.

### TÍTULO V - DA GOVERNANÇA, GESTÃO E CAPACITAÇÃO

#### Seção I - Das Instâncias de Gestão e Governança de TI

**Art. 11.** A governança estratégica do uso de Inteligência Artificial compete de forma exclusiva ao Comitê de Governança de TI (CGTI) da DPRJ, criado pela Resolução nº 1264/2024, ao qual incumbe:

I - Avaliar e homologar as avaliações de risco e de impacto algorítmico encaminhadas pelas unidades técnicas;

II - Analisar os casos de descumprimento desta Resolução e autorizar a homologação de sistemas de IA na instituição.

Parágrafo único. O CGTI atuará em cooperação mútua com o Comitê Gestor de Segurança da Informação (CGSI), devendo submeter à análise deste os sistemas de IA de risco médio ou alto que impactem de forma relevante a segurança dos ativos de informação e bancos de dados da Defensoria Pública.

**Art. 12.** Compete à Diretoria de Governança Digital e Inovação (DGD), por meio da Coordenação do Laboratório de Inovação e Inteligência Artificial (COILAB):

I - Prestar suporte técnico prévio de conformidade, acurácia e robustez dos sistemas de IA antes da sua implantação;

II - Manter atualizado o inventário centralizado das aplicações de IA em funcionamento na instituição.

**Art. 13.** A(o) Encarregada(o) de Proteção de Dados (EPD) deverá ser formalmente consultada(o) nas fases de planejamento, validação interna e descontinuação de sistemas de IA que envolvam o processamento de dados pessoais, zelando pela conformidade com a LGPD e pela realização de revisões de privacidade desde a concepção.

#### Seção II - Da Independência Tecnológica e Proteção do Legado de Conhecimento

**Art. 14.** Fica estabelecido o princípio da soberania e proteção do legado de conhecimento da Defensoria Pública, com o objetivo de mitigar a dependência tecnológica em face de fornecedores externos, atualizações de modelos ou descontinuação de ferramentas de Inteligência Artificial (IA).

**Art. 15.** Os processos de trabalho, fluxos de triagem e bases de conhecimento da Defensoria Pública devem ser mantidos de forma agnóstica e independente de qualquer tecnologia de IA específica, observadas as seguintes diretrizes:

I - Desacoplamento Arquitetural: Todo sistema de IA implementado deve funcionar como uma camada modular e intercambiável. As regras de negócio e a inteligência jurídica do órgão devem residir preferencialmente em sistemas próprios ou em bancos de conhecimento controlados pela Defensoria, permitindo a substituição do fornecedor ou do modelo de IA a qualquer tempo, sem perda do histórico ou interrupção do serviço.

II - Soberania dos Dados de Treinamento e Engenharia de Prompt: As bases de dados utilizadas para o ajuste fino e o histórico de comandos estruturados pela equipe da Defensoria são considerados patrimônio intelectual indissociável do órgão. É vedada a cessão de exclusividade ou a perda de acesso a esses ativos para fornecedores externos.

III - Preferência por Modelos de Código Aberto (Open-Source): Sempre que viável técnica e economicamente, o órgão priorizará o uso e a implantação local ou em nuvem governamental de modelos de IA de código aberto. Essa medida visa garantir a perenidade do sistema independentemente das oscilações de mercado ou mudanças de políticas comerciais de empresas privadas.

IV - Documentação do Conhecimento Humano: Nenhum fluxo de trabalho automatizado por IA poderá ter sua lógica conhecida exclusivamente pelo algoritmo. O processo de negócio deve ser obrigatoriamente documentado em manuais de procedimentos internos geridos por servidores da Defensoria Pública.

#### Seção III - Do Desenvolvimento de Pessoas e Letramento em IA

**Art. 16.** A DPRJ promoverá programas continuados de capacitação, formação ética e letramento digital voltados a agentes internos, focando nos seguintes aspectos:

I - Uso consciente e seguro das tecnologias de IA, com ênfase nas boas práticas de engenharia de comandos (prompts), privacidade e segurança de dados;

II - Noções de vieses algorítmicos, limites técnicos dos sistemas geradores de linguagem e identificação de desinformação;

III - Treinamento prático nos ambientes de IA Institucional homologados pela Defensoria Pública.

Parágrafo único. O treinamento em boas práticas de uso seguro de ferramentas de IA integrará a grade de capacitação obrigatória para novos agentes internos e prestadores de serviço, devendo ser concluído em até 60 (sessenta) dias após sua admissão, em estrita consonância com o Art. 11, § 1º da Resolução DPRJ nº 1363/2025.

#### Seção IV - Do Direito à Contestação

**Art. 17.** A DPRJ disponibiliza, em seu site institucional, de forma acessível e gratuita, mecanismos para o exercício do direito de contestação e solicitação de revisão humana nos casos de decisões, manifestações ou triagens baseadas, no todo ou em parte, em sistemas de Inteligência Artificial.

### TÍTULO VI - DISPOSIÇÕES FINAIS E TRANSITÓRIAS

**Art. 18.** Os contratos de prestação de serviços tecnológicos, desenvolvimento de software e aquisição de soluções que envolvam o uso de Inteligência Artificial na DPRJ deverão conter cláusulas expressas de:

I - Conformidade estrita com a LGPD, com as normas de Segurança da Informação da DPRJ e com as premissas de segurança cibernética estabelecidas pelo CGSI;

II - Compromisso de auditoria técnica contratual e fornecimento de documentação explicativa sobre o funcionamento dos algoritmos;

III - Todo edital de licitação ou termo de contratação de sistemas de IA deve conter cláusulas explícitas de portabilidade, exigindo que o fornecedor entregue, ao fim do contrato ou por solicitação do órgão, todos os dados, logs de auditoria e parametrizações em formatos abertos e interoperáveis.

**Art. 19.** Os casos omissos ou excepcionais relativos à aplicação desta Resolução serão decididos pelo Comitê de Governança de TI (CGTI) da DPRJ, ouvidos o Comitê Gestor de Segurança da Informação (CGSI) e a(o) Encarregada(o) pelo Tratamento de Dados Pessoais (EPD), conforme suas respectivas competências.

**Art. 20.** Esta Resolução entra em vigor na data de sua publicação, revogando-se todas as disposições em contrário.

Parágrafo único. Esta Política será revisada periodicamente ou extraordinariamente a qualquer tempo sempre que houver modificações legislativas nacionais ou evoluções tecnológicas substanciais que exijam adequação célere.

PAULO VINÍCIUS COZZOLINO ABRAHÃO
Defensor Público-Geral do Estado do Rio de Janeiro
