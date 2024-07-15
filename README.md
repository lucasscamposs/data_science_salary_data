# Projeto de Ciência de Dados - Experiência e Salário dos Funcionários

![sns-xp](https://github.com/user-attachments/assets/3858bfdd-6dbb-403b-9ddc-f97ee6a67910)



## Pergunta Principal
Se uma empresa fosse contratar esses funcionários, o tempo de experiência que eles possuem faria com que a empresa tivesse que pagar um salário maior por esses funcionários?

## 1. Introdução
Este projeto tem como objetivo analisar se existe uma relação significativa entre o tempo de experiência dos funcionários e o salário que eles recebem. Utilizamos um dataset fictício que contém informações sobre anos de experiência e salários.

## 2. Dataset
O dataset utilizado foi retirado do Kaggle e está disponível [aqui](https://www.kaggle.com/datasets/karthickveerakumar/salary-data-simple-linear-regression/data). Ele inclui duas colunas principais:
- **YearsExperience**: Anos de experiência dos funcionários.
- **Salary**: Salário dos funcionários.

## 3. Bibliotecas Utilizadas
- numpy
- pandas
- matplotlib.pyplot
- seaborn
- warnings

## 4. Carregamento e Preparação dos Dados
- **Carregamento dos Dados**: O dataset foi carregado e verificado.
- **Renomeação das Colunas**: As colunas foram renomeadas para `Xp` (Experiência) e `Renda` (Salário).
- **Verificação de Nulos**: Foi verificado se existiam valores nulos no dataset.

## 5. Análise Exploratória de Dados (EDA)
- **Dimensões do Dataset**: Verificação da quantidade de linhas e colunas.
- **Análise Descritiva**: Estatísticas descritivas básicas do dataset.
- **Visualizações Gráficas**:
  - **Distribuição do Salário**: Utilização de KDE plot para analisar a distribuição dos salários.
  - **Distribuição da Experiência**: Utilização de KDE plot para analisar a distribuição dos anos de experiência.
  - **Boxplots**: Boxplots para identificar outliers tanto na variável `Renda` quanto na `Xp`.
  - **Scatter Plot**: Gráfico de dispersão para visualizar a relação entre `Renda` e `Xp`.
  - **Regressão Linear**: Adição de uma linha de regressão ao scatter plot para melhor visualizar a tendência.

## 6. Análise de Correlação
- **Correlação de Pearson**: Cálculo da correlação de Pearson entre `Xp` e `Renda` e visualização através de um heatmap.
- **Correlação de Spearman**: Cálculo da correlação de Spearman entre `Xp` e `Renda` e visualização através de um heatmap.

## 7. Conclusão
A análise realizada no dataset sugere que há uma relação entre o tempo de experiência dos funcionários e o salário que eles recebem. Tanto os gráficos de dispersão com linha de regressão quanto os cálculos de correlação indicam uma tendência de aumento de salário com o aumento dos anos de experiência.
