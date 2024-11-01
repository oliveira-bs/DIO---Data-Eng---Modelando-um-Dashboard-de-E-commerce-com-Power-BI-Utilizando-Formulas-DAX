# Modelando um Dashboard de E-commerce com Power BI Utilizando Fórmulas DAX

## Objetivo

Utilizaremos a tabela única de Financial Sample para criar as tabelas dimensão e fato do nosso modelo baseado em star schema. Para construir este star schema devemos considerar que o objeto desta análise são as vendas realizadas dos produtos listados.


## Desenvolvimento

O processo consiste na criação das tabelas com base na tabela original. A partir da cópia serão selecionadas as colunas que irão compor a visão da nova tabela. Sendo assim, a partir da tabela principal serão criadas as tabelas:

Financials_origem (modo oculto – backup)

D_Produtos (ID_produto, Produto, Média de Unidades Vendidas, Médias do valor de vendas, Mediana do valor de vendas, Valor máximo de Venda, Valor mínimo de Venda)

D_Produtos_Detalhes(ID_produtos, Discount Band, Sale Price, Units Sold, Manufactoring Price)

D_Descontos (ID_produto, Discount, Discount Band)

D_Detalhes (Gross Sales, COGS, Month Number, Month Name, Year)

D_Calendário – Criada por DAX com calendar()

F_Vendas (SK_ID , ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Salers, Profit, Date (campos))

## Conclusão

O resultado desse projeto foi disponibilizado em [relatorio_PowerBI](Desafio_Modelando_Dashboard_Formula_DAX.pbix)