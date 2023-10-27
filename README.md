
### Introdução ao SQL/Learning SQL
![image](https://github.com/nadjapereira/introdu-o-ao-sql/assets/11997614/39799bdd-9b34-4f51-84f4-e31a414dbfbf)

Eu tenho a versão impressa deste livro em português e ele é relativamente barato. Certamente é o livro mais indicado para quem está dando os primeiros passos no SQL. 
Eles sugerem uma base chamada **rexon_metals** e a mesma é facilmente encontrável na web. 

##### Capítulo 4 
</p> 
O capítulo 4 é focado no SELECT, usado para exibir dados. </p>

```
Select * from  rexon_metals   
```

Usar o comando acima é excelente para fazer a abordagem exploratória de toda tabela que iremos trabalhar. 
Antes de realizar as queries, eu faço este **primeiro passo para aparecer todas as colunas.** 

Caso eu queira selecionar 2 colunas, eu faço:
```

Select name, region from customer; 
```

Uma coisa interessante no livro é o exemplo da página 37 para calcular um valor 7% maior, exemplo: 
```
Select
product_id,
description,
price,
price * 1.07 as taxed_price
from product
```

Acima ele criou uma tabela chamada 'taxed_price' com os valores calculados e acrescentados o 7%. 

> How to calculate a percent increase.
> A quick way to increase a number by a percentage, is to find the percent of your number, and add it to your number.
> So, suppose Jerry got a hot stock tip from a friend about some kind of robot butcher.
> Jerry bought the stock for $10 and it went up 37%. How much is Jerry's stock worth?

> - To get the answer, convert 37% to a decimal, which is .37 . You can find this on your calculator by typing 37 and hitting "%".
> - Now multiply .37 * 10, which is 3.70
> - Now add 3.70 to 10, and you get 13.70 which is your answer.*

> Another cool trick</p>
> You could also solve this problem by multiplying 10 * 1.37, which also gives you $13.70
If Jerry did this trick he could have saved a lot of time, and had an easy summmer. "The Summer of Jerry" 

Fonte: [Percent-change](https://percent-change.com/1-increase-by-7-percent)


Podemos usar o Round() para arredondar os valores em 2 casas decimais; o 2 na fórmula corresponde a quantidade de casas decimais que podemos arredondar. 

```
Select
product_id,
description,
price,
round(price * 1.07, 2) as taxed_price
from product

```

Concatenação de texto</p> 
A explicação é um pouco óbvia, serve para juntar textos. Por exemplo, temos na base em colunas separadas 'cidade' e 'estado', o próprio livro apresenta a opção 'location' com os dois.  
Você precisará usar o o pipe e o truque no teclado é com ALT + 124 para fazer as barrinhas. 


```
Select name,
city ||','|| state as location
from customer

```

Informações adicionais
> - AS é conhecido como ALIAS, usado para renomear a coluna com o valor calculado. 
> - Use sempre underscore se tiver dois nomes, como por exemplo, untaxed_price 

Operadores 
![image](https://github.com/nadjapereira/introdu-o-ao-sql/assets/11997614/5240d69f-d626-4637-ba75-38fd2fd4da8b)


Capítulo 3</p>
O que e SQLite 
SQLiteStudio
Importando e procurando banco de dados
Aqui o autor cita brevemente o que são 'views', uma espécie de consultas pré-definidas que são usadas com muita frequência. 
Uma coisa interessante a se fazer não citada pelo livro é clicar na database e conectar. Assim vai aparecerá as tabelas e as views. 

Capítulo 2</p> 
O que é um banco de dados?
Examinando um banco de dados relacionais
Por que tabelas separadas?
Selecionando uma solução de banco de dados
Banco de dados centralizados
	MySQL
	SQL Server
	Oracle
	PostgreSQL
	Teradata
	IBM DB2
	MariaDB

Capítulo 1</p> 
Por que aprender SQL?
O que é SQL e por que ele é vendável
