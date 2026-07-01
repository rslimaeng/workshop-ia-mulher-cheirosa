---
tipo: exemplo-pratico
caso: Caso 3 · Relatório executivo para diretoria
uso: prática do M2 · Workshop IA MC & Fígaro
formato: xlsx (2 versões — limpa e com anomalias)
atualizado: 2026-07-01
---

# Dados Executivo MC — Junho/2026

## Objetivo deste par de arquivos

Simular o "caderno da coordenadora" no fim do mês: métricas quantitativas de um lado, situações qualitativas do outro. A pergunta que a IA responde: **como transformar isso num relatório executivo de 1 página que a Lilianne consegue ler em 5 minutos?**

**Duas versões:**

| Arquivo | O que tem | Pra que serve |
|---|---|---|
| **03a · Versão LIMPA** | Métricas mai vs jun das 3 unidades + 16 anotações do mês | Ver como a IA estrutura relatório executivo "normal" |
| **03b · Versão COM ANOMALIAS** | Mesmos dados + 3 sujeiras plantadas | Ver como a IA detecta dado suspeito e separa "atenção operacional" de "atenção de dado" |

**Como usar:**

1. Abra ChatGPT, Claude ou Gemini (paga aceita upload direto)
2. Rode o mesmo prompt (aba "Como usar com IA") nas duas versões
3. Compare: o resumo executivo mudou? Os pontos de atenção mudaram? A IA distinguiu problema real de erro de cadastro?

---

## Estrutura das abas

**Aba "Métricas por Unidade"** — números consolidados

| Linha | O que traz |
|---|---|
| Faturamento | mai vs jun de cada unidade |
| Atendimentos | volume total no mês |
| Ticket médio | mai vs jun |
| Clientes novas (%) | proporção de primeira visita |
| Reagendamento (%) | quem já saiu agendando de novo |
| No-show (%) | não compareceu à data agendada |
| NPS | 0–100, mai vs jun |
| Serviço top 1 | serviço com mais volume no mês |
| Serviço top 2 | segundo colocado |

**Aba "Situações do Mês"** — anotações qualitativas

16 registros (na versão limpa) do jeito que chegam na mesa da coordenadora — misto de:

- **Elogios** de clientes (via depoimento, Google, WhatsApp)
- **Reclamações** com contexto (espera, política, resultado)
- **Operacional** (falta de material, equipamento, prazo)
- **Conquistas** (recorde, aniversário, meta batida)
- **Alertas** (concorrente novo, VIP não reagendou)

Formato: Data · Unidade · Categoria · Descrição.

**Aba "Como usar com IA"** — prompt PCTFL do relatório executivo.

---

## Anomalias plantadas na versão B

1. **Faturamento RioMar Recife 10× inflado** — R$ 714.000 no lugar de R$ 71.400. Erro de casa decimal. Se a IA não flaggar, o "faturamento total do grupo" fica inutilizável.
2. **Situação duplicada** — a anotação do aniversário da colaboradora L. Braga aparece 2 vezes (dia 15/06 na RioMar Papicu).
3. **Unidade inexistente** — uma anotação atribuída à "Unidade Iguatemi", que não existe no grupo. Provavelmente digitado errado.

**Meta didática:** ao rodar o prompt na versão B, a IA deve:
- Perceber que R$ 714.000 é fora do padrão e questionar antes de somar
- Não repetir a conquista duplicada no relatório
- Não inventar contexto para a unidade inexistente

Se a IA ignorar isso e somar tudo, o relatório executivo sai errado — e a Lilianne vai perguntar de onde veio o número.

---

## Insights que a IA deve entregar (versão limpa)

- **Resumo executivo em 3 linhas** com variação vs maio
- **Tabela das 5 métricas principais** com % de variação
- **Destaques por unidade** cruzando quantitativo com qualitativo (ex: "Maison — faturamento +5%, recorde de Spa da Noiva")
- **Pontos de atenção** priorizados — não todos os alertas, os 3 que exigem decisão
- **Recomendação com responsável e prazo**

---

## Conexão com o M2 do workshop

Este arquivo alimenta o **Caso 3 · Relatório executivo** (M2 · Bloco 3). É o momento onde a IA mais claramente **economiza tempo real** — o que a coordenadora leva 1h escrevendo, sai em 10 minutos.

> **Segurança:** dados fictícios. Em cenário real, esse relatório é para uso interno da diretoria — ferramenta corporativa autorizada, não conta pessoal grátis.
