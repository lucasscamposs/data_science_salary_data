# Projeto de Ciência de Dados - Experiência e Salário dos Funcionários
![Capa](https://github.com/user-attachments/assets/d581e5e0-3ee7-44fc-bfae-c31dbbb087b1)

## Introdução
O dataset que vou explorar trata-se de dados fictícios do tempo de experiência dos funcionários e do salário que eles recebem.

O objetivo da análise consiste em responder a seguinte pergunta: "Se uma empresa fosse contratar esses funcionários, o tempo de experiência que eles possuem fariam com que a empresa tivesse que pagar um salário maior por esses funcionários?"

Para responder a essa pergunta, analisei os dados para identificar se há uma correlação significativa entre os anos de experiência e o salário. Se for encontrada uma relação positiva, isso indicaria que mais anos de experiência resultam em salários mais altos. Por outro lado, se não houver correlação, o tempo de experiência não seria um fator determinante para o salário.

Primeiro, eu importei as bibliotecas necessárias para a modelagem e manipulação de dados, incluindo numpy e pandas. Em seguida, importei bibliotecas para análise gráfica, como matplotlib.pyplot e seaborn, e desabilitei avisos desnecessários utilizando a biblioteca warnings.

Depois, mudei o diretório de trabalho para a pasta onde está localizada a base de dados usando os.chdir. Li a base de dados Salary_Data.csv com pd.read_csv e verifiquei as primeiras linhas do dataframe para confirmar a leitura correta dos dados.

Renomeei as colunas do dataframe para facilitar a manipulação futura: "YearsExperience" foi renomeado para "Xp" e "Salary" foi renomeado para "Renda". Também verifiquei a dimensão do dataframe com Base_Dados.shape, que retornou um dataframe com 30 linhas e 2 colunas.

Chequei se havia campos nulos na base de dados com Base_Dados.isnull().sum(), o que confirmou a ausência de valores nulos. Para visualizar isso de forma gráfica, usei sns.heatmap para gerar um mapa de calor.

Finalmente, usei Base_Dados.describe() para gerar estatísticas descritivas das colunas "Xp" e "Renda", obtendo informações como média, desvio padrão, valores mínimos e máximos, e percentis.

Todo o passo a passo dos códigos do projeto está demostrado no arquivo `data_science_salary_data.ipynb`, abaixo vou deixar uma apresentação desse passo passo e mostrar o resultado da análise.

## Dataset
O dataset utilizado foi retirado do Kaggle e está disponível [aqui](https://www.kaggle.com/datasets/karthickveerakumar/salary-data-simple-linear-regression/data). Ele inclui duas colunas principais:
- **YearsExperience**: Anos de experiência dos funcionários.
- **Salary**: Salário dos funcionários.

## Bibliotecas Utilizadas
- **os**: Para a leitura dos dados.
- **numpy**: Para operações numéricas.
- **pandas**: Para manipulação de dados.
- **matplotlib.pyplot**: Para criação de gráficos.
- **seaborn**: Para visualização de dados estatísticos.
- **warnings**:Para gerenciar avisos e manter o ambiente de trabalho limpo.

## Carregamento e Preparação dos Dados
- **Carregamento dos Dados**: O dataset foi carregado utilizando "os" e verificado.
- **Renomeação das Colunas**: As colunas foram renomeadas para `Xp` (Experiência) e `Renda` (Salário).
- **Verificação de Nulos**: Foi verificado se existiam valores nulos no dataset.

# Análise Exploratória de Dados (EDA)
Primeiro foi feito uma verificação da quantidade de linhas e colunas do dataframe e em seguida uma análise descritiva breve para darmos início a visualizações gráficas.
## Visualizações Gráficas
**Distribuição do Salário**: Utilização de KDE plot para analisar a distribuição dos salários.
  - ![kdeRenda](https://github.com/user-attachments/assets/2e9a6419-04d3-4dd2-a6f9-6fbd6c5f7f55)

**Distribuição da Experiência**: Utilização de KDE plot para analisar a distribuição dos anos de experiência.
  - ![kdeXp](https://github.com/user-attachments/assets/a7ac75f3-ed04-4c4e-90be-b65e320fdb2f)

  - **Boxplots**: Boxplots para identificar outliers tanto na variável `Renda` quanto na `Xp`.
  - **Scatter Plot**: Gráfico de dispersão para visualizar a relação entre `Renda` e `Xp`.
  - ![dispersão](https://github.com/user-attachments/assets/fd783709-ccb9-40d4-8869-6e7c5c4312c5)

  - **Regressão Linear**: Adição de uma linha de regressão ao scatter plot para melhor visualizar a tendência.
  -   - ![sns-xp](https://github.com/user-attachments/assets/3858bfdd-6dbb-403b-9ddc-f97ee6a67910)


## Análise de Correlação
- **Correlação de Pearson**: Cálculo da correlação de Pearson entre `Xp` e `Renda` e visualização através de um heatmap.
![pearson](https://github.com/user-attachments/assets/53fcc0e7-e0f0-4d2d-a83b-e6e02da3fe9c)

- **Correlação de Spearman**: Cálculo da correlação de Spearman entre `Xp` e `Renda` e visualização através de um heatmap.
![spearman](https://github.com/user-attachments/assets/df84cdad-4f80-4d87-9987-7f40e949a7b5)

## Conclusão
A análise realizada no dataset sugere que há uma relação entre o tempo de experiência dos funcionários e o salário que eles recebem. Tanto os gráficos de dispersão com linha de regressão quanto os cálculos de correlação indicam uma tendência de aumento de salário com o aumento dos anos de experiência.
