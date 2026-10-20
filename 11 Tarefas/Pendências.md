---
tipo: guia
tags:
  - tarefa
---

# Pendências

Fonte única das tarefas do iLab. Cada tarefa é uma nota nesta pasta, com responsável, prazo e status (aberta, em andamento, feita). As tabelas abaixo, nas notas das pessoas e nas atas se atualizam sozinhas. A Google Agenda fica só como lembrete.

## Em aberto
```base
filters:
  and:
    - 'tipo == "tarefa"'
    - 'status != "feita"'
formulas:
  situacao: 'if(status == "feita", "feita", if(prazo < today(), "atrasada", status))'
views:
  - type: table
    name: Em aberto por prazo
    order:
      - file.name
      - responsavel
      - prazo
      - formula.situacao
    sort:
      - property: note.prazo
        direction: ASC
```

## Por responsável
```base
filters:
  and:
    - 'tipo == "tarefa"'
    - 'status != "feita"'
formulas:
  situacao: 'if(status == "feita", "feita", if(prazo < today(), "atrasada", status))'
views:
  - type: table
    name: Em aberto por responsável
    groupBy:
      property: note.responsavel
      direction: ASC
    order:
      - file.name
      - responsavel
      - prazo
      - formula.situacao
    sort:
      - property: note.prazo
        direction: ASC
```

## Feitas
```base
filters:
  and:
    - 'tipo == "tarefa"'
    - 'status == "feita"'
formulas:
  situacao: 'if(status == "feita", "feita", if(prazo < today(), "atrasada", status))'
views:
  - type: table
    name: Feitas
    order:
      - file.name
      - responsavel
      - prazo
      - formula.situacao
    sort:
      - property: note.prazo
        direction: ASC
```

## Como atualizar
- Mudou o andamento: troque `status` para `em andamento` e anote a data em **Andamento**.
- Concluiu: `status: feita` e a data em `concluida_em`.
- Tarefa nova: crie a nota aqui com o **Modelo - Tarefa** e ligue a reunião de origem em `origem`.
