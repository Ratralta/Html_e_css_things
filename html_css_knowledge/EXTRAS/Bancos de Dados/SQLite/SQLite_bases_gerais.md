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

# Integrando a alguma linguagem : 
## PHP : 
### [-- LINK --](https://www.youtube.com/watch?v=FvHrHM9K1X4)
* Antes, instale o sqlite3 para o php, através do comando :
	```CMD
	sudo apt-get install php5-sqlite3
	```
* Agora, no arquivo [php.ini](php_ini_php_file), habilite os seguintes drivers (Para habilitar esses drivers é só tirar o comentário do começo ";") : 
	* extension=sqlite3
	* extension=pdo_sqlite
	* extension_dir = "ext"
	* extension_dir = "./"

* Agora para testar se está funcionando, copie e cole o seguinte código :
	```PHP 
	$db = new SQLite3('banco.db');
	$db->exec('CREATE TABLE foo (bar TEXT)');
	$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");
	$result = $db->query('SELECT bar FROM foo');
	var_dump($result->fetchArray());
	```

