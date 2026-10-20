---
tipo: reuniao
data: 2026-10-20
hora: 
convidados:
  - Marcelle
  - Debora
  - Virgínia
  - Jane
  - Nicole
falaram: 
projeto: 
fonte: 
gravacao: 
prazo: 2026-11-05
tags:
  - reuniao
  - quinzenal
---

# Reunião quinzenal (20/10)

## Resumo

Reunião quinzenal do iLab. Registro das tarefas que ficaram para a próxima reunião quinzenal, em 05/11/2026.

## Decisões

- Prazo das tarefas abaixo: próxima reunião quinzenal, **05/11/2026**.
- Teste em campo do CREDCESTA na UERJ marcado para **22/10/2026**.

## Próximas etapas
As tarefas desta reunião ficam em `11 Tarefas` (ver [[Pendências]]). A tabela abaixo mostra o status atual.

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

## Relacionado
- [[Maria - atendimento automatizado]]
- [[2026-10-16 - Serviços MarIA - CREDCESTA]]
- [[Tykhe]]
