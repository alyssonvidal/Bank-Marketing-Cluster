
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

Count: 1086, 12.13%<br>
Purchase: $912.743.45<br.>
Profit: $316.071,25

<u>Plano de Ação:</u> Uma campanha de marketing que o banco poderia adotar para incentivar os clientes a comprar com adiantamento em dinheiro é o lançamento de uma promoção de descontos em compras com dinheiro. Por exemplo, o banco poderia oferecer um desconto de 10% em compras feitas com dinheiro. Essa promoção pode ser aplicada a todos os clientes, ou a um grupo específico de clientes, como os que usam a conta corrente do banco. O banco também pode oferecer brindes, como um cartão de crédito de presente, para aqueles que fizerem compras com adiantamento em dinheiro. A promoção pode ser divulgada em meios de comunicação, como anúncios em jornais, rádios, outdoors, postagens em mídias sociais, e-mails e outras formas de marketing.

O Banco poderia instituir um programa de recompensas que oferece descontos e benefícios adicionais para os clientes que costumam comprar com adiantamento em dinheiro. Estas recompensas podem incluir ofertas de descontos em contas de poupança, empréstimos, serviços de transferência de dinheiro e outros serviços financeiros. O Banco também poderá oferecer acesso a produtos e serviços especiais para esses clientes, como cartões de crédito premium, serviços de investimento e até mesmo descontos em estabelecimentos comerciais parceiros.

***

**Cluster 01 - Zé Soneca** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark> 
- São clientes que não possuem dividas com relação ao cartão de crédito.

Count: 2053.00	22.94%<br>
Purchase: $59.02<br>
Profit: $33.381.864,14

<u>Plano de Ação:</u> Uma campanha de marketing que pode ser adotada pelo Banco para clientes ausentes no cartão de crédito seria uma campanha de reactivação. Esta campanha pode incluir ofertas especiais, como juros reduzidos ou um período de isenção de taxas e juros, para incentivar os clientes a começarem a usar novamente o cartão de crédito. O banco também pode criar uma campanha de marketing para educar os clientes sobre como usar de forma responsável o cartão de crédito. Isso pode incluir informações sobre como gerenciar as dívidas, evitar o endividamento excessivo e, assim, ajudar os clientes a obterem o máximo dos benefícios do cartão de crédito.



***

**Cluster 02 - Zé Parcelinho Pobre** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark> 

Count: 1812	20.25%<br>
Purchases: $950.576,47<br>
Profit: $385.453,49

<u>Plano de Ação:</u> Uma campanha de marketing para clientes que costumam comprar parcelado pode incluir ofertas como descontos em pagamentos à vista, cupons de desconto, ofertas de pagamento em até 12x sem juros, promoções com itens adicionais, entre outros. Além disso, também é importante focar em um serviço de atendimento ao cliente de qualidade para garantir a satisfação dos clientes com a experiência de compra.

Uma estratégia que o Banco poderia adotar com os seus clientes que costumam comprar parcelado é oferecer uma recompensa por não pedir mais parcelas. Por exemplo, eles podem receber um bônus de desconto na próxima compra se pagarem a compra à vista. Além disso, o banco também pode oferecer programas de fidelidade que recompensam os clientes que fazem compras frequentes com descontos e outras vantagens. Finalmente, o banco também pode oferecer programas educativos para ensinar os clientes a administrar suas finanças de forma responsável e evitar o endividamento.


***

**Cluster 03 - Zé Entusiasta** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>levemente alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>levemente baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark> 

Count: 961, 10.74%<br>
Purchase: $1,631.380,69<br>
Profit: $814.026.84

<u>Plano de Ação:</u> Uma campanha de marketing para clientes que costumam comprar em varias modalidades pode começar com um programa de fidelidade. Isso pode incluir oferecer um desconto especial para cada compra, a chance de acumular pontos e trocá-los por recompensas, além de oferecer ofertas exclusivas para os clientes mais fiéis. Além disso, você também pode considerar a criação de cupons de desconto para incentivar os clientes a comprar mais. O envio de e-mails com promoções especiais para clientes com histórico de compras anteriores também pode ser útil. Por fim, você também pode considerar a criação de uma comunidade online para seus clientes, permitindo que eles compartilhem suas experiências de compra e discutam promoções.

O Banco poderia oferecer benefícios especiais para os clientes entusiastas, como descontos em contas, descontos em serviços bancários, acesso a linhas de crédito especiais, ofertas exclusivas, cashback e outros incentivos. Além disso, o banco também pode oferecer programas educativos para ensinar aos clientes sobre os benefícios de gerenciar suas finanças, ajudando-os a tomar decisões financeiras informadas. Por fim, o banco também pode criar campanhas de marketing para promover seus serviços e incentivar os clientes a usá-los.

***

**Cluster 04 - Zé Lascado** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark> 

Count: 1697, 18.96%
Purchases: $3.572.670,52<br>
Profit: -$276.002,85

Plano de Ação: Uma campanha de marketing que o Banco poderia adotar para clientes que possuem dívidas no cartão de crédito seria oferecer um plano de pagamento flexível. O plano de pagamento flexível permitiria que os clientes parcelassem as dívidas em um prazo maior, com juros menores. Além disso, o banco também poderia oferecer bônus como descontos, cashback e outros incentivos para que os clientes possam quitar suas dívidas mais rapidamente.

    
***

**Cluster 05 - Zé Parcelinho Rico** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark>

Count: 458, 5.12%
Purchases: $230.613,74
Profit: $642.650,66

<u>Plano de Ação:</u> São clientes que não utilizam tanto o cartão de crédito mas quando utilizam estão dispostos a gastar mais, principalmente para compras parceladas, o saldo do cartão de crédito destes clientes estam sempre alto. São tendem a pagar mais do que os clientes do cluster 2


***

**Cluster 06 - Zé Pão Duro**
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixa frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark>

Count: 793,	8.86%
Purchases: $470.009,02
Profit: $927.983,38

<u>Plano de Ação:</u> São o pefil de cliente que usam pouco o cartão, usam para compras a de maior valor e quase sempre compram a vista. Um possivel plano de ação é aumentar o limite do cartão desses clientes a comprarem produtos mais caros.
    
</blockquote>    

## Viabilidade do Projeto

Os projetos de clusterização para segmentação de clientes costumam apresentar bons resultados mesmo em modelos mais simples em que apenas um cientista de dados consegue desenvolve-lo em um intervalo de tempo baixo. Como não temos uma base comparativa ( estamos considerando que hipoteticamente o Banco não possuí nenhum projeto com essa caracteristica), o projeto apresenta uma boa solução pois consegue dividir bem, grupos distintos de clientes, que necessitam de tratamentos diferentes. 

<center><img src="/images/priorization_matrix.png" alt="viability" width="900" height="720"/></center>