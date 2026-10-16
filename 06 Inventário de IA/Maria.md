---
tipo: sistema-ia
status: em produção
nivel_risco: 
unidade_requisitante: 
fornecedor: AWS Bedrock (Anthropic)
modelo_ia: Claude 3 Haiku
ambiente: institucional
dados_pessoais: sim
aia: pendente
homologado_cgti: não
data_classificacao: 
proxima_reavaliacao: 
projeto: "[[Maria - atendimento automatizado]]"
tags:
  - inventario-ia
---

# Maria

> Inventário centralizado de IA (art. 12, II da [[Resolução DPRJ - Política de IA]]).
> Valores sugeridos: **status** em análise, piloto, em produção, descontinuado. **nivel_risco** I - Baixo, II - Médio, III - Alto, IV - Excessivo. **ambiente** institucional ou comercial. **aia** não se aplica, pendente, concluída.

> Cadastro feito a partir do repositório. Campos em branco e os marcados como "a confirmar" dependem de decisão do COILAB com a unidade requisitante. `homologado_cgti` e `aia` estão como "não" e "pendente" porque não há registro do contrário.

## Para que serve
Atende o cidadão que procura a Defensoria pelo chatbot (Tykhe), identifica qual atendimento ele precisa e coleta os dados com o Verde. Ver [[Maria - atendimento automatizado]].

## Como funciona
- Entradas: relato livre e respostas do cidadão (inclui CPF, RG, parentesco, número de processo e endereço).
- Saídas: escolha do fluxo de atendimento, texto da pergunta de desambiguação, resumo do relato e, opcionalmente, campos extraídos do texto.
- Onde a IA entra: 6 módulos que **classificam** o relato, **desambiguam**, **resumem**, **extraem** campos (desligado por padrão) e **reescrevem** perguntas (desligado desde 2026-08-31). Se a IA falhar, o fluxo segue sem ela.
- Onde a pessoa revisa (supervisão humana): as opções mostradas ao cidadão vêm do catálogo, nunca da IA; casos sem solução terminam em transferência para atendimento humano. Revisão de decisões por servidor: a confirmar.

## Classificação de risco (art. 5º)
- Nível: a confirmar. Sugestão: **II - Médio**, porque influencia o fluxo de atendimento sem decidir sozinho (art. 5º, II). Vale avaliar o III porque o atendimento toca direitos de assistidos (pessoa presa, violência doméstica).
- Justificativa: 
- Classificado por: COILAB e 

## Exigências do nível (art. 6º)
- [ ] Documentação técnica (simplificada no nível I, completa a partir do II). Base existente: pasta `docs/` do repositório.
- [ ] Aviso ao usuário de que há auxílio de IA
- [ ] Validação de segurança e supervisão humana documentada (nível II ou mais)
- [ ] Avaliação de Impacto Algorítmico, testes de viés e homologação no CGTI (nível III)
- [ ] Análise do CGSI (risco médio ou alto com impacto em segurança)
- [ ] Consulta à EPD (trata dados pessoais, art. 13)

## Soberania e contrato (arts. 15 e 18)
- Processo documentado fora do algoritmo: regras de cada fluxo em `docs/fluxo-*.md` do repositório.
- Prompts e bases de ajuste: no repositório, pasta `src/ia/`.
- Cláusulas de auditoria e portabilidade: 

## Histórico
- 2026-08-31: reescrita de perguntas por IA desligada após frases estranhas em produção.
- 2026-10-13: cadastro inicial no inventário, a partir do repositório.
