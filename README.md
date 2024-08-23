# Projeto de Análise de Dados sobre o Pré-Sal

## Resumo

Este projeto foca na análise e visualização de dados relacionados ao Pré-Sal, uma das maiores descobertas energéticas do Brasil e do mundo. Utilizando dados abertos da Agência Nacional do Petróleo, Gás Natural e Biocombustíveis (ANP), nossa meta é explorar o impacto econômico do Pré-Sal e avaliar a qualidade do petróleo e do gás natural extraídos, ajudando a prever tendências de produção e a identificar os poços mais promissores.

## 1. Introdução

O Pré-Sal é uma camada geológica rica em petróleo e gás natural, localizada sob o mar entre os estados de Espírito Santo e Santa Catarina. Desde sua descoberta em 2007, tornou-se uma área de grande importância econômica para o Brasil. Este projeto visa analisar esses recursos estratégicos, ajudando a entender seu impacto na economia nacional e global.

## 2. Objetivo

O objetivo do projeto é:
- Mapear e avaliar a produção de petróleo e gás em diferentes poços ao longo dos anos.
- Traçar o perfil químico do material extraído nas bacias e campos de exploração.
- Comparar a produção anual de petróleo e gás.
- Avaliar a produção diária em diferentes níveis hierárquicos, identificando os poços mais promissores.

## 3. Justificativa

Analisar dados históricos de produção de petróleo e gás é essencial para entender o impacto econômico do Pré-Sal e planejar estratégias futuras. Este projeto permitirá criar relatórios detalhados e projeções confiáveis, essenciais para o setor de óleo e gás até 2050.

## 4. Arquitetura do Projeto

### 4.1 Fonte de Dados

Os dados utilizados provêm do conjunto "Produção de Petróleo e Gás Natural por Poço", disponibilizado pela ANP, e são acessíveis [aqui](https://dados.gov.br/dados/conjuntos-dados/produo-de-petrleo-e-gs-natural-por-poo). A ANP oferece relatórios mensais e anuais desde 2005, em formato CSV.

### 4.2 Metodologia (ETL - Extrair, Transformar e Carregar)

1. **Extração**:
   - Os dados são extraídos da ANP para um servidor local e organizados em arquivos anuais.

2. **Transformação**:
   - Os arquivos são carregados na Azure e transformados de CSV para Parquet usando o Azure Data Factory, facilitando o processamento subsequente.

3. **Carregamento**:
   - Os dados transformados são carregados em um banco de dados SQL na Azure, onde são tratados e organizados em um modelo dimensional (fato e dimensão) usando Azure Synapse Analytics.

### 4.3 Visualização de Dados

A visualização dos dados será feita no Microsoft Power BI, permitindo a criação de dashboards interativos e relatórios que respondam às perguntas propostas pelo projeto.

## 5. Meta

O projeto visa criar uma aplicação que possibilite uma compreensão profunda dos dados do Pré-Sal, facilitando análises estratégicas e tomadas de decisão informadas.

---

Este README oferece uma visão geral clara do projeto, incluindo objetivos, metodologia e arquitetura. Ele é destinado a ajudar qualquer pessoa interessada a entender o escopo e as metas do projeto, e a contribuir para seu desenvolvimento.
