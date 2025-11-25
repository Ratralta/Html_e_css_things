# O que é : 

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
## Criar/Deletar [Table](MySQL_organizacao_do_database) : 
* Para mexer numa tabela, antes você precisar avisar ao [workbank](MySQL_workbank) em qual banco de dados você esta manipulando, então usando o comando **"USE nome_do_banco"**, você irá acessar o data base desejado. 
### Criar :
