
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

O Modelo de Mistura Gaussiana (GMM) é um modelo de agrupamento probabilístico que assume que cada ponto de dados é gerado por uma mistura de um número finito de distribuições Gaussianas com parâmetros desconhecidos. Os GMMs são comumente usados ​​para aplicações de cluster, pois podem modelar clusters que não são necessariamente redondos ou elípticos, dessa forma ele pode ser considerado uma extrapolação de outro modelo conhecido, o KMeans.

<br>

***

<br>

## Explique o principio de funcionamento de pelo menos uma das métricas escolhidas

O **Silhouette Score** é uma métrica usada para medir o quão próximo cada ponto em um cluster está dos pontos em outros clusters. Pode variar de -1 (indicando que o ponto está muito distante de outros clusters) a 1 (indicando que o ponto está muito próximo de outros clusters). É calculado tomando a média do coeficiente de silhueta para cada ponto.

$$s(i) = \frac{b(i) - a(i)}{\max\{a(i), b(i)\}}$$

onde:

$a(i) = \frac{1}{|C_i| - 1} \sum_{j \in C_i, j \neq i} d(i, j)$

$b(i) = \min_{k \in C, k \neq C_i} \left\{\frac{1}{|C_k|} \sum_{j \in C_k} d(i, j)\right\}$

$C_i$ is the set of data points in cluster $i$

$d(i, j)$ is the distance between data points $i$ and $j$

<br>

*** 

<br>

## Performace do Modelo

**Modelo Escolhido:** GMM<br>
**Parametros:**
**Numero ótimo de Clusters:** 7<br>
**Numero de Clusters escolhido:** 7<br>
**Silhouette Score:** 0.725387<br>
**Davies Bouldin Score:** 0.725387<br>
**AIC / BIC Score:** 90942 / 91233 <br>

<blockquote style="color: #000000;">

**Cluster 00 - Cannot Lose Them** 
- São clientes que <mark>utilizam o cartão de crédito com baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark> 
- São clientes que possuem <mark>moderada taxa de pagamento</mark>  com relação ao valor integral do cartão de crédito

*Rating: 3.5*

***

**Cluster 01 - Hinernating** 
- São clientes que <mark>utilizam o cartão de crédito com baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 1.0

***

**Cluster 02 - Champions** 
- São clientes que <mark>utilizam o cartão de crédito com alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>altissima frequencia</mark> 
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark>
- São clientes que possuem <mark>alta taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 5.0

***

**Cluster 03 - Trouble Costumer** 
- São clientes que <mark>utilizam o cartão de crédito com baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>baixissima frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 2.5

***

**Cluster 04 - Loyal Customers** 
- São clientes que <mark>utilizam o cartão de crédito com altissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>moderada frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>baixissima frequencia</mark>
- São clientes que possuem <mark>alta taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 4.5
    
***

**Cluster 05 - Need Attention** 
- São clientes que <mark>utilizam o cartão de crédito com moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>alta frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito

Rating: 3.0

***

**Cluster 06**
- São clientes que <mark>utilizam o cartão de crédito com altissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>"ONE OFF"</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>"Parcelado"</mark> com <mark>moderada frequencia</mark>
- São clientes que <mark>solicitam adiantamento</mark> de crédito com <mark>alta frequencia</mark>
- São clientes que possuem <mark>baixa taxa de pagamento</mark> com relação ao valor integral do cartão de crédito


Rating: 3.0
    
</blockquote>    

## Esboço de Estudo de Viabilidade do Projeto

<center><img src="/images/priorization_matrix.png" alt="viability" width="900" height="720"/></center>

## Possível plano de ação


