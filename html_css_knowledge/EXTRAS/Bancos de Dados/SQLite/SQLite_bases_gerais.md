# O que é :
* É uma maneira de manipular arquivos de extensão ".db" (banco de dados) utilizando a linguagem de banco de dados **SQL**. 
* Ele é um programa que só é acessível através do terminal.  

# Instalação : 
* É só usar o seguinte comando no terminal :
	```CMD
	sudo apt update
	sudo apt install sqlite3
	``` 
# Coisas base  :
## [-- LINK --](https://absam.io/blog/como-instalar-a-usar-o-sqlite-no-ubuntu-20-04/)
## Shell e Bancos de dados : 
* O programa é dividido em duas partes, sendo elas : 
	* O **shell** : O shell é a "homepage" do programa, aonde você possui alguns comandos relacionados ao programa. 
	* Os Bancos de Dados : São os bancos de dados, utilizam a linguagem do **SQL** para fazer manipulações neles.
## Entrando no Shell :
* Para entrar no **shell** do programa, basta usar o seguinte comando : 
	```CMD
	sqlite3
	```

## Entrando no Banco de Dados  : 
* Crie um arquivo de extensão "db". 
* Abra um terminal no local do arquivo. 
* Então você terá duas maneiras de entrar neste arquivo usando o SQLite :
	* Fora do **shell**, use o comando no terminal : 
		```CMD
		sqlite3 banco_de_dados.db
		``` 
	* Dentro do **shell**, use o comando : 
		```shell
		.open banco_de_dados.db
		```
* ==DETALHE :=== 
	* Todos os comandos SQL usados no próprio SQLite, **precisam** terminar com ponto e virgula (;).  
# Integrando a alguma linguagem : 
## PHP : 
### [-- LINK --](https://www.youtube.com/watch?v=FvHrHM9K1X4)
### Conexão com o DB : 
* Antes, instale o sqlite3 para o php, através do comando :
	```CMD
	sudo apt-get install php5-sqlite3
	```
* Agora, no arquivo [php.ini](php_ini_php_file.md), habilite os seguintes drivers (Para habilitar esses drivers é só tirar o comentário do começo ";") : 
	* extension=sqlite3
	* extension=pdo_sqlite
	* extension_dir = "ext"
	* extension_dir = "./"
* Com tudo isso é pra ser possível se conectar com um banco de dados, **para se conectar com um banco de dados**, use o constructor especial "SQLite3", que retorna um [banco de dados como objeto]( SQLite_data_base_object)(DBO). Esse constructor pede como parâmetro o local do arquivo do "db", caso o arquivo não exista será criado um.  EX :
	```PHP
	$db = new SQLite3('banco.db');
	// variável "$db" é um objeto do seu banco 
	// "SQLite3('banco.db')" é o constructor especial que pedi como paramâmetro o local do arquivo do banco de dados, caso o arquivo não exista, será criado um. 
	``` 
* Agora o objeto "$db" carrega as informações do banco, sendo possível graças a ele fazer manipulações/acessa-lo pelo PHP.
### Manipulação do DB pelo PHP : 
* Com o [DBO](SQLite_data_base_object), você pode usar uma função dele chamada "exec".
* O exec permite rodar comandos **SQL** através do PHP.  
