# fjmorais.github.io

#### Download Database AdventureWorks Database Versão 2022:

Link: https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2022.bak

#### Entendendo o projeto:

O Gerente da AdventureWorks deseja receber um relatório em um formato D-1 com as seguintes informações:

1 - Vendas unitárias bem como a sua quantidade;

2 - Produtos Vendidos;

3 - Data do Pedido;

4 - Localidade;

5 - Loja.

Com essa ideia temos a necessidade de criar:

1 - Uma Fato de vendas com o valor unitário e sua quantidade;

2 - Dimensão de Produtos;

3 - Dimensão de Data do porduto vendido;

4 - Dimesão de localidade;

5 - Dimensão Loja.


#### Fazendo o SQL Power Archicteture para a modelagem do banco de dados Stage

![image](https://github.com/fjmorais/fjmorais.github.io/assets/40808066/a5a9f7d3-4f73-4a24-acc9-a7104e1763bf)





Figura 1 - Modelagem OLAP para o DW Vendas AdventureWorks2022

Um ponto de atenção nesse modelagem está no quesito de inserir o identificador único da venda na tabela fato. Como a mesmo não representa uma Dimensão, temos o que chamamos de Dimensão Degenerada. E, nesse caso também, esse tipo de modelagem permite em uma base de dados onde o valor unitário pode receber uma atualização ou até mesmo ser excluído, criar uma processo para atualizar o dado na tabela fato ou até mesmo excluir.








