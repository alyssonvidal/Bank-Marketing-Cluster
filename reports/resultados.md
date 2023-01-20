
# Resumo Técnico


## Data Preprocessing

**Linhas:** 8950

**Colunas:** 18

**Valores Duplicados:** 0<br>
**Estratégia:** Nenhuma

**Valores Faltantes:** MINIMUM_PAYMENTS(313), CREDIT_LIMIT(1)<br>
**Estratégias:** KNN Imputer

<br>

*** 
<br>

## Data Preparation


**Normalização:** Sim<br>
**Estratégia:** log1p colunas com assimetria maior que 0.75

**Padronização:** Sim<br>
**Estratégia:** MinMaxScaler, StandardScaler

**Tratamento de Outliers:** Sim<br>
**Estratégia** Isolation Forest, com indice de contaminação de 0.01%

**Redução de Dimensionalidade:** Sim<br>
**Estratégia:** PCA(9) e UMAP(2)

<br>

*** 

<br>

## Modelo - GMM

O **Modelo de Mistura Gaussiana (GMM)** é um modelo de agrupamento probabilístico que assume que cada ponto de dados é gerado por uma mistura de um número finito de distribuições Gaussianas com parâmetros desconhecidos. Esses parâmetros incluem os limites de cada distribuição Gaussiana, bem como os pesos que determinam a proporção de cada distribuição na mistura. Os GMMs são comumente usados ​​para aplicações de cluster, pois podem modelar clusters que não são necessariamente redondos ou elípticos, dessa forma ele pode ser considerado uma extrapolação de outro modelo conhecido, o KMeans.

**Parametros:** sklearn.mixture.GaussianMixture(n_components=7, *, covariance_type='full', tol=0.001, reg_covar=1e-06, max_iter=100, n_init=1, init_params='kmeans', weights_init=None, means_init=None, precisions_init=None, random_state=None, warm_start=False, verbose=0, verbose_interval=10)<br>
**Numero de Clusters:** 7<br>
**Silhouette Score:** 0.725387<br>
**Davies Bouldin Score:** 0.344484<br>
**AIC / BIC Score:** 90942 / 91233 <br>

<center><img src="/images/gmm_performace_table.png" alt="table" width="445" height="338"/></center>


<i>Nota: o valor encontrado para o Silhouette Score e Davies Bouldin Score são consideravelmente bons,  a distancia intra cluster é relativamente alta ( estão bem separados)<i><br>

<center><img src="/images/gmm_clusters_graph.png" alt="clusters" width="700" height="525"/></center>

<br>

*** 

<br>

## Interpretação do Clusters

