<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

# Descrição do Problema

Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: segmentação de clientes, detecção de fraude, previsão de inadinplência, predição de churn, analises em tempo real, automação de processos de comunicação, etc. 

Neste projeto será desenvolvido uma solução para o problema de segmentação de cliente de um Banco com base no perfil de uso do cartão de crédito, o objetivo é identificar esses clientes e com os resultados obtido sugerir um plano de ação.

O problema de segmentação de clientes em ciência de dados consiste na divisão dos clientes em grupos distintos que compartilham características semelhantes. Esses grupos, ou segmentos, são usados ​​para identificar oportunidades unicas, potenciais de marketing, desenvolvimento de produtos e atendimento personalizado. Ao entender as características únicas de cada segmento, o Banco pode direcionar melhor seus produtos e serviços para atender essas necessidades necessidades.
Através de algoritmos inteligentes de Machine Learning, é possivel desenvolver soluções otimizadas, capazes de fazer agrupamentos ( conhecidos também como clusters) matemáticamente o mais distinto possivel, descobrir padrões ocultos na base de dados e automatatizar processos de forma robusta e escalável.

A base de dados contém os dados referentes ao uso do cartão de crédito de 8950 clientes de uma determinada agencia, coletados num periodo de seis meses e está disponivel no [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)<br><br>


# Objetivo

* O candidato deve desenvolver uma solução dentre o escopo de atuação do cientista de dados para o Estudo de Caso escolhido.
* Apresentar um possivel plano de ação com base nos resultados obtidos.<br><br>

<i>Nota: O candidato será avaliado, principalmente pelo conhecimento de negócio, dominio das ferramentas de desenvolvimento Python/R, dominio das abordagens estatisticas e domínio em Machine Learning.</i><br><br>

# Estágios de Desenvolvimento
[**Pré Processamento dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part01_preprocessing.ipynb)<br>
Lidando com valores ausentes com o KNN Imputer...

[**Analise Exploratória dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part02_eda.ipynb)<br>
Analise Univariada, Analise Bivariada, Analise Multivariada.

[**Preparação dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
Detecção de Outlier com Isolation Forest, Normalização, Padronização, Redução de Dimensionalidade (PCA, UMAP, t-SNE).

[**Modelo de Machine Learning**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
 Kmeans, Hierachical Clustering, Gaussian Mixture Model<br><br>


# Relatórios
[**Resumo Técnico**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/resultados.md)<br>

# Ferramentas
Linguagens: Python<br>
IDE: Visual Studio Code, Jupyter Notebook<br>
Bibliotecas: Pandas, Matplotlib, Seaborn, Plotly, Sklearn, scipy, yellowbricks<br>
Metodologia: CRISP-DM<br><br>

***


# Resultados

Após o desenvolvimento do modelo de clusterização chegamos, numa solução otimizada para sete agrupamentos de clientes e um possivel plano de ação de acordo com as principais caracteristicas apontadas. A estratégia basica do plano de ação é explorar as modalidades de compra que o cliente estão habituados a usar, oferencendo-os vantagens.

<center><img src="/images/pie.png" alt="pie" width="512" height="411"/></center>

<center><img src="/images/clusters_table.png" alt="clusters" width="1007" height="237"/></center>