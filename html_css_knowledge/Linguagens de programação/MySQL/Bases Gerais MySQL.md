# O que é : 
* SQL é a **linguagem** que o MySQL utiliza.

# Coisas Base : 
## Sintaxe : 
* As instruções do MySQL são em **maiúsculo**.
* Suas instruções são em **minúsculo**  
* EX:
	CREATE DATABASE pizzaria;
	"CREATE DATABASE" --> Comandos do MySQL.
	"pizzaria" --> Comando do usuário. 

* Termina com ponto e virgula (;)

## Coisas realmente básicas : 
* Quando for manipular em um banco de dados através do [workbank](MySQL_workbank), utilize o comando **"USE nome_do_banco"**, para avisar ao MySQL qual data base você deseja manipular.  
* Para comentar, use "-- --".
* [LINK PARA REVER TUDO.](https://youtu.be/XQkf-6Yl3WM?si=_I158NcIfEchQ-m0)
* Para acessar o painel do MySQL, acesse "http://localhost/phpmyadmin/".

# Manipulação de um Banco de Dados Básica : 
## Criar/Deletar Data Base 
### Criar :
* Para criar, no [workbank](MySQL_workbank), use os comandos "CREATE" ,  "DATABASE" e o nome que você deseja no banco de dados.
* EX:
```MySQL
CREATE DATABASE ronaldo_banco; 
/* APÓS EXECUTAR :  
Banco de dados criado 
```
### Deletar : 
* Para deletar, no [workbank](MySQL_workbank), use os comando "DROP" , "DATABASE" e o nome do banco de dados que deseja deletar. 
* EX: 
```MySQL
DROP DATABASE ronaldo_banco;  
/* APÓS EXECUTAR :  
Banco de dados deletado
```

# Manipulação de [Table](MySQL_organizacao_do_database) :
## Criar :
* Para criar uma table, use as Query "CREATE" , "TABLE", o nome da sua tabela e as colunas que ela irá possuir. 
* As colunas possuem tipos, sendo os principais : 
	* VARCHAR(\_par) --> Tipo string mais utilizado, o numero que você colocar no parâmetro será a quantidade de caracteres aceitos por essa coluna. 
* EX : 
```MySQL
USE pizzaria;
CREATE TABLE sabores(
	peperoni VARCHAR(10),
	calabresa VARCHAR(10)
);
```

## Deletar : 
* Para deletar uma table, use as Query "DROP", "TABLE" e o nome da sua table. 
* EX:
```MySQL
USE pizzaria;
DROP TABLE sabores;
```

## Alterar : 
* A base geral de alterar alguma coisa da tabela segue a mesma logica, sendo essa :
	* ==ALTER TABLE nome ALTERAÇÃO==
		* A query de ação "ALTER" indica que irá modificar algo
		* A query de especificação "TABLE" indica que irá modificar uma tabela 
		* "nome" é o nome da tabela que irá ser modificada.
		* "ALTERAÇÃO" é o que você deseja alterar da tabela
### Adicionar coluna :
* Para adicionar colunas a uma tabela já existente, use :
```MySQL
ALTER TABLE sabores ADD COLUMN quatro_queijos VARCHAR(255);
```
### Deletar uma coluna : 
* Para deletar uma coluna, use : 
```MySQL 
ALTER TABLE sabores DROP COLUMN peperoni;
-- "peperoni" é uma coluna que existe na table "sabores"
```

### Alterar valor de uma coluna : 
* Para alterar o valor de uma coluna é diferente, sendo : 
```MySQL
UPDATE tabela SET coluna = novo_valor;
```
*  Com "WHERE", é possível adicionar condições para a troca do valor, como : 
```SQL
/*
tabela : 
coluna = null id = 1
coluna = null id = 2
coluna = null id = 3
*/
UPDATE tabela SET coluna = "67" WHERE id = 1;
```
## **CRUD** :
### O que é :
* São recursos para a manipulação de uma [tabela](MySQL_organizacao_do_database).
* É dividido em 4 operações, onde cada uma significa :
	* C = Create --> INSERT
	* R = Read --> SELECT
	* U = Update --> UPDATE
	* D = Delete
### INSERT :
* No CRUD, ele cria um [item](MySQL_item), inserindo valor em cada uma das "colunas".
* EX:
```MySQL
-- Tabela "pessoas" possui as colunas : "nome", "idade" e "profissao"
INSERT INTO pessoas(nome,idade,profissao)
VALUES("ronaldo",19,"programador");
```

### SELECT (WHERE):
* No CRUD, ele serve para retorna dados do banco de dados. 
* Pode retornar os valores de uma [coluna especifica](MySQL_colunas_especificaveis) duma tabela e também pode **condicionar um valor para ser retornado** de alguma coluna (através do WHERE).
* EX:
```MySQL
SELECT * FROM tabela; 
-- Mostra no "workbank" as colunas de "tabela"
```

```MySQL
SELECT * FROM tabela WHERE id = 1;
-- Mostra no "workbank" somente o "item" de id 1
```
### UPDATE :
* No CRUD, ele serve para mudar valores de um [itens](MySQL_item), também consegue mudar o valor duma coluna.
* EX: 
```MySQL
UPDATE tabela SET coluna = new_valor 
-- todos os itens teve seu valor "coluna" igualado a "new_valor"
```
*  Com "WHERE", é possível adicionar condições para a troca do valor, como : 
```MySQL
/*
tabela : 
coluna = null id = 1
coluna = null id = 2
coluna = null id = 3 */
UPDATE tabela SET coluna = "67" WHERE id = 1;
/* agora está assim :
coluna = 67 id = 1
coluna = null id = 2
coluna = null id = 3 */
```
### DELETE : 
* No CRUD, deleta um [item](MySQL_item) ou uma [coluna](MySQL_organizacao_do_database). 
* EX:
```SQL
DELETE FROM tabela WHERE id = 2;
-- deleta o item da table "tabela" que possui a "id" igual a "2"
```


# Tipos de Dados :
## Texto : 
* VARCHAR(x) :
	* Tipo string mais utilizado, 
	* Limita a quantidade de caracteres que a variável pode receber. 

## Números :  
* INT :
	* Tipo de numero mais básico.
	* Pode limitar sua quantidade de caracteres.
## Datas : 
* TIMESTAMP :
	* Consegue guardar todas as informações de tempo.
	* São o ano, mês , dia , hora , minuto , segundos. 
* DATE :
	* Consegue informações sobre o dia.
	* A ordem é : ano, mês e dia

