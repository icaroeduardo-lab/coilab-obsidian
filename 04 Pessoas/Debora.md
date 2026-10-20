---
tipo: pessoa
status: ativo
funcao: 
entrada: 
projetos:
  - "[[Maria - atendimento automatizado]]"
proxima_entrega: 2026-11-05
ultima_conversa: 
tags:
  - pessoa
---

# Debora

> Função e data de entrada ainda não registradas: preencha quando souber.

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

## Contexto
- O fluxo de divórcio e os serviços do CREDCESTA foram discutidos em [[2026-10-16 - Serviços MarIA - CREDCESTA]] (Debora não aparece nessa ata).

## Histórico de reuniões
- 2026-10-20: [[2026-10-20 - Reunião quinzenal]] (convidada; tarefas combinadas nessa reunião)

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
- 

## Cursos feitos
- 

## Próximos passos de desenvolvimento
- 
