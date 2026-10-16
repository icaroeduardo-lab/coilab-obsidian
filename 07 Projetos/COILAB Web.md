---
tipo: projeto
etapa: implantação
status: ativo
dimensao: governança
unidade_demandante: COILAB
responsavel: COILAB
parceiros: 
envolve_ia: não
sistema_ia: 
inicio: "2026-04-24"
prazo: 
repositorio: https://github.com/dgd-dprj/coilab-web
tags:
  - projeto
---

# COILAB Web

> Valores sugeridos: **etapa** demanda, triagem, priorizado, protótipo, piloto, implantação, concluído, encerrado. **status** ativo, pausado, concluído, encerrado. **dimensao** cultura, capacitação, prospecção, projetos, governança.

## Demanda
- Problema real e quem sofre com ele: o laboratório precisa gerenciar seus projetos, tarefas e entregas num só lugar.
- Quem trouxe: o próprio COILAB.

## Triagem
- Cabe ao laboratório? Por quê: é a ferramenta interna de gestão do portfólio do laboratório.
- Alinhamento estratégico: 
- Impacto x esforço: 

## Hipótese e protótipo
- O que vamos testar: 
- Como saberemos que deu certo (critério de sucesso): 
- Critério de saída (quando paramos): 

## Como é feito
- **Front-end:** Next.js (`apps/web`), publicado no AWS Amplify.
- **Back-end:** NestJS + Prisma + PostgreSQL (`apps/api`), publicado com Serverless na AWS via GitHub Actions.
- **Domínio:** projetos, tarefas e subtarefas, com setor solicitante e fluxo associados; numeração sequencial `#AAAAnnnn`.
- Regras de negócio: `apps/api/docs/business-rules.md` no repositório.

## Indicadores
| Tipo | Indicador | Meta | Resultado |
|---|---|---|---|
| Esforço |  |  |  |
| Processo |  |  |  |
| Resultado |  |  |  |

## Decisão
- Data e instância:
- Decisão: seguir, ajustar ou encerrar
- Justificativa:

## Implantação e escala
- Área executora: COILAB
- Processo documentado em: [README do repositório](https://github.com/dgd-dprj/coilab-web)

## Aprendizados


## Relacionado
- [[Sobre os projetos]]
- [[Maria - atendimento automatizado]]
