---
name: paid-traffic-intelligence
description: "Squad e Skill para Análise Avançada de Tráfego Pago, Copywriting e Funis de Conversão."
license: MIT
compatibility: "Claude Code, Codex, Gemini CLI, Cursor, Antigravity, Windsurf, OpenCode"
allowed-tools: Read Write Edit Bash(ls:*)
argument-hint: "[command] [args]"
metadata:
  author: AIOS
  version: "1.0.0"
---

# Paid Traffic Intelligence Skill

This skill acts as an AIOS Squad orchestrator and natively handles user intents regarding paid traffic, ad campaigns, and conversion rate optimization (CRO) inside the IDE.

## Intent Classification Engine

Given ANY request related to paid traffic, ad metrics, copywriting, or landing page audits, classify into one intent, then use tools or execute workflows based on this:

```
User request → Classify:
│
├─ ANALYZE_METRICS → User wants to analyze a screenshot of an Ads Manager dashboard (Facebook/TikTok/Google).
│  ACTION: Read image constraints and execute the `traffic-analysis-pipeline` workflow.
│
├─ AUDIT_FUNNEL → User provides a landing page URL or screenshot for CRO audit.
│  ACTION: Execute the `landing-page-audit` workflow.
│
├─ COPYWRITING → User needs new ad body text, headlines, or VSL scripts.
│  ACTION: Activate `pti-conversion-copywriter` agent directly.
│
├─ CREATIVES → User needs ideas for new creatives (video angles, static images) to overcome ad fatigue.
│  ACTION: Activate `pti-creative-strategist` agent directly.
│
└─ STRATEGY → User needs media buying budget allocation, CBO/ABO strategies, and campaign scaling.
   ACTION: Activate `pti-campaign-commander` agent directly.
```

## Intent Detection Keywords

| Intent | Triggers |
|--------|----------|
| **ANALYZE_METRICS** | analisar métricas, cpa alto, roas baixo, ler dashboard, print de anuncios, metrics, ctr, ad manager |
| **AUDIT_FUNNEL** | analisar landing page, lp, funil de conversao, pagina de vendas, checkout, taxa de conversão |
| **COPYWRITING** | escrever copy, novos textos, melhor headline, script vsl, copywriting para anuncio |
| **CREATIVES** | ideias de criativos, novos ads, roteiro de video, ad fatigue, angulos de criativo, ugc |
| **STRATEGY** | planejar campanha, escalar anuncio, distribuir orcamento, cbo, abo, publicos estruturados |

## Quick Commands (Slash Commands)

If the user types a shortcut, use the corresponding action immediately:

| Command | Action |
|---------|--------|
| `*analyze-traffic [caminho_da_imagem]` | Run task `analyze-dashboard-image.md` -> run workflow `traffic-analysis-pipeline` |
| `*audit-lp [url_ou_caminho]` | Run workflow `landing-page-audit` |
| `*new-copy [contexto]` | Route to `pti-conversion-copywriter` |
| `*new-creatives [contexto]` | Route to `pti-creative-strategist` | 
| `*campaign-plan [objetivo_orcamento]` | Route to `pti-campaign-commander` |

## Usage Protocol
Quando ativar essa skill ou interagir com um usuário, siga estritamente estas regras de interação:

1. **Intake / Coleta de Dados**: Se o usuário solicitar uma "análise de campanha" ou "ajuda com tráfego" de forma genérica, **NÃO execute o fluxo de imediato**. Primeiro, responda pedindo tudo que é necessário para a análise:
   - A imagem/print do gerenciador de anúncios contendo as métricas (CTR, CPA, ROAS, Frequência).
   - O orçamento disponível.
   - O objetivo da campanha e a URL da página de destino (se aplicável).
   - *Só avance para invocar o `traffic-analysis-pipeline` quando ele fornecer esses dados.*

2. **Dashboard Web Interativo (HTML/CSS)**: Quando o fluxo terminar e o comandante compilar todas as sugestões, você deve **gerar e salvar um arquivo `dashboard.html`** no repositório do usuário contendo o relatório completo.
   - Construa uma página web linda e premium (usando glassmorphism, micro-animações, layout moderno) para hospedar as métricas falhas, a nova copy e o novo plano de mídia formulado pelo squad.
   - Sua resposta no chat não deve ser um textão enorme de markdown; apenas notifique que o site relacional (relatório interativo) foi gerado e instrua o usuário a abrir o arquivo HTML em seu navegador.
