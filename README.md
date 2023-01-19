<center><img src="/images/pexels-pixabay-259200.jpg" alt="logo" width="800" height="600"/></center>

## Descrição do Problema
Uma das dificuldades nos processos seletivos são as situações em que o o candidato é obrigado a mostrar competencia em um intervalo de tempo relativamente pequeno, esse processo se da por uma ou mais entrevistas, provas teoricas, praticas, dinâmicas de analises comportamentais, etc. Outro problema é que Cientistas de Dados jr muitas vezes sequer chegam na etapa de entrevistas, seus os portifolios de projetos sequer são vistos, o que desanima um pouco já que muitos dos projetos demoram meses para serem desenvolvidos. 

Este projeto tem como objetivo simular o processo seletivo / inserção de um cientista de dados jr em um grande Banco Nacional. Os Bancos e outras intituições financeiras são hoje um dos setores que mais contratam cientistas de dados, devido a grande variedade de soluções propiciada por eles: detecção de fraude, segmentação de clientes, previsão de Inadinplencia, predição de Churn, analises em tempo real, automação de processos de comunicação, etc. 

Para isso, o Banco forneceu algumas opções de datasets para candidado escolher( referentes as principais áreas de atuação do Cientista de Dados como as citadas anteriormente), a partir dessa escolha o candidato deverá apresentar um projeto num prazo máximo de sete dias exibindo de acordo com os objetivos propostos a baixo.

<i>**Nota:** A premissa de que poderia ser um projeto de um processo seletivo Cientista de Dados Jr de um Banco, é uma percepção minha, não necessáriamente significa que os processos seletivos atuais seguem esse molde.</i><br><br>


## Objetivo
**Principal:**
* O candidato deve desenvolver uma solução dentre o escopo de atuação do cientista de dados para o Estudo de Caso escolhido.
* Reportar os resultados obtidos. 
<br><br>

<i>Nota: O candidato será avaliado, principalmente pelo conhecimento de negócio, dominio das ferramentas de desenvolvimento Python/R, dominio das abordagens estatisticas e domínio em Machine Learning.</i>


**Secundário:**
* Justificar os motivos para a escolha do estudo de caso.
* Descrever o principio de funcionamento do algoritimo de Machine Learning selecionado e as métricas utilizadas.
* Apresentar a viabilidade do projeto, considerando que hipoteticamente o Banco possua poucas ou nenhuma solução na área de atuação escolhida.
* Apresentar um possivel plano de ação do Banco com base os resultados obtidos<br><br>

## Estudo de Caso

**Cluster Segmentation** - A segmentação de clientes é uma técnica de ciência de dados que envolve a análise de dados de clientes para dividi-los em grupos distintos que compartilham características semelhantes. Esses grupos, ou segmentos, são usados ​​para identificar oportunidades potenciais de marketing, desenvolvimento de produtos e atendimento ao cliente. Ao entender as características únicas de cada segmento, as empresas podem direcionar melhor seus produtos e serviços para atender às necessidades de clientes individuais.

**Base de Dados** - A base de dados contém os dados referentes ao uso do cartão de crédito de 8950 clientes de uma determinada agencia, coletados num periodo de seis meses. A base de dados está disponivel no [kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)<br><br>


## Estágios de Desenvolvimento
[**Pré Processamento dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part01_preprocessing.ipynb)<br>
Lidando com valores ausentes com o KNN Imputer...

[**Analise Exploratória dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part02_eda.ipynb)<br>
Analise Univariada, Analise Bivariada, Analise Multivariada.

[**Preparação dos dados**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
Detecção de Outlier com Isolation Forest, Normalização, Padronização, Redução de Dimensionalidade (PCA, UMAP, t-SNE).

[**Modelo de Machine Learning**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/notebooks/part03_model.ipynb)<br>
 Kmeans, Hierachical Clustering, Gaussian Mixture Model<br><br>


## Relatórios
[**Apresentação**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/resultados.md)<br>
[**Q & A - Operações com o Cartão de Crédito**](https://github.com/alyssonvidal/Bank-Marketing-Cluster/blob/main/reports/qa.md)<br><br>


## Ferramentas
Linguagens: Python<br>
IDE: Visual Studio Code, Jupyter Notebook<br>
Bibliotecas: Pandas, Matplotlib, Seaborn, Plotly, Sklearn, scipy, yellowbricks<br>
Metodologia: CRISP-DM<br>

**

# Resumo

Após o desenvolvimento do modelo de clusterização chegamos, numa solução otimizada para sete agrupamentos de clientes, com as seguintes caracteristicas:

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

Count: 2053.00, 22.94%<br>
Purchase: $59.02<br>
Profit: $33.381.864,14

<u>Plano de Ação:</u> Uma campanha de marketing que pode ser adotada pelo Banco para clientes ausentes no cartão de crédito seria uma campanha de reactivação. Esta campanha pode incluir ofertas especiais, como juros reduzidos ou um período de isenção de taxas e juros, para incentivar os clientes a começarem a usar novamente o cartão de crédito. O banco também pode criar uma campanha de marketing para educar os clientes sobre como usar de forma responsável o cartão de crédito. Isso pode incluir informações sobre como gerenciar as dívidas, evitar o endividamento excessivo e, assim, ajudar os clientes a obterem o máximo dos benefícios do cartão de crédito.



***

**Cluster 02 - Zé Parcelinho Pobre** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>alta frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixissima frequencia</mark>
- São clientes que na média possuem <mark>pouco saldo</mark> no cartão de crédito 

Count: 1812, 20.25%<br>
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

Count: 1697, 18.96%<br>
Purchases: $3.572.670,52<br>
Profit: -$276.002,85

Plano de Ação: Uma campanha de marketing que o Banco poderia adotar para clientes que possuem dívidas no cartão de crédito seria oferecer um plano de pagamento flexível. O plano de pagamento flexível permitiria que os clientes parcelassem as dívidas em um prazo maior, com juros menores. Além disso, o banco também poderia oferecer bônus como descontos, cashback e outros incentivos para que os clientes possam quitar suas dívidas mais rapidamente.

    
***

**Cluster 05 - Zé Parcelinho Rico** 
- São clientes que utilizam a modalidade <mark>a vista</mark> com <mark>baixissima frequencia</mark>
- São clientes que utilizam a modalidade <mark>parcelado</mark> com <mark>moderada frequencia</mark>
- São clientes que utilizam a modalidade <mark>adiantamento em dinheiro</mark> com <mark>baixa frequencia</mark>
- São clientes que na média <mark>possuem bastante</mark> saldo no cartão de crédito

Count: 458, 5.12%<br>
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

## Referencias
https://www.forbes.com/advisor/credit-cards/what-is-a-cash-advance-and-should-you-get-one/