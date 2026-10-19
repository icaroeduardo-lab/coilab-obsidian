---
tipo: projeto
etapa: implantação
status: ativo
dimensao: projetos
unidade_demandante: 
responsavel: COILAB
parceiros: 
envolve_ia: sim
sistema_ia: "[[Maria]]"
inicio: 
prazo: 
repositorio: https://github.com/dgd-dprj/maria-langgraph-pp
tags:
  - projeto
---

# Maria: atendimento automatizado

> Valores sugeridos: **etapa** demanda, triagem, priorizado, protótipo, piloto, implantação, concluído, encerrado. **status** ativo, pausado, concluído, encerrado. **dimensao** cultura, capacitação, prospecção, projetos, governança.

## Demanda
- Problema real e quem sofre com ele: o cidadão que procura a Defensoria pelo chatbot precisa ter o pedido encaminhado com os dados reais do Verde, sem depender de uma pessoa em cada etapa.
- Quem trouxe: 

## Triagem
- Cabe ao laboratório? Por quê: 
- Alinhamento estratégico: 
- Impacto x esforço: 

## O que é
Ponte entre a **Tykhe** (chatbot que atende o cidadão por WhatsApp e web) e o **Verde** (sistema da Defensoria com os dados de pessoas, processos e órgãos de atendimento). Cada fluxo de atendimento é um grafo de estados (LangGraph) que faz as perguntas, consulta o Verde e termina em **concluído** (resolvido pelo bot) ou **transferência para atendimento humano**.

Fluxos implementados: **pessoa presa**, **violência doméstica** e um fluxo padrão para as demais categorias. Um orquestrador classifica o relato livre do cidadão para o fluxo certo.

## Hipótese e protótipo
- O que vamos testar: 
- Como saberemos que deu certo (critério de sucesso): 
- Critério de saída (quando paramos): 

## Indicadores
| Tipo | Indicador | Meta | Resultado |
|---|---|---|---|
| Esforço |  |  |  |
| Processo |  |  |  |
| Resultado |  |  |  |

> O sistema já registra o desfecho de cada atendimento e tem painéis no Grafana: bons candidatos para os indicadores de processo e resultado.

## Decisão
- Data e instância:
- Decisão: seguir, ajustar ou encerrar
- Justificativa:

## Implantação e escala
- Área executora: COILAB
- Processo documentado em: [documentação do repositório](https://github.com/dgd-dprj/maria-langgraph-pp/tree/main/docs)

## Aprendizados
- 2026-08-31: a reescrita de perguntas por IA foi desligada depois de gerar frases estranhas em produção (ex.: "Essa é o Fulano presa?"). As perguntas voltaram a ter texto fixo.

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

## Relacionado
- [[Compartilhamento da MarIA com a Bahia]]
- [[Maria]] (inventário de IA)
- [[Tykhe]] (sistema integrado: canal do cidadão)
- [[Intimação por WhatsApp - boas práticas]]
- [[Cidadania Digital - TJMT e Governo de MT]]
