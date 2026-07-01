---
tipo: exemplo-pratico
caso: Caso 1 · Análise comparativa das 3 unidades
uso: prática do M2 · Workshop IA MC & Fígaro
formato: xlsx (2 versões — limpa e com anomalias)
atualizado: 2026-07-01
---

# Vendas das 3 Unidades — Junho/2026

## Objetivo deste par de arquivos

Simular o dado que uma coordenadora do Grupo MC recebe do sistema: **planilha bruta de vendas do mês nas 3 unidades**. A tarefa é transformar isso em análise executiva pronta pra reunião com a Lilianne — em minutos, não em horas.

**Duas versões:**

| Arquivo | O que tem | Pra que serve |
|---|---|---|
| **01a · Versão LIMPA** | 185 vendas de jun/2026, dados internamente consistentes | Ver como a IA analisa dado "bom" |
| **01b · Versão COM ANOMALIAS** | Mesmos 185 registros + 3 anomalias plantadas | Ver como a IA detecta erro — **e reforçar por que revisão humana continua importante** |

**Como usar:**

1. Abra ChatGPT, Claude ou Gemini (versão paga aceita upload direto de .xlsx)
2. Rode o **mesmo prompt** (está na aba "Como usar com IA" de cada arquivo) primeiro no arquivo limpo, depois no arquivo com anomalias
3. Compare os dois outputs. A IA deve flaggar as 3 anomalias no segundo — mas veja **como** ela flagga, **onde** ela falha, e **o que ela sugere** vs. o que você faria diferente.

---

## Cenário

**Grupo Mulher Cheirosa & Fígaro** — 3 unidades:

| Unidade | Cidade | Perfil | Ticket médio esperado |
|---|---|---|---|
| Maison Aldeota | Fortaleza | Rua, tradicional desde 1987, clientela fiel | Mais alto (~R$ 650–750) |
| RioMar Papicu | Fortaleza | Shopping, volume alto e passagem | Médio (~R$ 400–500) |
| RioMar Recife | Recife (PE) | Unidade mais nova, em crescimento | Médio (~R$ 420–500) |

**Portfólio de serviços considerado:**
Banho de Lua · Spa da Noiva · Cronograma Capilar · Micropigmentação · Massagem Modeladora · Design Sobrancelha + Henna · Depilação Cera Quente · Manicure/Pedicure Premium · Escova Premium · Terapia Capilar.

---

## Estrutura das abas

**Aba "Vendas"** — 1 linha por atendimento

| Coluna | Descrição |
|---|---|
| Data | 01/06/2026 a 30/06/2026 (sazonalidade: sex/sáb mais fortes) |
| Unidade | Maison Aldeota (FOR) · RioMar Papicu (FOR) · RioMar Recife |
| Serviço | 1 dos 11 do portfólio |
| Cliente (iniciais) | Padrão M.V.C. — anonimizado |
| Valor | R$ com 2 casas |
| Forma pagamento | Cartão Crédito 50% · Débito 20% · PIX 20% · Dinheiro 10% |

**Aba "Resumo por Unidade"** — pivô calculado

Atendimentos · Faturamento · Ticket médio · Top 2 serviços por unidade.

**Aba "Mix de Serviços"** — matriz serviço × unidade

Volume de cada serviço em cada unidade.

**Aba "Como usar com IA"** — prompt PCTFL completo, pronto pra colar.

---

## Anomalias plantadas na versão B (não conta pro participante — deixa ele achar)

1. **Valor negativo** — uma venda de R$ -450,00 em 14/06 na RioMar Papicu. Provável estorno mal classificado (deveria estar em categoria própria, não como venda).
2. **Valor 10× acima** — Spa da Noiva de R$ 25.000,00 em 21/06 na Maison. Preço típico do serviço é R$ 1.800–2.600. Provável erro de digitação (25.000 ao invés de 2.500).
3. **Unidade escrita inconsistente** — "Riomar Papicu" (sem "(FOR)", sem maiúscula no R) em 24/06. Quebra o agrupamento em SUMIFS e no dashboard da IA — pode inflar contagem de "unidades" para 4.

**Meta didática:** ao ver o output da versão B, o participante deve perceber que a IA **listou 2 das 3 anomalias como pontos de atenção** — não corrigiu sozinha. Reforça: IA é copiloto, humano decide.

---

## Insights que a IA deve entregar (versão limpa)

- **Ranking de faturamento** — RioMar Papicu lidera em volume, Maison em ticket médio, RioMar Recife é a menor
- **Mix por unidade** — Cronograma Capilar/Micropigmentação forte na Maison; Banho de Lua/Manicure forte em RioMar Papicu
- **Hipótese de perfil** — Maison retém cliente que compra pacote longo; RioMar Papicu capta cliente de passagem com ticket médio
- **Recomendação** — cross-sell de Cronograma Capilar para clientes de Banho de Lua na RioMar Papicu (base grande, ticket a subir)

---

## Conexão com o M2 do workshop

Este arquivo alimenta o **Caso 1 · Análise comparativa das 3 unidades** (M2 · Bloco 1). Serve também como base para o Caso 3 (relatório executivo) — dá pra rodar os dois prompts em cima do mesmo arquivo se quiser.

> **Segurança:** dados fictícios. No dia a dia real da MC, aplique o mesmo protocolo — iniciais nunca com nome completo, e dados sensíveis só em ferramenta corporativa autorizada.
