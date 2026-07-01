---
tipo: exemplo-pratico
caso: Caso 2 · Cross-sell de clientes
uso: prática do M2 · Workshop IA MC & Fígaro
formato: xlsx (2 versões — limpa e com anomalias)
atualizado: 2026-07-01
---

# Base de Clientes MC — 2º trimestre/2026

## Objetivo deste par de arquivos

Simular a base de clientes do Grupo MC no 2º trimestre: quem veio, qual serviço fez, quanto gastou. A pergunta que a IA responde: **quem entre as clientes que só fizeram Banho de Lua tem perfil para ser abordada para Spa da Noiva, Cronograma Capilar ou Massagem Modeladora?**

**Duas versões:**

| Arquivo | O que tem | Pra que serve |
|---|---|---|
| **02a · Versão LIMPA** | 100 clientes com dados consistentes | Base para o cross-sell "normal" |
| **02b · Versão COM ANOMALIAS** | Mesmos 100 + 4 sujeiras plantadas | Testar se a IA identifica cadastro furado |

**Como usar:**

1. Abra ChatGPT, Claude ou Gemini (paga aceita upload direto)
2. Rode o mesmo prompt (aba "Como usar com IA") nos dois arquivos
3. No output da versão limpa, veja as 3 mensagens de WhatsApp que a IA gerou
4. No output da versão com anomalias, veja se a IA listou os 4 registros suspeitos antes de gerar as mensagens

---

## Cenário

**Base de clientes do Grupo MC no 2º trimestre/2026** (abr–jun). Cada cliente aparece 1 vez, com o resumo do trimestre inteiro. Iniciais no lugar de nome (padrão de segurança MC).

**Distribuição por perfil:**

| Perfil | Qtd | Descrição |
|---|---|---|
| Só Banho de Lua | 25 | **Target primário do cross-sell** — quem veio para o BL e nada mais |
| Banho de Lua + outro | 20 | Já começou a comprar outros serviços — pode ampliar |
| Pacote noiva/Spa | 15 | Compra pacotes longos — cliente premium consolidada |
| Recorrentes de manicure/escova | 15 | Base fiel, alto giro, ticket menor |
| VIP (Micropigmentação/Terapia) | 15 | Ticket alto, serviços de alta margem |
| Novas | 10 | Só 1 visita no trimestre — precisa engajamento |

---

## Estrutura das abas

**Aba "Clientes"** — a base inteira

| Coluna | Descrição |
|---|---|
| ID | MC001, MC002, ... (padrão interno) |
| Iniciais | M.V.C. — anonimizado |
| Idade | 28–62 |
| 1ª visita | Data da primeira vez que veio ao grupo |
| Visitas 2º tri | Nº de vezes que veio abr–jun/2026 |
| Serviços realizados 2º tri | Lista separada por `;` |
| Ticket total 2º tri | Soma gasta no trimestre |
| Última visita | Data |
| Unidade preferencial | Onde a cliente foi atendida mais vezes |

**Aba "Só Banho de Lua"** — filtro do target primário

Mesma estrutura, mas só as 25 clientes que fizeram exclusivamente Banho de Lua no trimestre. Facilita a IA analisar o perfil sem se perder nas outras.

**Aba "Resumo"** — indicadores gerais da base

Total de clientes · ticket médio · faturamento total · distribuição por perfil.

**Aba "Como usar com IA"** — prompt PCTFL de cross-sell.

---

## Anomalias plantadas na versão B

1. **Idade 12** — impossível para o portfólio adulto da MC. Erro de cadastro (talvez ano de nascimento invertido).
2. **Última visita 12/03/2028** — data futura. Erro de digitação (talvez 2026).
3. **Ticket total R$ -820,00** — negativo. Provável estorno mal classificado.
4. **Cliente duplicada** — o registro MC016 aparece de novo como MC101, com os mesmos dados. Duplicação no CRM.

**Meta didática:** ao rodar o prompt na versão B, a IA deve listar essas 4 sujeiras **antes** de fazer o cross-sell — não tratá-las como dado válido. Se ela tratar como dado válido, o resultado do cross-sell fica contaminado (inclui cliente de 12 anos, ticket errado no cálculo etc.).

---

## Insights que a IA deve entregar (versão limpa)

- **Perfil do target primário** — idade média, ticket típico, frequência
- **Qual característica indica propensão a Spa da Noiva** — provável correlação com idade + ticket + frequência
- **3 mensagens de WhatsApp personalizadas** no tom MC (sofisticado, acolhedor, feminino, sem emoji)
- **Recomendação do segmento** com melhor custo/benefício para começar a campanha

---

## Conexão com o M2 do workshop

Este arquivo alimenta o **Caso 2 · Cross-sell de clientes** (M2 · Bloco 2). Também pode ser combinado com o Arquivo 3 (dados executivo) para o Caso 3 — cross-sell de clientes que reclamaram no mês, por exemplo.

> **Segurança:** dados fictícios. Reforço do módulo: nunca cole dados de clientes com nome completo, CPF ou telefone em conta pessoal de IA. Iniciais + apelidos genéricos, sempre.
