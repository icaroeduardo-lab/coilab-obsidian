---
tipo: guia
tags:
  - pessoa
---

# Carga da equipe

Tarefas em aberto agrupadas por responsável, com a contagem de cada grupo, e a data da última conversa individual de cada pessoa. Tudo se atualiza a partir das notas em `11 Tarefas` e `04 Pessoas`.

## Tarefas em aberto por pessoa
```base
filters:
  and:
    - 'tipo == "tarefa"'
    - 'status != "feita"'
formulas:
  situacao: 'if(prazo < today(), "atrasada", status)'
views:
  - type: table
    name: Carga por pessoa
    groupBy:
      property: note.responsavel
      direction: ASC
    order:
      - file.name
      - prazo
      - formula.situacao
    summaries:
      file.name: Count
```

## Última conversa individual
```base
filters:
  and:
    - file.inFolder("04 Pessoas")
    - 'tipo == "pessoa"'
    - 'status == "ativo"'
views:
  - type: table
    name: Conversas
    order:
      - file.name
      - ultima_conversa
      - proxima_entrega
      - projetos
    sort:
      - property: note.ultima_conversa
        direction: ASC
```

## Como ler
- Tarefa com duas responsáveis aparece no grupo das duas juntas (por exemplo "Debora, Virgínia"). Some esse grupo à carga de cada uma.
- Quem tem mais tarefas abertas é a primeira pessoa a checar antes de distribuir algo novo.
- `ultima_conversa` vazia ou antiga indica que vale marcar uma conversa individual (Modelo - Conversa individual).
