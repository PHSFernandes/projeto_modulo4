
# Análise exploratória de série histórica de combustíveis.

Esta análise faz parte do trabalho de conclusão de curso de formação em Análise de Dados da Resilia Educação com base nas informações disponibilizadas pela Agência Nacional de Petróleo e Gás
Natural e Biocombustíveis (ANP).


## Autores
- [Gabriel Lima](https://github.com/Gabriellimar)
- [Jean Rafael S. D. Spinola](https://github.com/jeansevenz)
- [Odilon Junior](https://github.com/Odilon-Jr)
- [Paulo H. S. Fernandes](https://github.com/PHSFernandes)
- [Roberto Dias](https://github.com/rddiasbk)

## 🔗 Links
Os datafames utilizados estão disponibilizados abaixo:
- [Série de combustíveis de Junho de 2021](https://www.gov.br/anp/pt-br/centrais-de-conteudo/dados-abertos/arquivos/shpc/dsan/2021/2021-07-gasolina-etanol.csv)
- [Série de combustíveis de Julho de 2021](https://www.gov.br/anp/pt-br/centrais-de-conteudo/dados-abertos/arquivos/shpc/dsan/2021/2021-06-gasolina-etanol.csv)

## Sobre a análise: 

A análise foi criada a apartir de 10 perguntas propostas que foram divididas entre os membros do grupo:
>     1) Como se comportaram o preço dos combustíveis durante os dois meses citados? Os valores do etanol e da gasolina tiveram uma tendência de queda ou diminuição?
>     2) Qual o preço médio da gasolina e do etanol nesses dois meses?
>     3) Quais os 5 estados com o preço médio da gasolina e do etanol mais caros?
>     4) Qual o preço médio da gasolina e do etanol por estado?
>     5) Qual o município que possui o menor preço para a gasolina e para o etanol?
>     6) Qual o município que possui o maior preço para a gasolina e para o etanol?
>     7) Qual a região que possui o maior valor médio da gasolina?
>     8) Qual a região que possui o menor valor médio do etanol?
>     9) Há alguma correlação entre o valor do combustível (gasolina e etanol) e a região onde ele é vendido?
>     10) Há alguma correlação entre o valor do combustível (gasolina e etanol) e a bandeira que vende ele?


## Resultados
**Questão 01** -  Consulta aferida a partir do valor médio dos combustíveis que apresentaram os seguintes dados:
 ### Mês de Junho - 2021
>     ETANOL                4.576389
>     GASOLINA              5.671506
>     GASOLINA ADITIVADA    5.819346

### Mês de Julho - 2021
>     ETANOL                4.576389
>     GASOLINA              5.671506
>     GASOLINA ADITIVADA    5.819346

Utilizou-se um gráfico (abaixo) do tipo `plt.scatter` para melhor visualizar o **aumento** dos combustíveis nos meses pesquisados. 
![Gráfico 1](data:image/png;base64,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)

**Questão 02** - Filtrou-se o campo gasolina e etanol e gasolina e em seguida utilizou-se a função `mean()` para encontrar o valor médio.
 ### Gasolina

>     Junho - R$ 5.67
>     Julho - R$ 5.80
- Variação de R$ 0,13 centavos.

### Etanol
>     Junho - R$ 4.57 
>     Julho - R$ 4.58

- Variação de R$ 0,01 centavos para o Etanol.

**Questão 03** - Foi necessário filtrar gasolina e etanol e agrupar por preço e unidade administrativa, além de organizá-los por valor e concatenar resultados.
Assim conclui-se que os cinco estados com o preço médio de gasolina e etanol mais caros são:

>     - Etanol:
>     1. Rio Grande do Sul
>     2. Acre
>     3. Rio Grande do Norte
>     4. Pará
>     5. Amapá.

>     - Gasolina
>     1. Acre
>     2. Rio de Janeiro
>     3. Rio Grande do Norte
>     4. Piauí
>     5. Goiás

**Questão 04** - Após agrupamento, nota-se que o **Acre** possui a maior média de preço para **Gasolina**, no valor de **6,44** e o estado **Rio Grande do Sul**, possui a maior média para **Etanol** no valor de **R$ 5,81**


**Questão 05** - Entre os meses analisados o município de **Adamantina - SP** apresentou os menores valores de combustíveis: **R$ 4,19** e **R$ 3,09** respectivamente Gasolina e Etanol.

**Questão 06** - O município de **Xanxere - SC** apresentou os maiores valores de combustíveis:  **R$ 6,99** e **R$ 7,09**, respectivamente Etanol e Gasolina.

**Questão 07** - A região Centro-Oeste apresentou o maior valor para Gasolina.

**Questão 08** - A região Sudeste apresentou o valor médio de combustíveis. Especula-se que o maior número de refinarias na região influencie na queda dos preços.

**Questão 09** - A região SE é a que apresenta o menor valor médio dos combustíveis (Álcool e Gasolina), enquanto a região N é a que apresenta o maior. O desvio padrão calculado para a s regiões revela que a região CO, seguida da região SE são as que apresentam maior desvio.

**Questão 10** - Correlacionando os dados, inclusive com apoio do Excel, foi possível observar que a Bandeira influencia no valor do combustível.

**Questão Extra N° 01:** QUAL O DESVIO PADRÃO DO ETANOL POR ESTADO?
Resposta: O Desvio Padrão para o Preço do ETANOL por Estado revela que o Maranhão possui a menor variação de preço, enquanto o Rio de Janeiro possui a maior variação.

**Questão Extra N°2:**  QUAL O DESVIO PADRÃO DA GASOLINA E DO ETANOL POR REGIÃO?
O Cálculo do Desvio Padrão da GASOLINA por região revela que a região que apresenta o maior valor de Desvio Padrão para a GASOLINA COMUM é a região Norte, seguida das regiões SE, S, NE e CO, respectivamente. Para a GASOLINA ADITIVADA, o maior valor de Desvio Padrão fica para o SE, seguido do N, S, NE e CO, respectivamente.
Exibindo o resultado somente para o produto ETANOL por região, indicando que a região Nordeste tem o maior preço médio de Etanol do Brasil.
O Desvio Padrão para o Preço do ETANOL por região revela que a região Sul Possui a maior variação. A região Nordeste, que possui a maior Média, possui o menor Desvio padrão.
Esses resultados apresentam uma situação mais complicada para a região Nordeste. Além de ter preço médio maior, existe uma menor variação nos preços o que revela que o consumidores possuem menos chances de encontrar preços significativamente abaixo da méd
## Referência

 - [Sugar and ethanol mills in Brazil – SHP](https://gismaps.com.br/en/downloads/usinas-de-acucar-e-alcool-no-brasil-shp/)
 - [Análise de Conjuntura dos Biocombustíveis – Ano 2020](https://www.epe.gov.br/pt/publicacoes-dados-abertos/publicacoes/analise-de-conjuntura-dos-biocombustiveis-2020)
