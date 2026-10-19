---
tipo: projeto
etapa: triagem
status: ativo
dimensao: projetos
unidade_demandante: Defensoria Pública do Estado da Bahia (DPBA)
responsavel: COILAB
parceiros: DPBA, COPPE
envolve_ia: sim
sistema_ia: "[[Maria]]"
inicio: 2026-10-15
prazo: 
dedicacao: tempo reservado toda semana
tags:
  - projeto
  - maria
---

# Compartilhamento da MarIA com a Bahia

> Valores sugeridos: **etapa** demanda, triagem, priorizado, protótipo, piloto, implantação, concluído, encerrado. **status** ativo, pausado, concluído, encerrado. **dimensao** cultura, capacitação, prospecção, projetos, governança.

## Demanda
- Problema real e quem sofre com ele: a DPBA quer adotar a MarIA (atendimento digital da DPRJ) e pediu o código-fonte, a lógica de negócio e apoio para implantar. Outras defensorias (DF, RS, ES) também já demonstraram interesse, então o modelo definido aqui vale para os próximos pedidos.
- Quem trouxe: Defensoria da Bahia, com apoio da administração da DPRJ (Defensora Pública Geral e Dr. Paulo).

## Triagem
- Cabe ao laboratório? Por quê: sim. O COILAB precisa definir como compartilhar sem sobrecarregar a equipe da DPRJ nem consumir o contrato da COPPE com demandas da Bahia.
- Alinhamento estratégico: fortalecer a MarIA nacionalmente, de forma colaborativa.
- Impacto x esforço: esforço ainda não estimado. Filipe Braida lista as melhorias para generalizar o sistema e Gustavo Pinto estima PF e UST a partir dessa lista.

## O que vamos fazer
Definir e executar o modelo de transferência da MarIA para a DPBA: o que a Bahia precisa ter (órgãos, integrações, infraestrutura, equipe), como o código será compartilhado e mantido, e quanto esforço isso custa para a DPRJ. O ponto de partida é o documento [[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]], escrito pelo Iran.

### Rotina
- Vamos reservar um tempo toda semana para este projeto.
- Dia e horário: 

### Frentes
| Frente | Pergunta principal | Quem |
|---|---|---|
| Negócio | A DPBA tem órgãos equivalentes ao NAD, POMAR e CRC? | Iran, Camila |
| Integrações | Broker de mensagens da Bahia e integração com o SOLAR | DPBA |
| Infraestrutura | Precisa ser AWS? S3, Redis, LLM e requisitos de máquina | Braida |
| Governança de código | Repositório central, PRs, adapters Verde/Solar, quem corrige bugs | Icaro, Iran |
| Contrato | Convênio, cessão de uso e limite do contrato da COPPE | Diogo, Frederico |
| Esforço | Estimativa de PF e UST da generalização | Braida, Gustavo |

## Decisões até agora
- 2026-10-15: o fluxo de divórcio em diante entra direto no novo motor da MarIA ([[2026-10-15 - Compartilhamento MarIA - Melhores práticas]]).
- 2026-10-16: a DPRJ vai ceder o código da MarIA para a DPBA ([[2026-10-16 - Compartilhamento MarIA]]).
- 2026-10-16: Braida lista as tarefas de generalização e Gustavo estima PF e UST a partir dela.
- Em aberto: modelo técnico de compartilhamento (centralizado, segregado ou híbrido) e volume de UST a consumir.

## Próximos passos
- [ ] Icaro: estudar governança de repositórios, controle de acesso e versionamento, e compartilhar com o Iran.
- [ ] Iran: mapear requisitos de pessoas, TI, IA, suporte e fluxos para a implantação.
- [ ] Braida: listar melhorias para generalizar o sistema (logos, nomes, GovBR opcional).
- [ ] Gustavo: estimar PF e UST a partir da lista do Braida.
- [ ] Diogo: revisar as cláusulas do convênio sobre compartilhamento de código.
- [ ] Camila: apresentar cenário e impactos para a Dra. Anderson.
- [ ] Grupo: reunião técnica com a equipe da Bahia, depois que eles estudarem a documentação.
- [ ] Redigir o Acordo de Cooperação Técnica (ACT) com as limitações do contrato da COPPE e as regras de governança de código.

## Indicadores
| Tipo | Indicador | Meta | Resultado |
|---|---|---|---|
| Esforço | Horas da equipe DPRJ por semana no projeto |  |  |
| Processo | Prazo de resposta às dúvidas técnicas da DPBA | até 5 dias úteis |  |
| Resultado | MarIA em produção na DPBA |  |  |

## Decisão
- Data e instância:
- Decisão: seguir, ajustar ou encerrar
- Justificativa:

## Implantação e escala
- Área executora: COILAB, com DPBA responsável pelas próprias integrações
- Processo documentado em:

## Reuniões

```base
filters:
  and:
    - file.inFolder("09 Reuniões")
    - 'tipo == "reuniao"'
    - file.hasLink(this.file)
views:
  - type: table
    name: Reuniões do projeto
    order:
      - file.name
      - data
```

## Aprendizados
Registrar mesmo se o projeto for encerrado (fracasso produtivo).

## Relacionado
- [[Maria - atendimento automatizado]]
- [[Maria]] (inventário de IA)
- [[Análise e Planejamento de Transferência Tecnológica - MarIA (DPRJ-DPBA)]]
