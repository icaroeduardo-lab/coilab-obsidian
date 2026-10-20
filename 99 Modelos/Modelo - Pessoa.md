---
tipo: pessoa
status: ativo
funcao: 
entrada: 
projetos: 
proxima_entrega: 
ultima_conversa: 
tags:
  - pessoa
---

# {{title}}

## Tarefas atuais
Tarefas em aberto desta pessoa (fonte: [[Pendências]]).

```base
filters:
  and:
    - 'tipo == "tarefa"'
    - file.hasLink(this.file)
    - 'status != "feita"'
formulas:
  situacao: 'if(status == "feita", "feita", if(prazo < today(), "atrasada", status))'
views:
  - type: table
    name: Tarefas em aberto
    order:
      - file.name
      - responsavel
      - prazo
      - formula.situacao
    sort:
      - property: note.prazo
        direction: ASC
```

## Histórico de reuniões
- AAAA-MM-DD: [[]]

## Conversas individuais
```base
filters:
  and:
    - 'tipo == "conversa-individual"'
    - file.hasLink(this.file)
views:
  - type: table
    name: Conversas individuais
    order:
      - file.name
      - data
      - proxima_conversa
```

## Treinamentos concluídos
- [[]]

## Cursos feitos
- [[]]

## Próximos passos de desenvolvimento
- 
