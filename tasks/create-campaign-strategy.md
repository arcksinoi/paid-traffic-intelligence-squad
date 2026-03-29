---
name: "Create Campaign Strategy"
id: "create-campaign-strategy"
description: "Centraliza informações, corta sugestões inúteis e estrutura a alocação de orçamentos e hierarquia de campanhas a subir no gerenciador."
trigger: "Último passo de todos workflows lógicos ou via `*campaign-plan`"
---
# Context
Gestores de tráfego se confundem em como estruturar publicações e testes de criativo versus tráfego frio e retenção. Essa task monta a planificação financeira de mídia.

# Objective
1. Recolha os relatórios de todos os times ativados antes de você (criativos e copies foram feitos no passo anterior?).
2. Liste em formato Markdown as diretrizes de "Mata X Escala". (Desativar camp X, Ativar Camp Y).
3. Crie o "Media Plan" claro:
    - **Campanha D1: CBO Teste de Criativos Frios**. Orçamento sugerido (proporcional caso o usuário tenha informado orçamento X).
    - **Campanha D2: ABO Remarketing**. 
    - Especifique quais criativos + quais copys de conversão sugeridos nas fases prévias devem ser acoplados nessa estratégia.
4. Toda a inteligência produzida deve ser programada e salva fisicamente em um **Dashboard Interativo em HTML/CSS (`dashboard.html`)**:
    - Gere este código com design premium estilo **Awwwards** (glassmorphism, sombras suaves, cores de alto nível, CSS nativo maravilhoso e responsivo).
    - O site deve conter as seções: **Gargalos Analisados** (KPIs em cards), **Ideias de Correção** (Tabelas do que Pausar x Subir de novo) e **Plano de Mídia** (Estrutura visual recomendada).
5. No chat com o usuário, apenas entregue um resumo hiper-curto avisando que o arquivo web `dashboard.html` foi gerado e está pronto para ser aberto no navegador.
