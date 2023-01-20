<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

# Descrição do Problema

Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: segmentação de clientes, detecção de fraude, previsão de inadinplência, predição de churn, analises em tempo real, automação de processos de comunicação, etc. 

Neste projeto será desenvolvido uma solução para o problema de segmentação de cliente de um Banco com base no perfil de uso do cartão de crédito, o objetivo é identificar esses clientes e com os resultados obtido sugerir um plano de ação.

O problema de segmentação de clientes em ciência de dados consiste na divisão dos clientes em grupos distintos que compartilham características semelhantes. Esses grupos, ou segmentos, são usados ​​para identificar oportunidades unicas, potenciais de marketing, desenvolvimento de produtos e atendimento personalizado. Ao entender as características únicas de cada segmento, o Banco pode direcionar melhor seus produtos e serviços para atender essas necessidades necessidades.
Através de algoritmos inteligentes de Machine Learning, é possivel desenvolver soluções otimizadas, capazes de fazer agrupamentos ( conhecidos também como clusters) matemáticamente o mais distinto possivel, descobrir padrões ocultos na base de dados e automatatizar processos de forma robusta e escalável.

A base de dados contém dados referentes ao uso do cartão de crédito de 8950 clientes de uma determinada agencia, coletados num periodo de seis meses. Está disponivel no [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)<br><br>


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

<center><img src="/images/clusters_table.png" alt="clusters" width="1104" height="277"/></center>

<i> O lucro descrito refere-se apenas as operações com cartão de crédito (a vista e parcelado) a base de dados não possui informações suficientes para calcular o lucro referente ao paganmento do adiantamento em dinheiro.<br>

Os clientes do Cluster "01" possuem saldo no cartão de crédito no entando não usam, de qualquer formas as taxas de anuidade, admistração, manutenção entre outras são cobradas, e são lucrativas para o Banco, que lucrou nesse periodo com esses clientes $33.381.864,14.</i>

## Plano de Ação

Cluster 00 - São clientes que compram pouco no cartão de crédito, mas quando compram optam pelo pagamento a vista. em baixa quantidade mas de valores mais elevados, possuem tendencia a se endividar. Um plano de ação do Banco poderia ser instruir esse clientes a usarem mais o cartão de crédito parcelado para evitar que se endividem num periodo de tempo curto.

**Cluster 01 -**  São clientes possuem saldo no cartão de crédito mas não utilizam e optam pelo adiantamento em dinheiro. Essas pessoas talvez possuem alguns receios pelo fato das taxas de juros do cartão de crédito, serem maior do que as do adiantamento em dinheiro. Um plano de ação interessante seria iniciar um programa capaz de instruir, estimular e facilitar esses clientes a utilizarem o cartão de crédito, um programa capaz de oferecer suporte ao cliente para facilitar a compreensão das taxas, tarifas e outras obrigações associadas ao uso do cartão de crédito; oferecer opção de pagar suas contas de cartão de crédito online; alertas de pagamento para ajudar os clientes a lembrar de realizar seus pagamentos em tempo, etc.

**Cluster 02 -** São cliente que tem o hábito de comprar com cartão de crédito parcelado, são clientes com tendencia a se endividarem. Um plano de ação poderia ser oferecer incentivos, como descontos, pontos de recompensa e outras vantagens.

**Cluster 03 -** São clientes entusiastas, que estão acostumados a comprar em todas as modalidades e possuem limite de crédito elevado. Um plano de ação seria a criação de um programa de fidelidade, para garantir que esse cliente continue no Banco.

**Cluster 04 -** São clientes endividados, que não estão as vezes o minimo requisitado pelo cartão de crédito. Um plano de ação seria o Banco oferecer um plano de pagamento flexivel que esses clientes parcelassem as dívidas em um prazo maior, com juros menores. Além disso, o banco também poderia oferecer bônus como descontos, cashback e outros incentivos para que os clientes possam quitar suas dívidas mais rapidamente.

**Cluster 05 -** São cliente que tem o hábito de comprar com cartão de crédito parcelado, são clientes com bom historico de pagamento. Um plano de ação poderia ser oferecer incentivos, como descontos, pontos de recompensa e outras vantagens.

**Cluster 06 -** São clientes que compram pouco no cartão de crédito, mas quando compram optam tanto pelo pagamento a vista quanto adiantamento em dinheiro. São clientes possuem saldo mas não utilizam, usam para compras a de maior valor e quase sempre compram a vista, no geral possuem bom histórico de pagamento. Um plano de ação interessante poderia é o aumento do limite de crédito de forma a incentivar compras com valores ainda mais maiores.