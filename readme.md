# Previsão de Preços de Imóveis: Regressão Avançada com o Dataset Ames

Este projeto foca na predição de preços de venda de imóveis utilizando o conjunto de dados Ames Housing, fornecido na competição "House Prices - Advanced Regression Techniques" do Kaggle. O objetivo principal é desenvolver e avaliar modelos de regressão para estimar os preços com base em múltiplas características dos imóveis.

## Etapas do Projeto

O desenvolvimento do projeto seguiu as seguintes etapas principais:

1.  **Carregamento e Análise Exploratória dos Dados (EDA)**:
    * Os conjuntos de dados de treino (`train.csv`) e teste (`test.csv`) foram carregados utilizando a biblioteca Pandas.
    * O arquivo `data_description.txt` foi consultado para entendimento das 79 variáveis explicativas que descrevem diversos aspectos das residências.
    * Foi realizada uma análise exploratória dos dados para visualizar distribuições, identificar valores ausentes, outliers e entender as correlações entre as variáveis e a variável alvo (`SalePrice`), utilizando bibliotecas como Matplotlib e Seaborn.

2.  **Pré-processamento e Engenharia de Features**:
    * Os valores ausentes identificados na etapa de EDA foram tratados utilizando estratégias de imputação apropriadas para cada tipo de variável (numérica ou categórica).
    * As variáveis categóricas foram transformadas em representações numéricas (ex: *one-hot encoding*, *label encoding*) para compatibilidade com os algoritmos de machine learning.
    * Potencialmente, foram criadas novas *features* a partir das existentes para tentar capturar informações adicionais e melhorar o desempenho do modelo (ex: combinação de `YearBuilt` e `YearRemodAdd` para representar a "idade efetiva" do imóvel).

3.  **Seleção, Treinamento e Avaliação de Modelos**:
    * Diferentes algoritmos de regressão foram considerados e treinados. O notebook `code.ipynb` indica o uso de Random Forest (`rf.predict`) e a importação de bibliotecas como TensorFlow e Yggdrasil Decision Forests (`ydf`), sugerindo a experimentação com modelos como *Gradient Boosted Trees* ou redes neurais.
    * O conjunto de treinamento (`train.csv`) foi utilizado para treinar os modelos. Estratégias como validação cruzada podem ter sido empregadas para ajuste de hiperparâmetros e para uma avaliação mais robusta da performance dos modelos.

4.  **Geração de Previsões e Submissão**:
    * As mesmas etapas de pré-processamento aplicadas aos dados de treino foram replicadas no conjunto de teste (`test.csv`).
    * O modelo final treinado foi utilizado para gerar as previsões de `SalePrice` para cada imóvel no conjunto de teste.
    * As previsões foram formatadas no arquivo `submission.csv`, contendo as colunas `Id` e `SalePrice`, conforme as especificações da competição Kaggle. A métrica de avaliação da competição é o Erro Quadrático Médio Logarítmico Raiz (RMSLE) entre o logaritmo do valor previsto e o logaritmo do valor de venda observado.

## Resultados

* O projeto resultou em um modelo preditivo capaz de estimar os preços de venda de imóveis com base nas características fornecidas.
* As previsões para o conjunto de teste estão consolidadas no arquivo `submission.csv`.
* O notebook `code.ipynb` contém todo o fluxo de trabalho, desde a importação dos dados até a geração das previsões finais, detalhando as análises e as etapas de modelagem.

## Tecnologias Utilizadas

* **Python**: Linguagem de programação principal.
* **Pandas**: Para manipulação e análise de dados.
* **NumPy**: Para operações numéricas.
* **Scikit-learn**: Para pré-processamento, implementação de modelos (como Random Forest) e métricas de avaliação.
* **Matplotlib & Seaborn**: Para visualização de dados.
* **TensorFlow & Yggdrasil Decision Forests (`ydf`)**: Bibliotecas para construção e treinamento de modelos avançados de machine learning.
* **Jupyter Notebook**: Para desenvolvimento interativo, documentação e apresentação do código.

## Possíveis Próximos Passos

* Investigar técnicas mais avançadas de engenharia de *features*.
* Realizar uma otimização de hiperparâmetros mais extensiva (ex: *Grid Search*, *Random Search*, Otimização Bayesiana).
* Experimentar com diferentes arquiteturas de redes neurais ou modelos de *ensemble* mais complexos.
* Analisar os erros do modelo para identificar padrões e áreas de melhoria.

---

## Citações

* **Competição Kaggle:**
    Anna Montoya and DataCanary. House Prices - Advanced Regression Techniques. [https://kaggle.com/competitions/house-prices-advanced-regression-techniques](https://kaggle.com/competitions/house-prices-advanced-regression-techniques), 2016. Kaggle.

* **Conjunto de Dados Ames Housing:**
    O conjunto de dados Ames Housing foi compilado por Dean De Cock para uso em educação em ciência de dados. É uma alternativa moderna e expandida ao frequentemente citado conjunto de dados Boston Housing.