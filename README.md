# 🚧 Análise de Padrões em Acidentes Rodoviários no Brasil - 2024

O objetivo deste projeto é explorar os fatores e identificar padrões em acidentes rodoviários ocorridos no Brasil em 2024. Para isso, o trabalho engloba a limpeza e o tratamento dos dados, seguido pela aplicação do algoritmo Apriori para a descoberta de regras de associação relevantes.


## 🗂️ Origem dos Dados

Os dados utilizados neste projeto são provenientes do portal de Dados Abertos da Polícia Rodoviária Federal (PRF), disponibilizados pelo Governo Federal [Fonte Oficial](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf). Para a análise, foi selecionado o arquivo Documento CSV de Acidentes 2024 (Agrupados por pessoa - Todas as causas e tipos de acidentes) `acidentes2024_todas_causas_tipos.csv`.

## 📜 Sobre o Projeto

O núcleo do projeto consiste em transformar cada registro de acidente em um formato transacional, onde cada transação representa o conjunto de características de um evento (ex: estado, tipo de pista, condição do tempo). A partir disso, foi aplicado o algoritmo Apriori para extrair itemsets frequentes e, subsequentemente, gerar regras de associação com métricas de suporte, confiança e lift.

Foi conduzida inicialmente uma análise exploratória dos dados para compreender as principais variáveis e tendências. Em seguida, o algoritmo foi aplicado com um suporte mínimo de 1% para identificar os padrões mais relevantes sobre os fatores que ocorrem em conjunto nos acidentes rodoviários.

## 🎯 Objetivos

- Realizar uma Análise Exploratória de Dados (EDA) para compreender as principais características dos acidentes (causas, locais, horários).
- Aplicar o algoritmo Apriori para gerar regras de associação entre os diferentes fatores dos acidentes (ex: tipo de pista, condição do tempo, UF).
 - Avaliar as regras geradas com base em métricas como suporte, confiança e lift.
 - Identificar padrões que indiquem os principais fatores de risco ou as condições mais recorrentes nos acidentes.


## 📋 Etapas do Projeto

O projeto foi desenvolvido em dois Jupyter Notebooks, cada um focado em uma fase distinta do processo.

#### **Notebook: `01_exploracao_dados_acidentes.ipynb`**

1.  **Carregamento e Preparação dos Dados:**  Leitura do arquivo `acidentes2024_todas_causas_tipos.csv`, seguida pela limpeza da base, tratamento de valores ausentes, remoção de colunas e conversão de tipos de dados.
2.  **Análise Exploratória de Dados (EDA):** Investigação das principais características dos acidentes, como distribuição por UF, tipo de pista, causas, condições meteorológicas e período do dia.

#### **Notebook: `02_regras_associacao.ipynb`**

3.  **Pré-processamento para Apriori:**
    * Transformação dos dados em um formato transacional, onde cada acidente se torna um conjunto de itens representando suas características (ex: `uf_MG`, `pista_Simples`). 
       
   4.  **Aplicação do Algoritmo Apriori:** Execução do algoritmo com um suporte mínimo de 1% para encontrar os itemsets (conjuntos de fatores) que ocorrem com mais frequência.
   5.  **Geração e Análise das Regras:** Criação de regras de associação a partir dos *itemsets* frequentes e análise das métricas (suporte, confiança e lift) para identificar as correlações mais relevantes entre os fatores dos acidentes.

## 🛠️ Tecnologias Utilizadas

- Python 3.13.5
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 📊 Análises Realizadas

- Distribuição de acidentes por mês
- Distribuição de acidentes por dia da semana
- Comparativo por estados (UF)
- Acidentes por tipo de pista
- Relação entre atributos importantes (ex: tipo de pista vs estado)
- Tratamento e visualização de dados faltantes

## 🔍 Resultados e Visualizações

Este projeto apresenta os resultados da análise exploratória e da mineração de dados sobre os acidentes rodoviários de 2024. Através de gráficos, tabelas e regras de associação, o estudo revela padrões e tendências significativas, aprofundando a compreensão sobre os fatores de risco e fornecendo uma base sólida para possíveis tomadas de decisão.


---

👤 Autor

- Priscila Borges 


