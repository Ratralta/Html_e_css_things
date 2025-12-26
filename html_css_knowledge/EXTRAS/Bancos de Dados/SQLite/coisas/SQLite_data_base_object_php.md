# O que é : 
* Data Base Object(DBO), é um objeto do banco de dados apos fazer uso do constructor especial "SQLite3".
* Com ele é possível manipular o data base através da função "exec" do DBO. 
# Comandos de um PDO :
## exec :
### O que é :
* Permite executar comandos [[SQL]] no PDO. 
### EX :
#### Criação de tabela básica :
```PHP
$conn = new SQLite3('data_base.db');

$conn->exec("
CREATE TABLE pessoas(
id INTEGER PRIMARY KEY,
nome VARCHAR(40),
idade INT
)");
```

#### Inserindo conteúdo na tabela  :
```PHP
$conn->exec("
INSERT INTO pessoas(nome,idade) VALUES('Ronaldo',19);
INSERT INTO pessoas(nome,idade) VALUES('Felipe',41);
INSERT INTO pessoas(nome,idade) VALUES('Paulo',22)
");
```

## query :

### O que é : 
* Permite realizar consultas ao banco de dados, mais diferente do exec, ele **retorna valores**. 
* Útil para transformar tabelas em objetos. 
### EX :
#### Printando uma coluna especifica duma Tabela : 
```PHP
$conn = new PDO('sqlite:banco.db','','',[
	PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_OBJ
]); // fazendo conexão com um banco de dados, seu retorno no "fetch" é um "OBJ"


$query = $conn->query('
SELECT * FROM tabela
'); // "$conn->query" retorna tabela "tabela" como um "PDOStatement Object"

$query_obj = $query->fetchAll(); // "$query->fetchAll()" retorna "$query" como um objeto normal 

foreach($query_obj as $i)
{
	echo $i->nome;
} // printando dado especifico da tabela 
```


## prepare e bindParam :  
### O que é : 
* **prepare** : 
* **bindParam** :
	* É uma função do "prepare", ele permite usar **variáveis** nos comandos [[SQL]].
	* Para usar uma variável com o bindParam possui 5 parâmetros, sendo eles :
		* **var name** -> :name
		* **value** -> "Ronaldo" 
		* **value type** -> PDO::PARAM_...
			* ==Existem 3 "PARAM_...", cada um automatiza vários tipos de dados, sendo eles : ==
				* **PDO::PARAM_STR**, vale para os : 
					* VARCHAR
					* CHAR
					* STRING
				* **PDO::PARAM_INT**, vale para os :
					* INT
					* FLOAT
				* **PDO::PARAM_BOOL**, vale para os :
					* BOOLEAN
		* **dado size (opcional)**
		* **driverOptions (opcional)**

### EX : 
#### Usando uma variável do PHP para inserir um valor numa table : 
```PHP
$nome = "ronaldo";
$idade = 20;

$comando_sql = "INSERT INTO tabela(nome,idade) VALUES(:nome,:idade)"
// ":nome" é uma variável SQL, ela precisa ter seu valor definido atráves do "bindParam()"

$prepare = $conn->prepare($comando_sql); // criando prepare 

$prepare->bindParam(":nome",$nome,PDO::PARAM_STR)// variavel SQL(:nome) recebendo valor traduzido da variavel "$nome"
$prepare->bindParam(":nome",$nome,PDO::PARAM_INT)
$prepare->execute(); // executando comando SQL com as alterações feitas
``` 


