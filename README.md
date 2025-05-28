# 📦 Olist Analytics — Processamento Analítico de Dados

Este projeto consiste na modelagem e análise analítica de dados públicos da Olist. Foram investigados três processos críticos:

- Desempenho de vendas

- Funil de marketing

- Satisfação do cliente

Utilizamos modelagem dimensional para construir um data warehouse e exploramos os dados com operações OLAP, identificando oportunidades estratégicas e otimizando decisões comerciais no e-commerce.

## Estrutura Dimensional
Modelagem de três esquemas estrela, com as seguintes tabelas fato:

- fct_sales: Desempenho de vendas (grão: item de pedido)

- fct_funnel: Funil de marketing (grão: lead qualificado)

- fct_reviews: Avaliações de clientes (grão: review individual)

As tabelas estão associadas às dimensões:

- dim_date — Datas dos eventos

- dim_customer — Dados geográficos do cliente

- dim_product — Categoria do produto

- dim_seller — Localização do vendedor

- dim_campaign — Canal e origem de campanhas

- dim_business_segment — Segmento de negócio

- dim_price_range — Faixa de preço média do produto

## Consultas OLAP e Análises
1. Rentabilidade por Categoria (Roll-Up)
Agrega margem estimada, receita total e número de vendedores por categoria. Identifica os segmentos mais lucrativos.

2. Produtos com Baixa Concorrência (Drill-Down)
Explora produtos com ≤ 5 vendedores por categoria. Ideal para revelar oportunidades em nichos pouco explorados.

3. Classificação de Nichos Lucrativos e Bem Avaliados (Drill-Across)
Integra vendas e avaliações. Classifica categorias em:

- Nicho Ideal: alta margem, baixa concorrência, boa avaliação

- Nicho Promissor

- Nicho Regular

4. Conversão por Origem e Segmento (Slice and Dice + Pivot)
Analisa leads por origem e segmento, avaliando taxa de conversão, tempo médio para fechamento e volume.

5. Desempenho de Nichos Lucrativos (Drill-Across)
Integra marketing, vendas e satisfação por nicho e canal de aquisição. Revela quais nichos são sustentáveis e escaláveis.

## Algumas Descobertas
Região Sudeste lidera em receita, com destaque para São Paulo.

Categorias como health_beauty, watches_gifts e computers_accessories são altamente rentáveis.

Niches com ≤ 5 vendedores, como la_cuisine e arts_and_craftmanship, oferecem margens atrativas com baixa concorrência.

Canais orgânicos demonstram melhor eficiência de conversão no funil.


## 🛠️ Tecnologias Utilizadas
Python

Pandas

SQL (via pandasql)

Jupyter Notebook

Matplotlib / Seaborn (para visualizações)


### Autor
Arturo Kolster Borges
Nº USP: 16285381
Projeto desenvolvido para a disciplina de Processamento Analítico de Dados
Instituto de Matemática e Estatística (ICMC) — Universidade de São Paulo (USP)
