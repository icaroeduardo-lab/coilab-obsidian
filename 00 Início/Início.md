---
tipo: inicio
---

# COILAB: base de conhecimento

Página inicial do COILAB (Coordenação do Laboratório de Inovação e Inteligência Artificial da DPRJ): cultura, treinamentos, cursos, eventos, reuniões, normativos, projetos, inventário de IA e sistemas integrados.

## Como usar

- Para criar uma nota nova, crie o arquivo na pasta certa e use **Inserir modelo** (paleta de comandos, `Ctrl+P`), escolhendo o modelo correspondente em `99 Modelos`.
- Preencha as propriedades no topo da nota (status, datas, responsável). As tabelas abaixo se atualizam sozinhas.

## Projetos

```base
filters:
  and:
    - file.inFolder("07 Projetos")
    - 'tipo == "projeto"'
views:
  - type: table
    name: Projetos por etapa
    groupBy:
      property: note.etapa
      direction: ASC
    order:
      - file.name
      - status
      - unidade_demandante
      - responsavel
      - envolve_ia
      - prazo
```

## Inventário de IA

```base
filters:
  and:
    - file.inFolder("06 Inventário de IA")
    - 'tipo == "sistema-ia"'
views:
  - type: table
    name: Sistemas por nível de risco
    groupBy:
      property: note.nivel_risco
      direction: DESC
    order:
      - file.name
      - status
      - unidade_requisitante
      - fornecedor
      - ambiente
      - homologado_cgti
      - proxima_reavaliacao
```

## Sistemas

```base
filters:
  and:
    - file.inFolder("10 Sistemas")
    - 'tipo == "sistema"'
views:
  - type: table
    name: Sistemas integrados
    order:
      - file.name
      - status
      - uso_no_coilab
      - autenticacao
      - projetos
      - atualizado_em
```

## Cultura

```base
filters:
  and:
    - file.inFolder("01 Cultura")
views:
  - type: table
    name: Práticas culturais
    order:
      - file.name
      - categoria
      - responsavel
      - atualizado_em
```

## Treinamentos

```base
filters:
  and:
    - file.inFolder("02 Treinamentos")
    - 'tipo == "treinamento"'
views:
  - type: table
    name: Treinamentos por status
    groupBy:
      property: note.status
      direction: ASC
    order:
      - file.name
      - status
      - publico
      - responsavel
      - carga_horaria
```

## Cursos

```base
filters:
  and:
    - file.inFolder("03 Cursos")
    - 'tipo == "curso"'
views:
  - type: table
    name: Cursos por status
    groupBy:
      property: note.status
      direction: ASC
    order:
      - file.name
      - status
      - plataforma
      - quem_fez
      - data_conclusao
```

## Eventos e palestras

```base
filters:
  and:
    - file.inFolder("08 Eventos")
    - 'tipo == "evento"'
views:
  - type: table
    name: Eventos
    order:
      - file.name
      - data
      - local
      - quem_foi
```

```base
filters:
  and:
    - file.inFolder("08 Eventos")
    - 'tipo == "palestra"'
views:
  - type: table
    name: Palestras
    order:
      - file.name
      - data
      - instituicao
      - tema
```

## Reuniões

```base
filters:
  and:
    - file.inFolder("09 Reuniões")
    - 'tipo == "reuniao"'
views:
  - type: table
    name: Reuniões
    order:
      - file.name
      - data
      - projeto
      - falaram
```

## Normativos

```base
filters:
  and:
    - file.inFolder("05 Normativos")
views:
  - type: table
    name: Normativos
    order:
      - file.name
      - orgao
      - assunto
      - processo
      - status
```

## Pessoas

```base
filters:
  and:
    - file.inFolder("04 Pessoas")
views:
  - type: table
    name: Pessoas
    order:
      - file.name
      - funcao
      - entrada
```
