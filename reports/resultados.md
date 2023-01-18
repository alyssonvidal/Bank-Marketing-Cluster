
# Report

Essa parte será apresentado os resultados do projeto de forma resumida.

<br><br>

## Justifique a escolha do Estudo de Caso para Costumer Segmentation?

No problema de Customer Segmentation, através de algoritimos de clusterização, somos capazes de produzir insights sobre como dados similares estão relacionados e agrupados e nos ajuda também entender nosso problema de negócio, desde os conceitos mais simples até a identificação de padrões mais ocultos. Os algoritmos de clusterização também podem ajudar a reduzir o tamanho de um conjunto de dados e permitir que os dados sejam analisados mais facilmente.

Considerando a segunda parte do projeto, "viabilidade", os projetos de Costumer Segmentation são um otimo ponto de partida dentre o escopo de atuação do Cientista de Dados. Para uma empresa que não tem nenhuma ou pouca estrutura nesse aspecto, os algoritimos de clusterização costumam produzir bons resultados mesmo nos algoritimos mais simples. 

<br>

***

<br>

## Explique o principio de funcionamento do algortimo escolhido.

O **Modelo de Mistura Gaussiana (GMM)** é um modelo de agrupamento probabilístico que assume que cada ponto de dados é gerado por uma mistura de um número finito de distribuições Gaussianas com parâmetros desconhecidos. Esses parâmetros incluem os limites de cada distribuição Gaussiana, bem como os pesos que determinam a proporção de cada distribuição na mistura. Os GMMs são comumente usados ​​para aplicações de cluster, pois podem modelar clusters que não são necessariamente redondos ou elípticos, dessa forma ele pode ser considerado uma extrapolação de outro modelo conhecido, o KMeans.

<br>

***

<br>

## Explique o principio de funcionamento de pelo menos uma das métricas escolhidas.

O **Silhouette Score** é uma métrica usada para medir o quão próximo cada ponto em um cluster está dos pontos em outros clusters. Pode variar de -1 (indicando que o ponto está muito distante de outros clusters) a 1 (indicando que o ponto está muito próximo de outros clusters). É calculado tomando a média do coeficiente de silhueta para cada ponto.

<br>

*** 

<br>

## Performace do Modelo

**Modelo Escolhido:** GMM<br>
**Parametros:** sklearn.mixture.GaussianMixture(n_components=7, *, covariance_type='full', tol=0.001, reg_covar=1e-06, max_iter=100, n_init=1, init_params='kmeans', weights_init=None, means_init=None, precisions_init=None, random_state=None, warm_start=False, verbose=0, verbose_interval=10)<br>
**Numero de Clusters escolhido:** 7<br>
**Silhouette Score:** 0.725387<br>
**Davies Bouldin Score:** 0.344484<br>
**AIC / BIC Score:** 90942 / 91233 <br>

<center><img src="/images/gmm_performace_table.png" alt="table" width="445" height="338"/></center>


<i>Nota: o valor encontrado para o Silhouette Score e Davies Bouldin Score são consideravelmente bons,  a distancia intra cluster é relativamente alta ( estão bem separados)<i><br>

<br>

*** 

<br>

## Resultado dos Clusters

<center><img src="/images/gmm_clusters_graph.png" alt="clusters" width="700" height="525"/></center>


<blockquote style="color: #000000;">

**Cluster 00 - Zé Dinheirista**
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark>  

Count: 1086, 12.13%
Profit: $316.071,25

**Plano de Ação:** O que difere esses clientes para os demais são as operações com adiantamento em dinheiro, esse é o grupo com clientes que mais operam nessa modalidade. As taxas de adiantamento em dinheiro costumam ser altas.

***

**Cluster 01 - Zé Soneca** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark> 
- São clientes que não possuem dividas com relação ao cartão de crédito.

Plano de Ação: A estratégia nesse caso é reativar o cliente e identificar as possiveis causas, questões pessoais, problemas operacionais, acessibilidade, etc. Por serem clientes que não possuí debitos com o Banco, promoções com taxas mais acessíveis pode ser uma boa idéia.

Count: 2053.00	22.94%
Profit: $33.381.864,14

***

**Cluster 02 - Zé Parcelinho Pobre** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark> 

Count: 1812	20.25%
Purchases: $950.576,47
Profit: $385.453,49

Plano de Ação: A estratégia nesse caso é reativar o cliente e identificar as possiveis causas, questões pessoais, problemas operacionais, acessibilidade, etc. Por serem clientes que não possuí debitos com o Banco, promoções com taxas mais acessíveis pode ser uma boa idéia.


***

**Cluster 03 - Zé Entusiasta** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>levemente alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>levemente baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark> 

Count: 961, 10.74%
Profit: $814.026.84

Plano de Ação: São clientes que operam nas três modalidades do Banco, possuem um perfil de pessoa atenta as novidades e boas promoções. 

***

**Cluster 04 - Zé Lascado** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark> 

Count: 1697, 18.96%
Profit: -$276.002,85

Plano de Ação: A estratégia nesse caso é uma parcimonia entre cobrança e negociação das dividas.

    
***

**Cluster 05 - Zé Parcelinho Rico** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark>

Count: 458, 5.12%
Purchases: $230.613,74
Profit: $642.650,66

Plano de Ação: São clientes que não utilizam tanto o cartão de crédito mas quando utilizam estão dispostos a gastar mais, principalmente para compras parceladas, o saldo do cartão de crédito destes clientes estam sempre alto. São tendem a pagar mais do que os clientes do cluster 2


***

**Cluster 06 - Zé Pão Duro**
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark>

Count: 793,	8.86%
Purchases: $470.009,02
Profit: $927.983,38

Plano de Ação: São o pefil de cliente que usam pouco o cartão, usam para compras a de maior valor e quase sempre compram a vista. Um possivel plano de ação é aumentar o limite do cartão desses clientes a comprarem produtos mais caros.
    
</blockquote>    

## Viabilidade do Projeto

Os projetos de clusterização para segmentação de clientes costumam apresentar bons resultados mesmo em modelos mais simples em que apenas um cientista de dados consegue desenvolve-lo em um intervalo de tempo baixo. Como não temos uma base comparativa ( estamos considerando que hipoteticamente o Banco não possuí nenhum projeto com essa caracteristica), o projeto apresenta uma boa solução pois consegue dividir bem, grupos distintos de clientes, que necessitam de tratamentos diferentes. 

<center><img src="/images/priorization_matrix.png" alt="viability" width="900" height="720"/></center>

