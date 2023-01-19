<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

## Descrição do Problema
Uma das dificuldades nos processos seletivos são as situações em que o o candidato é obrigado a mostrar competencia em um intervalo de tempo relativamente pequeno, esse processo se da por uma ou mais entrevistas, provas teoricas, praticas, dinâmicas de analises comportamentais, etc. Outro problema é que Cientistas de Dados jr muitas vezes sequer chegam na etapa de entrevistas, seus os portifolios de projetos sequer são vistos, o que desanima um pouco já que muitos dos projetos demoram meses para serem desenvolvidos. 

Este projeto tem como objetivo simular o processo seletivo / inserção de um cientista de dados jr em um grande Banco Nacional. Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: detecção de fraude, segmentação de clientes, previsão de inadinplência, predição de churn, analises em tempo real, automação de processos de comunicação, etc. 

Para isso, o Banco forneceu algumas opções de datasets para candidado escolher( referentes as principais áreas de atuação do Cientista de Dados como as citadas anteriormente), a partir dessa escolha o candidato deverá apresentar um projeto num prazo máximo de sete dias exibindo de acordo com os objetivos propostos a baixo.

<i>Nota: A premissa de que poderia ser um projeto de um processo seletivo Cientista de Dados Jr de um Banco, é uma percepção minha, não necessáriamente significa que os processos seletivos atuais seguem esse molde.</i><br><br>


## Objetivo
**Principal:**
* O candidato deve desenvolver uma solução dentre o escopo de atuação do cientista de dados para o Estudo de Caso escolhido.
* Apresentar os resultados obtidos de maneira simples. 
<br><br>

<i>Nota: O candidato será avaliado, principalmente pelo conhecimento de negócio, dominio das ferramentas de desenvolvimento Python/R, dominio das abordagens estatisticas e domínio em Machine Learning.</i>


**Secundário:**

* Apresentar um possivel plano de ação do Banco com base os resultados obtidos<br><br>

## Estudo de Caso

**Cluster Segmentation** - A segmentação de clientes é uma técnica de ciência de dados que envolve a análise de dados de clientes para dividi-los em grupos distintos que compartilham características semelhantes. Esses grupos, ou segmentos, são usados ​​para identificar oportunidades potenciais de marketing, desenvolvimento de produtos e atendimento ao cliente. Ao entender as características únicas de cada segmento, as empresas podem direcionar melhor seus produtos e serviços para atender às necessidades de clientes individuais.

**Base de Dados** - A base de dados contém os dados referentes ao uso do cartão de crédito de 8950 clientes de uma determinada agencia, coletados num periodo de seis meses. A base de dados está disponivel no [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)<br><br>


## Estágios de Desenvolvimento
[**Pré Processamento dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part01_preprocessing.ipynb)<br>
Lidando com valores ausentes com o KNN Imputer...

[**Analise Exploratória dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part02_eda.ipynb)<br>
Analise Univariada, Analise Bivariada, Analise Multivariada.

[**Preparação dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
Detecção de Outlier com Isolation Forest, Normalização, Padronização, Redução de Dimensionalidade (PCA, UMAP, t-SNE).

[**Modelo de Machine Learning**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
 Kmeans, Hierachical Clustering, Gaussian Mixture Model<br><br>


## Relatórios
[**Apresentação**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/resultados.md)<br>
[**Q & A - Operações com o Cartão de Crédito**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/qa.md)<br><br>


## Ferramentas
Linguagens: Python<br>
IDE: Visual Studio Code, Jupyter Notebook<br>
Bibliotecas: Pandas, Matplotlib, Seaborn, Plotly, Sklearn, scipy, yellowbricks<br>
Metodologia: CRISP-DM<br>

**

# Resultados

Após o desenvolvimento do modelo de clusterização chegamos, numa solução otimizada para sete agrupamentos de clientes e um possivel plano de ação de acordo com as principais caracteristicas apontadas. A estratégia basica do plano de ação é explorar as modalidades de compra que o cliente estão habituados a usar, oferencendo-os vantagens.

<center><img src="/images/pie.png" alt="pie" width="512" height="411"/></center>

<blockquote style="color: #000000;">

**Cluster 00 - Consumidores de baixa frequencia que compram quase sempre a vista**

Clientes: 1086, 12.13%<br>
Compras: $912.743.45<br>
Frequencia média de compras: 0.35<br>
Qtd média de compras: 7.40 +/- 11.47<br>
Lucro: $316.071,25<br>
Limite de Crédito Médio: $4411.29<br>
Qtd de clientes que excederam o limite de crédito: 50


<u>Plano de Ação:</u> é oferecer descontos especiais ou recompensas por usá-lo mais. Por exemplo, o banco pode oferecer descontos em compras feitas no cartão ou recompensas em forma de pontos ou milhas que podem ser trocadas por produtos ou serviços. O banco também pode oferecer incentivos para usar o cartão em certas lojas ou em certos tipos de compras, como compras online ou em estabelecimentos específicos. Além disso, o banco pode promover promoções e oferecer prêmios aos clientes que usam o cartão de crédito à vista com mais frequência.

***

**Cluster 01 - Consumidores de baixa frequencia que compram quase sempre com adiantamento em dinheiro** 

Clientes: 2053.00, 22.94%<br>
Compras: $59.02<br>
Frequencia média de compras: 0.00<br>
Qtd média de compras: 0.01 +/-	0.10<br>
Lucro: $33.381.864,14 <i>A base de dados não possuí dados referentes ao pagamento do adiantamento</i><br>
Limite de Crédito Médio: $4020.97 +/- 3249.02<br>
Qtd de clientes que excederam o limite de crédito: 50


<u>Plano de Ação:</u> 


***

**Cluster 02 - Consumidores de alta frequencia que quase sempre compram parcelados** 

Clientes: 1812, 20.25%<br>
Compras: $950.576,47<br>
Frequencia média de compras: 0.70<br>
Qtd média de compras: 11.68	+/- 11.33<br>
Lucro: $385.453,49<br>
Limite de Crédito Médio: $3114.81 +/- 2692.72<br>
Qtd de clientes que excederam o limite de crédito: 57


<u>Plano de Ação:</u> Uma campanha de marketing que um banco poderia adotar para incentivar clientes a usarem ainda mais o cartão de crédito parcelado é oferecer descontos especiais para compras realizadas com o cartão. Além disso, o banco poderia oferecer programas de fidelidade que oferecem pontos para cada compra realizada com o cartão, que podem ser trocados por recompensas. Outra opção é oferecer parcelamentos especiais para compras realizadas com o cartão, com taxas de juros mais baixas ou prazos de pagamento mais longos. Finalmente, o banco poderia oferecer ainda mais benefícios para aqueles que usam o cartão frequentemente, como descontos em produtos específicos ou serviços adicionais.


***

**Cluster 03 - Consumidores de alta frequencia que operam em todas modalidades** 

Clientes: 961, 10.74%<br>
Compras: $1,631.380,69<br>  
Frequencia média de compras: 0.78<br>
Qtd média de compras: 28.37	+/- 25.48<br>
Lucro: $814.026.84<br>
Limite de Crédito Médio: $5589.61 +/- 3908.91<br>
Qtd de clientes que excederam o limite de crédito: 69

<u>Plano de Ação:</u> Uma campanha de marketing para clientes que costumam comprar em varias modalidades pode começar com um programa de fidelidade. Isso pode incluir oferecer um desconto especial para cada compra, a chance de acumular pontos e trocá-los por recompensas, além de oferecer ofertas exclusivas para os clientes mais fiéis. Além disso, você também pode considerar a criação de cupons de desconto para incentivar os clientes a comprar mais. O envio de e-mails com promoções especiais para clientes com histórico de compras anteriores também pode ser útil. Por fim, você também pode considerar a criação de uma comunidade online para seus clientes, permitindo que eles compartilhem suas experiências de compra e discutam promoções.


***

**Cluster 04 - Consumidores com histórico ruim de pagamento** 

Clientes: 1697, 18.96%<br>
Compras: $3.572.670,52<br>
Frequencia média de compras: 0.81<br>
Qtd média de compras: 32.41 +/- 31.07<br>
Lucro: -$276.002,85<br>
Limite de Crédito Médio: $5539.68 +/- 3774.96<br>
Qtd de clientes que excederam o limite de crédito: 203


Plano de Ação: Uma campanha de marketing que o Banco poderia adotar para clientes que possuem com histórico ruim de pagamentos e que possuem dívidas no cartão de crédito seria oferecer um plano de pagamento flexível. O plano de pagamento flexível permitiria que os clientes parcelassem as dívidas em um prazo maior, com juros menores. Além disso, o banco também poderia oferecer bônus como descontos, cashback e outros incentivos para que os clientes possam quitar suas dívidas mais rapidamente.

    
***

**Cluster 05 - Consumidores de alta frequencia que quase sempre compram parcelados, eventualmente com adiantamento em dinheiro** 

Clientes: 458, 5.12%<br>
Compras: $230.613,74
Frequencia média de compras: 0.65<br>
Qtd média de compras: 11.58	+/- 11.64<br>
Lucro: $642.650,66<br>
Limite de Crédito Médio: $4298.91 +/- 3516.92<br>
Qtd de clientes que excederam o limite de crédito: 8


<u>Plano de Ação:</u> São clientes que não utilizam tanto o cartão de crédito mas quando utilizam estão dispostos a gastar mais, principalmente para compras parceladas, o saldo do cartão de crédito destes clientes estam sempre alto. São tendem a pagar mais do que os clientes do cluster 2


***

**Cluster 05 - Consumidores de baixa frequencia que quase sempre compram a vista, eventualmente com adiantamento em dinheiro** 

Clientes: 793,	8.86%<br>
Compras: $470.009,02
Frequencia média de compras: 0.28<br>
Qtd média de compras: 6.23 +/- 13.33<br>
Lucro: $927.983,38<br>
Limite de Crédito Médio: $4584.27 +/- 3462.71<br>
Qtd de clientes que excederam o limite de crédito: 14


<u>Plano de Ação:</u> São o pefil de cliente que usam pouco o cartão, usam para compras a de maior valor e quase sempre compram a vista. Um possivel plano de ação é aumentar o limite do cartão desses clientes a comprarem produtos mais caros.
    
</blockquote>    

## Viabilidade do Projeto

Os projetos de clusterização para segmentação de clientes costumam apresentar bons resultados mesmo em modelos mais simples em que apenas um cientista de dados consegue desenvolve-lo em um intervalo de tempo baixo. Como não temos uma base comparativa ( estamos considerando que hipoteticamente o Banco não possuí nenhum projeto com essa caracteristica), o projeto apresenta uma boa solução pois consegue dividir bem, grupos distintos de clientes, que necessitam de tratamentos diferentes. 

<center><img src="/images/priorization_matrix.png" alt="viability" width="900" height="720"/></center>

## Referencias
https://www.forbes.com/advisor/credit-cards/what-is-a-cash-advance-and-should-you-get-one/