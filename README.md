# Análise Exploratória de Dados de E-commerce

Este repositório contém um notebook Jupyter (`RID190878_Desafio07.ipynb`) que realiza uma análise exploratória de dados (EDA) em um conjunto de dados de transações de uma loja online.

## Objetivo

O objetivo principal deste projeto é explorar e entender os padrões presentes nos dados de vendas, como a distribuição geográfica dos clientes e a sazonalidade das transações, utilizando técnicas de visualização de dados.

## Dataset

O notebook utiliza um arquivo chamado `data.csv` (não incluído neste repositório, mas referenciado no código). Com base no código, espera-se que o dataset contenha as seguintes colunas:

*   `InvoiceNo`: Número da fatura (identificador único por transação).
*   `StockCode`: Código do produto.
*   `Description`: Descrição do produto.
*   `Quantity`: Quantidade de itens comprados na transação.
*   `InvoiceDate`: Data e hora da transação.
*   `UnitPrice`: Preço unitário do produto.
*   `CustomerID`: Identificador único do cliente.
*   `Country`: País onde a transação ocorreu.

## Tecnologias Utilizadas

*   **Python 3**: Linguagem de programação principal.
*   **Pandas**: Para manipulação e análise de dados.
*   **NumPy**: Para operações numéricas.
*   **Matplotlib**: Para criação de gráficos estáticos.
*   **Seaborn**: Para visualizações estatísticas mais elaboradas.
*   **Jupyter Notebook**: Ambiente interativo para execução do código.

## Como Usar

1.  **Clone o repositório:**
    ```bash
    git clone <URL_DO_REPOSITORIO>
    cd <NOME_DO_REPOSITORIO>
    ```
2.  **Prepare o ambiente:**
    Certifique-se de ter Python 3 instalado. Recomenda-se o uso de um ambiente virtual:
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows use `venv\Scripts\activate`
    ```
3.  **Instale as dependências:**
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
5.  **Execute o Notebook:**
    Inicie o Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
    Abra o arquivo `RID190878_Desafio07.ipynb` na interface do Jupyter e execute as células.

## Análise Realizada

O notebook realiza as seguintes etapas:

1.  **Carregamento dos Dados:** Leitura do arquivo `data.csv` para um DataFrame Pandas.
2.  **Análise Exploratória Inicial:**
    *   Visualização das primeiras linhas (`head()`).
    *   Verificação das informações do DataFrame (`info()`), incluindo tipos de dados e contagem de valores não nulos.
    *   Cálculo de estatísticas descritivas para colunas numéricas (`describe(include=[int, float])`).
    *   Cálculo de estatísticas descritivas para colunas de objeto (`describe(include=[object])`).
3.  **Visualizações:**
    *   Gráfico de barras mostrando o top 10 países com mais transações.
    *   Gráfico de barras mostrando a distribuição do número de transações por mês.

## Análise dos Resultados

A análise exploratória inicial revelou informações importantes sobre o conjunto de dados. As estatísticas descritivas indicaram a presença de valores negativos nas colunas Quantity e UnitPrice, o que pode sugerir transações de devolução ou possíveis erros nos dados que necessitam de investigação e tratamento adicionais. Além disso, foi observada uma quantidade significativa de valores ausentes na coluna CustomerID, impactando análises que dependem da identificação do cliente.

A visualização da distribuição geográfica das transações mostrou uma concentração massiva de vendas no Reino Unido (United Kingdom), que representa a vasta maioria das operações registradas no dataset. Outros países como Alemanha, França e EIRE (Irlanda) aparecem em seguida, mas com volumes consideravelmente menores.

Ao analisar a distribuição temporal das transações ao longo dos meses, percebe-se um aumento notável no volume de vendas nos últimos meses do ano, especialmente em novembro, seguido por outubro e dezembro. Isso sugere uma forte sazonalidade nas vendas, possivelmente associada às compras de fim de ano e feriados, um padrão comum no varejo.
