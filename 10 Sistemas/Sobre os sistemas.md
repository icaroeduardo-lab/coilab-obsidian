---
tipo: guia
tags:
  - sistema
---

# Sobre os sistemas

Referência dos sistemas externos e corporativos com que os projetos do laboratório se integram (ex.: Tykhe, Verde). Uma nota por sistema: o que é, como integramos, API, autenticação, pontos de atenção e perguntas em aberto.

## Como registrar um sistema
1. Crie uma nota nesta pasta com o nome do sistema.
2. Rode **Inserir modelo** (`Ctrl+P`) e escolha **Modelo - Sistema**.
3. Liste em `projetos` as notas de `07 Projetos` que dependem dele. A tabela na [[Início|página inicial]] mostra todos.

## Regras
- **Nunca** registrar token, senha, chave de API ou `.env`. Só o mecanismo (ex.: "Bearer JWT") e onde a credencial é obtida.
- Especificações originais (OpenAPI/Swagger) vão em `10 Sistemas/anexos/`, linkadas na nota. A nota resume; o anexo é a fonte.
- Documentação que exige login: registrar a URL e a data em que o anexo foi exportado (`atualizado_em`).
