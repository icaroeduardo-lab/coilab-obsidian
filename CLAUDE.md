# Convenções do vault (COILAB)

Regras para qualquer sessão do Claude que editar este vault. Migrado e adaptado do vault antigo `~/COILAB-vault` em 2026-10-14.

## Estrutura
- Pastas numeradas: `00 Início`, `01 Cultura`, `02 Treinamentos`, `03 Cursos`, `04 Pessoas`, `05 Normativos`, `06 Inventário de IA`, `07 Projetos`, `08 Eventos`, `09 Reuniões`, `10 Sistemas`, `11 Tarefas`, `99 Modelos`.
- Toda nota nova parte do modelo correspondente em `99 Modelos` e preenche as propriedades do topo: as tabelas (Bases) de `00 Início/Início.md` dependem delas (`tipo`, `status`, `etapa`…).
- Nome de arquivo: o título da nota em pt-BR, com acento e espaço (padrão atual do vault). Eventos e reuniões começam com data `AAAA-MM-DD - `.
- Links internos com `[[Nome da nota]]`.

## Idioma
- Tudo em pt-BR. Termos técnicos consagrados podem ficar em inglês (deploy, merge, backup).

## Regras
- Nenhum segredo, token, senha, chave de API ou `.env` no vault.
- Dado de cidadão, cliente ou processo: anonimizar antes de salvar.
- Nunca apagar nota. Obsoleta: `status: encerrado`/`arquivado` e registrar o motivo.
- Tarefa: o cofre é a fonte única. Uma nota por tarefa em `11 Tarefas` (Modelo - Tarefa) com `responsavel`, `prazo`, `status` (aberta, em andamento, feita) e `origem`. Atas e notas de pessoas só exibem tarefas por tabela (Bases), sem copiar. A Google Agenda é só lembrete.
- Projeto que envolve IA: cadastrar também em `06 Inventário de IA` e ligar pela propriedade `sistema_ia`.
- Sistema externo (Tykhe, Verde…): nota em `10 Sistemas`; especificação original em `10 Sistemas/anexos/`.
