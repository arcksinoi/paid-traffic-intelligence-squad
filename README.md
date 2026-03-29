# Paid Traffic Intelligence Squad 🎯

**Paid Traffic Intelligence** é uma skill/squad completo de ponta-a-ponta para analisar painéis de anúncios (Meta Ads, Google Ads, TikTok Ads), auditar páginas de vendas e montar novos planos de ação para escalar campanhas e ROAS (Retorno Sobre Investimento).

Construído via arquitetura *AIOS Nirvana Squad Creator*.

## 🌟 Visão Geral

O squad usa 5 agentes hiper-especializados, treinados para trabalhar em cadeia:
1. **Analista de Métricas** (`pti-metrics-analyst`): Enxerga imagens de Dashboards (screenshots) via visão computacional (LLMs Vision) para ler CTR, CPC, CPA, ROAS, Frequência, e Custo Por Clique. Identifica se o problema é o anúncio, o público ou a página.
2. **Arquiteto de Funil** (`pti-funnel-architect`): Avalia UX, Taxa de Carregamento e a Oferta na sua Landing Page.
3. **Copywriter de Conversão** (`pti-conversion-copywriter`): Cria os novos gatilhos, headlines e scripts (estilo Halbert/Brunson) baseados na falha identificada nas métricas.
4. **Estrategista Criativo** (`pti-creative-strategist`): Focado em imagem/audiovisual. Cria ângulos de vídeos UGC ou criativos estáticos focados em aumentar o Click-Through-Rate (CTR).
5. **Comandante da Campanha** (`pti-campaign-commander`): Sintetiza as partes. Entrega a você a planilha de ação final (Quais campanhas subir, quando desligar as velhas, orçamentos sugeridos CBO/ABO).

## 🚀 Como Instalar

Instale diretamente do repositório no GitHub usando o instalador de squads ou skills:
```bash
npx squads add arcksinoi/paid-traffic-intelligence-squad
```
ou, se preferir instalá-lo nativamente como skill:
```bash
npx skills add arcksinoi/paid-traffic-intelligence-squad
```

## 💻 Como Usar (Comandos Rápidos)

Você pode usar os comandos rápidos nativos da Skill para economizar tempo na sua IDE:

* **Análise de Métricas por Imagem**:
  Envie no PROMPT a imagem do seu Gerenciador de Anúncios e digite:
  `*analyze-traffic [imagem.png]`

* **Auditoria Completa de Funil (Landing Page)**:
  `*audit-lp www.seusite.com.br/lp` (Pode também enviar print da tela)

* **Refazer Copys ou Criativos**:
  `*new-copy "meu anúncio de dieta não converte mais"`
  `*new-creatives "preciso de 3 video scripts para remarketing"`

* **Estratégia e Planejamento Mídia**:
  `*campaign-plan "Tenho 500 reais por dia para investir em moda feminina, monte a estrutura"`

## 🛠️ Workflows

1. **`traffic-analysis-pipeline`**: Ocorre quando você envia um dashboard. Os dados passam do analista numérico para os criadores, devolvendo uma solução final unificada no Commander.
2. **`landing-page-audit`**: Ocorre na auditoria de LP. Envolve Arquiteto de Funil + Copywriter.
