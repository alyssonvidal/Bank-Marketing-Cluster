<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

# Descrição do Problema

Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: segmentação de clientes, detecção de fraude, previsão de inadinplência, predição de churn, analises em tempo real, automação de processos de comunicação, etc. 

Neste projeto iremos desenvolver uma solução para o problema de segmentação de cliente de um Banco com base no perfil de uso do cartão de crédito, nosso objetivo é identificar esses clientes e com os resultados obtido sugerir um plano de ação.

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

<blockquote style="color: #000000;">

**Cluster 00 - Clientes com baixa frequencia de uso do cartão de crédito e que compram quase sempre a vista**

Clientes: 1086, 12.13%<br>
Compras: $912.743.45<br>
Frequencia média de compras: 0.35<br>
Qtd média de compras: 7.40 +/- 11.47<br>
Lucro: $316.071,25<br>
Limite de Crédito Médio: $4411.29<br>
Qtd de clientes que excederam o limite de crédito: 50


<u>Plano de Ação:</u> O Banco poderia aumentar o limite do cartão de crédito, como são clientes quem compram em qualidade não quantidade talvez um saldo maior um pouco seja um insentivo a gastar mais.

***

**Cluster 01 - Clientes com baixa frequencia de uso do cartão de crédito e que compram quase sempre com adiantamento em dinheiro** 

Clientes: 2053.00, 22.94%<br>
Compras: $59.02<br>
Frequencia média de compras: 0.00<br>
Qtd média de compras: 0.01 +/-	0.10<br>
Lucro: $33.381.864,14<br>
Limite de Crédito Médio: $4020.97 +/- 3249.02<br>
Qtd de clientes que excederam o limite de crédito: 50<br>

<i>A base de dados não possuí dados referentes ao pagamento do adiantamento. Além disso mesmo não utilizando o cartão os Bancos lucram através de taxas de admnistração, manutenção, anuidade,etc... por isso o lucro alto</i><br>


<u>Plano de Ação:</u> O Banco poderia iniciar um programa que instrua e estimule esses clientes o o cartão de crédito já que eles possuem saldo mas não utilizam, essas pessoas talvez possuem alguns receios pelo fato das taxas de juros do cartão de crédito, serem maior do que as do adiantamento em dinheiro.


***

**Cluster 02 - Clientes com alta frequencia de uso do cartão de crédito e que compram parcelado** 

Clientes: 1812, 20.25%<br>
Compras: $950.576,47<br>
Frequencia média de compras: 0.70<br>
Qtd média de compras: 11.68	+/- 11.33<br>
Lucro: $385.453,49<br>
Limite de Crédito Médio: $3114.81 +/- 2692.72<br>
Qtd de clientes que excederam o limite de crédito: 57


<u>Plano de Ação:</u> O Banco poderia oferecer parcelamentos especiais para compras realizadas com o cartão de crédito, com taxas de juros mais baixas ou prazos de pagamento mais longos, o Banco poderia oferecer ainda mais benefícios para aqueles que usam o cartão frequentemente, como descontos em produtos específicos ou serviços adicionais.


***

**Cluster 03 - Clientes com alta frequencia de uso do cartão de crédito e que compram em todas modalidades** 

Clientes: 961, 10.74%<br>
Compras: $1,631.380,69<br>  
Frequencia média de compras: 0.78<br>
Qtd média de compras: 28.37	+/- 25.48<br>
Lucro: $814.026.84<br>
Limite de Crédito Médio: $5589.61 +/- 3908.91<br>
Qtd de clientes que excederam o limite de crédito: 69

<u>Plano de Ação:</u> O Banco poderia fazer um programa de fidelidade, já que são clientes que operam em todos as modalidades, são os clientes extremamente lucrativos.


***

**Cluster 04 - Clientes com alta frequencia de uso do cartão de crédito e com histórico ruim de pagamento** 

Clientes: 1697, 18.96%<br>
Compras: $3.572.670,52<br>
Frequencia média de compras: 0.81<br>
Qtd média de compras: 32.41 +/- 31.07<br>
Lucro: -$276.002,85<br>
Limite de Crédito Médio: $5539.68 +/- 3774.96<br>
Qtd de clientes que excederam o limite de crédito: 203


<u>Plano de Ação:</u> O Banco oferecer um plano de pagamento flexível. O plano de pagamento flexível permitiria que os clientes parcelassem as dívidas em um prazo maior, com juros menores. Além disso, o banco também poderia oferecer bônus como descontos, cashback e outros incentivos para que os clientes possam quitar suas dívidas mais rapidamente.

    
***

**Cluster 05 - Clientes com alta frequencia de uso do cartão de crédito, que quase sempre compram parcelados e eventualmente com adiantamento em dinheiro** 

Clientes: 458, 5.12%<br>
Compras: $230.613,74
Frequencia média de compras: 0.65<br>
Qtd média de compras: 11.58	+/- 11.64<br>
Lucro: $642.650,66<br>
Limite de Crédito Médio: $4298.91 +/- 3516.92<br>
Qtd de clientes que excederam o limite de crédito: 8


<u>Plano de Ação:</u> São clientes que estão dispostos a gastar mais quando comparado com o cluster 2, o plano de ação poderia ser o mesmo.


***

**Cluster 06 - Clientes com baixa frequencia de usdo do cartão de crédito, que quase sempre compram a vista e eventualmente com adiantamento em dinheiro** 

Clientes: 793,	8.86%<br>
Compras: $470.009,02
Frequencia média de compras: 0.28<br>
Qtd média de compras: 6.23 +/- 13.33<br>
Lucro: $927.983,38<br>
Limite de Crédito Médio: $4584.27 +/- 3462.71<br>
Qtd de clientes que excederam o limite de crédito: 14


<u>Plano de Ação:</u> São o pefil de cliente que usam pouco o cartão, usam para compras a de maior valor e quase sempre compram a vista. Um possivel plano de ação é aumentar o limite do cartão desses clientes a comprarem produtos mais caros.
    
</blockquote>    

<center><img src="/images/swarm.png" alt="swarm" width="962" height="783"/></center>

## Referencias
https://www.forbes.com/advisor/credit-cards/what-is-a-cash-advance-and-should-you-get-one/
https://www.infomoney.com.br/guias/cartao-de-credito/