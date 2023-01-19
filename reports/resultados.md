
# Report

Essa parte será apresentado os resultados do projeto de forma resumida.

<br><br>

## Justifique a escolha do Estudo de Caso para Costumer Segmentation?

No problema de Customer Segmentation, através de algoritimos de clusterização, somos capazes de produzir insights sobre como dados similares estão relacionados e agrupados e nos ajuda também entender nosso problema de negócio, desde os conceitos mais basicos até a identificação de padrões mais ocultos. Os algoritmos de clusterização também podem ajudar a reduzir o tamanho de um conjunto de dados e permitir que os dados sejam analisados mais facilmente.

Considerando a segunda parte do projeto, "viabilidade", os projetos de Costumer Segmentation são um otimo ponto de partida dentre o escopo de atuação do Cientista de Dados. Para uma empresa que não tem nenhuma ou pouca estrutura nesse aspecto. 

<br>

*** 

<br>

## Modelo - GMM

O **Modelo de Mistura Gaussiana (GMM)** é um modelo de agrupamento probabilístico que assume que cada ponto de dados é gerado por uma mistura de um número finito de distribuições Gaussianas com parâmetros desconhecidos. Esses parâmetros incluem os limites de cada distribuição Gaussiana, bem como os pesos que determinam a proporção de cada distribuição na mistura. Os GMMs são comumente usados ​​para aplicações de cluster, pois podem modelar clusters que não são necessariamente redondos ou elípticos, dessa forma ele pode ser considerado uma extrapolação de outro modelo conhecido, o KMeans.

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