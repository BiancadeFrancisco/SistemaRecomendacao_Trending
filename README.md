# SistemaRecomendacao_Trending

## Descrição Projeto

**Conjunto de dados:**
O dataset a ser utilizado será o [MovieLens](https://grouplens.org/datasets/movielens/). Com os dados distribuídos da sequinte forma:

- `item id`: identificador do filme
- `title`: título do filme
- `genres`: lista com os gêneros associados ao filme
- `year`: ano em que o filme teve sua estreia

Além do dataset de filmes, também será utilizado um dataset com as avaliações desses filmes, com os dados distribuídos através das colunas:

- `user id`: identificador do usuário
- `item id`: identificador do filme
- `rating`: avaliação do filme
- `timestamp`: tempo que foi realizada a avaliação
- `date`: data da avaliação

**Arquivo:** .parquet

**Objetivo:**
Realizar uma análise exploratório em um dataset com dados informativos sobre filmes, com o objetivo de apresentar itens que tiveram maiores lifts de consumo em uma determinada janela de tempo, podendo ser chamado de recomendação trending.

Obs: Trending são considerados itens que estão em ascensão. Janela de tempo é o período de tempo considerado para contabilizar aumento ou diminuição do consumo

Lift = ( consumoJanelaAtual – consumoJanelaAnterior ) / consumoJanelaAnterior
Nesse código utilizou-se como janela de tempo, o mês de consumo do item. 

**IDE:** Colab

**Linguagem:** Python 

**Principais bibliotecas utilizadas:**
•	Cycler, para personalizar cores em gráficos;
•	Pandas, para manipulação e tratamento dos dados;
•	Matplotlib, para criação e visualização de gráficos;
•	Google.colab, para importar arquivos da núvem;
•	Datetime, para manipulação de dados no formato de data.

**Sequencia processos:**
1° Instalação bibliotecas; 

2° Pré processamento datasets;

3° Definir a janela que será utilizado:
- Nesse código, utilizou-se como janela o ano e o mês da avaliação dos usuários.

4° Avaliar o consumo por janela temporal:
- Avaliou-se o quanto teve de consumo para cada item, comparando na janela atual com a anterior, verificando se houve aumento ou diminuição no consumo. 

5° Realizado cálculo do lift;

6° Especificado a janela de recomendação que será utilizado como referência;

7° Recomendação dos itens com maior ascensão;

8° Recomendação de uma seleção de acervo.

**Resultado:**
Através da sequência de processos realizadas, foi possível gerar um acervo de recomendações de filmes através de itens considerados trending.
