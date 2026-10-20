---
tipo: reuniao
data: "{{date}}"
hora: 
convidados: 
falaram: 
projeto: 
fonte: 
gravacao: 
tags:
  - reuniao
---

# {{title}}

> Guarde em `09 Reuniões` com o nome `AAAA-MM-DD - Nome da reunião`. Se houver transcrição, crie a nota em `09 Reuniões/Transcrições` e ligue as duas.

## Resumo

## Decisões

## Próximas etapas
Crie uma nota por tarefa em `11 Tarefas` (Modelo - Tarefa) com `origem` apontando para esta reunião.

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
- 
