
# Report

Essa parte é a respostas para as perguntas solicitadas um recorte do que foi desenvolvido 
<br><br>

## Justifique a escolha do estudo de caso para Costumer Segmentation?

No problema de Customer Segmentation, através de algoritimos de clusterização, somos capazes de produzir insights sobre como dados similares estão relacionados e agrupados e nos ajuda também entender nosso problema de negócio, desde os conceitos mais simples até a identificação de padrões mais ocultos. Os algoritmos de clusterização também podem ajudar a reduzir o tamanho de um conjunto de dados e permitir que os dados sejam analisados mais facilmente.

Considerando a segunda parte do projeto, "viabilidade", os projetos de Costumer Segmentation são um otimo ponto de partida dentre o escopo de atuação do Cientista de Dados. Para uma empresa que não tem nenhuma ou pouca estrutura nesse aspecto, os algoritimos de clusterização costumam produzir bons resultados mesmo nos algoritimos mais simples. 

<br>

***

<br>

## Explique o principio de funcionamento do algortimo escolhido

O **Modelo de Mistura Gaussiana (GMM)** é um modelo de agrupamento probabilístico que assume que cada ponto de dados é gerado por uma mistura de um número finito de distribuições Gaussianas com parâmetros desconhecidos. Esses parâmetros incluem os limites de cada distribuição Gaussiana, bem como os pesos que determinam a proporção de cada distribuição na mistura. Os GMMs são comumente usados ​​para aplicações de cluster, pois podem modelar clusters que não são necessariamente redondos ou elípticos, dessa forma ele pode ser considerado uma extrapolação de outro modelo conhecido, o KMeans.

<br>

***

<br>

## Explique o principio de funcionamento de pelo menos uma das métricas escolhidas

O **Silhouette Score** é uma métrica usada para medir o quão próximo cada ponto em um cluster está dos pontos em outros clusters. Pode variar de -1 (indicando que o ponto está muito distante de outros clusters) a 1 (indicando que o ponto está muito próximo de outros clusters). É calculado tomando a média do coeficiente de silhueta para cada ponto.

<br>

*** 

<br>

## Performace do Modelo

**Modelo Escolhido:** GMM<br>
**Parametros:** sklearn.mixture.GaussianMixture(n_components=7, *, covariance_type='full', tol=0.001, reg_covar=1e-06, max_iter=100, n_init=1, init_params='kmeans', weights_init=None, means_init=None, precisions_init=None, random_state=None, warm_start=False, verbose=0, verbose_interval=10)<br>
**Numero ótimo de Clusters:** 7<br>
**Numero de Clusters escolhido:** 7<br>
**Silhouette Score:** 0.725387<br>
**Davies Bouldin Score:** 0.344484<br>
**AIC / BIC Score:** 90942 / 91233 <br>

<center><img src="/images/gmm_performace_table.png" alt="table" width="445" height="338"/></center>


<i>Nota: o valor encontrado para o Silhouette Score é bom, o que siginifica que a distancia intra cluster é relativamente alta ( estão bem separados)<i><br>

<br>

*** 

<br>

## Resultado dos Clusters

<center><img src="/images/gmm_clusters_graph.png" alt="clusters" width="700" height="525"/></center>


<blockquote style="color: #000000;">

**Cluster 00 - Cannot Lose Them** 
- São clientes que <mark>utilizam o cartão de crédito com baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark> 
- São clientes que possuem <mark>moderada taxa de pagamento</mark>  com relação ao valor integral do cartão de crédito

Plano de Ação:

***

**Cluster 01 - Hinernating** 
- São clientes que <mark>utilizam o cartão de crédito com baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 1.0

***

**Cluster 02 - Champions** 
- São clientes que <mark>utilizam o cartão de crédito com alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>altissima frequencia</mark> 
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark>
- São clientes que possuem <mark>alta taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 5.0

***

**Cluster 03 - Trouble Costumer** 
- São clientes que <mark>utilizam o cartão de crédito com baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 2.5

***

**Cluster 04 - Loyal Customers** 
- São clientes que <mark>utilizam o cartão de crédito com altissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>moderada frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark>
- São clientes que possuem <mark>alta taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 4.5
    
***

**Cluster 05 - Need Attention** 
- São clientes que <mark>utilizam o cartão de crédito com moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>alta frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 3.0

***

**Cluster 06**
- São clientes que <mark>utilizam o cartão de crédito com altissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"a vista"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"parcelado"</mark> com <mark>moderada frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito


Rating: 3.0
    
</blockquote>    

## Viabilidade do Projeto

Os projetos de clusterização para segmentação de clientes costumam apresentar bons resultados mesmo em modelos mais simples em que apenas um cientista de dados consegue desenvolve-lo em um intervalo de tempo baixo. Como não temos uma base comparativa ( estamos considerando que hipoteticamente o Banco não possuí nenhum projeto com essa caracteristica), o projeto apresenta uma boa solução pois consegue dividir bem, grupos distintos de clientes, que necessitam de tratamentos diferentes. 

<center><img src="/images/priorization_matrix.png" alt="viability" width="900" height="720"/></center>