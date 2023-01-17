<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

## Descrição do Problema
Uma das dificuldades nos processos seletivos são as situações em que o o candidato é obrigado a mostrar competencia em um intervalo de tempo relativamente pequeno, esse processo se da por uma ou mais entrevistas, provas teoricas, praticas, dinâmicas de analises comportamentais, etc. Outro problema é que Cientistas de Dados jr muitas vezes sequer chegam na etapa de entrevistas, seus os portifolios de projetos sequer são vistos, o que desanima um pouco já que muitos dos projetos demoram meses para serem desenvolvidos. 

Este projeto étem como objetivo simular o processo seletivo / inserção de um cientista de dados jr em um grande Banco Nacional. Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: detecção de fraude, segmentação de clientes, previsão de Inadinplencia, predição de Churn, analises em tempo real, automação de processos de comunicação. Para isso, o Banco forneceu algumas opções de datasets para escolha do candidado ( referentes as principais areas de atuação do Cientista de Dados como as citadas anteriormente) a partir dessa escolha o candidato apresentar um projeto num prazo de sete dias exibindo de acordo com os objetivos propostos a baixo.

<i>**Nota:** A premissa de que poderia ser um projeto de um processo seletivo Cientista de Dados Jr de um Banco, é uma percepção MINHA, não necessáriamente significa que os processos seletivos atuais seguem esse molde</i><br><br>


## Objetivo
**Principal:**
* O candidato deve desenvolver uma solução para o estudo de caso escolhido, o desenvolvimento consiste:
    -  Tratamento da Base de Dados
    -  Analise Exploratória de Dados 
    -  Criação do modelo de Machine Learning 
    -  Conclusão<br><br>

<i>**Nota:** O candidato será avaliado, principalmente pelo conhecimento de negócio, dominio das ferramentas de desenvolvimento Python/R, dominio das abordagens estatisticas e domínio em Machine Learning.</i>


**Secundário:**
* Justificar os motivos para a escolha do estudo de caso.
* Descrever o principio de funcionamento do algoritimo de Machine Learning selecionado e as métricas utilizadas.
* Apresentar a viabilidade do projeto, considerando que hipoteticamente a empresa possua poucas ou nenhuma solução na área de atuação escolhida.
* Apresentar um possivel plano de ação da empresa com base os resultados do estudo de caso.<br><br>

## Study Case

**Cluster Segmentation** - A segmentação de clientes é uma técnica de ciência de dados que envolve a análise de dados de clientes para dividi-los em grupos distintos que compartilham características semelhantes. Esses grupos, ou segmentos, são usados ​​para identificar oportunidades potenciais de marketing, desenvolvimento de produtos e atendimento ao cliente. Ao entender as características únicas de cada segmento, as empresas podem direcionar melhor seus produtos e serviços para atender às necessidades de clientes individuais.

**Base de Dados** - A base de dados contém os dados referentes ao uso do cartão de crédito de 8950 clientes de uma determinada agencia, coletados num determinado periodo. A base de dados está disponivel no [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)<br><br>


## Estágios de Desenvolvimento
[**Data Preprocessing**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/bank_market.ipynb)<br>
Lidando com valores ausentes com o KNN Imputer...

[**Exploratory Data Analysis**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/bank_market.ipynb)<br>
Estatistica Descritiva, Analise Univariada, Analise Multivariada.

[**Data Preparation**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/bank_market.ipynb)<br>
Detecção de Outlier com Isolation Forest, Normalização, Padronização, Redução de Dimensionalidade (PCA, UMAP, t-SNE).

[**Machine Learning Model**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/bank_market.ipynb)<br>
 Kmeans, Hierachical Clustering, Gaussian Mixture Model<br><br>


## Relatórios
[**Apresentação**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/resultados.md)<br>
[**Q & A - Operações com o Cartão de Crédito**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/qa.md)<br><br>


## Ferramentas
Linguagens: Python<br>
IDE: Visual Studio Code, Jupyter Notebook<br>
Bibliotecas: Pandas, Matplotlib, Seaborn, Plotly, Sklearn, scipy, yellowbricks<br>
Metodologia: CRISP-DM<br>

*** 

