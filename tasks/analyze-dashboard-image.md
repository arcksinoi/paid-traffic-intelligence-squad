---
name: "Analyze Dashboard Image"
id: "analyze-dashboard-image"
description: "Extrai métricas e KPIs via leitura OCR/Vision de fotos de dashboard de ferramentas como Meta ou Google Ads."
trigger: "Quando o usuário envia um print da tela preta de métricas ou resultados isolados"
---
# Context
A conversão muitas vezes estagna e o gestor fica com "cegueira das métricas". A visão computacional isolada em um agente tira o emocional e lê apenas o frio KPI.

# Objective
1. Leia o "Screenshot" fornecido de fora a fora.
2. Identifique nomes de campanhas/anjuntos.
3. Extraia o CTR, CPA, CPC, CPM e ROAS (se visível). 
4. Crie uma tabela Markdown limpa com esses dados (Dashboard).
5. Se CTR de link for Menor que 1%, escreva em negrito "Atenção: Criativo em colapso".
6. Se o CPC for R$0.50 e nenhuma venda ocorreu, escreva "Atenção: LP falhando na conversão". 
7. Envie a análise formatada para os próximos agentes na cadeia.
