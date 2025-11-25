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




## CRUD :
### O que é :
* São recursos para a manipulação de uma [tabela](MySQL_organizacao_do_database)
* É dividido em 4 operações, onde cada uma significa :
	* C = Create --> INSERT
	* R = Read --> SELECT
	* U = Update --> 
	* D = Delete
### INSERT :
* No CRUD, ele insere **valores** nas colunas de uma table.
* EX:
```MySQL
-- Tabela "pessoas" possui as colunas : "nome", "idade" e "profissao"
INSERT INTO pessoas(nome,idade,profissao)
VALUES("ronaldo",19,"programador");
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
	* São ano, mês e dia

