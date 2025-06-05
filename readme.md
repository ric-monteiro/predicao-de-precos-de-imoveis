# Previsão de Preços de Imóveis: Regressão com o Dataset Ames

Este projeto foca na predição de preços de venda de imóveis utilizando o conjunto de dados Ames Housing, fornecido na competição "House Prices - Advanced Regression Techniques" do Kaggle. A ideia principal foi explorar diferentes técnicas de regressão para construir um modelo que estimasse bem os preços dos imóveis.

## Etapas do Projeto

O processo foi dividido em quatro grandes partes:

1.  **Carregamento e Análise Exploratória dos Dados (EDA)**:
    * Os conjuntos de dados de treino (`train.csv`) e teste (`test.csv`) foram carregados com Pandas.
    * O arquivo `data_description.txt` foi consultado para entender as 79 variáveis explicativas.
    * Visualizações com Matplotlib e Seaborn ajudaram a entender distribuições, valores ausentes, outliers e correlações com o preço de venda (SalePrice).

2.  **Pré-processamento e Engenharia de Features**:
    * Valores ausentes foram tratados com estratégias específicas para cada tipo de dado.
    * Variáveis categóricas foram transformadas em valores numéricos usando técnicas como one-hot encoding e label encoding.
    * Algumas novas *features* também foram criadas para melhorar o modelo, como uma variável que combina o ano de construção com o ano de reforma para representar a "idade real" da casa.

3.  **Seleção, Treinamento e Avaliação de Modelos**:
    * Como modelo de regressão, foi usado o Random Forest e as bibliotecas TensorFow e Yggdrasil Decision Forests.
    * O conjunto de treinamento (`train.csv`) foi utilizado para treinar os modelos. Técnicas como validação cruzada ajudaram a avaliar o desempenho dos modelos e ajustar hiperparâmetros.

4.  **Geração de Previsões e Submissão**:
    * O mesmo pré-processamento foi aplicado aos dados de teste.
    * O modelo final gerou as previsões de preço `SalePrice`, que foram salvas no arquivo
    * A métrica usada para avaliação foi o RMSLE (Erro Quadrático Médio Logarítmico Raiz), conforme as regras da competição.

## Resultados

* O modelo treinado conseguiu prever os preços com uma boa margem de acerto, levando em conta as variáveis disponíveis. Alcançando o score de 0.14857 na competição do Kaggle.
* As previsões foram consolidadas no `submission.csv`.
* O notebook `code.ipynb` contém todo o fluxo de trabalho, desde a importação dos dados até a geração das previsões finais.

## Tecnologias Utilizadas

* **Python**: Linguagem de programação principal.
* **Pandas**: Para manipulação e análise de dados.
* **NumPy**: Para operações numéricas.
* **Scikit-learn**: Para pré-processamento, implementação de modelos (como Random Forest) e métricas de avaliação.
* **Matplotlib & Seaborn**: Para visualização de dados.
* **TensorFlow & Yggdrasil Decision Forests (`ydf`)**: Bibliotecas para construção e treinamento de modelos avançados de machine learning.

## Possíveis Próximos Passos

* Testar abordagens mais criativas de criação de *features*.
* Otimizar melhor os hiperparâmetros com técnicas como Grid Search, Random Search ou até Otimização Bayesiana.
* Explorar modelos de ensemble mais sofisticados.
* Analisar os erros do modelo para entender onde ele pode melhorar.

---

## Citações

* **Competição Kaggle:**
    Anna Montoya and DataCanary. House Prices - Advanced Regression Techniques. [https://kaggle.com/competitions/house-prices-advanced-regression-techniques](https://kaggle.com/competitions/house-prices-advanced-regression-techniques), 2016. Kaggle.

* **Conjunto de Dados Ames Housing:**
    O conjunto de dados Ames Housing foi compilado por Dean De Cock para uso em educação em ciência de dados. É uma alternativa moderna e expandida ao frequentemente usado conjunto de dados Boston Housing.
