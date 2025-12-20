# O que é :
* O php é uma linguagem de programação voltada para servidores, além de possuir fácil integridade com [[HTML]]. 
* Para começar a usar o php, você precisa ter um [servidor web.](html_servidor_web) 

# Coisas Básicas : 
## [-- Como usar o PHP --](php_como_usar_php) 

## Coisas verdadeiramente básicas :
* Para utilizar o PHP, você precisa com o "XAMPP" ligar o "Apache".
* Seu arquivo precisa ser da extensão "php", não funciona caso seja "html".  
* TODAS as variáveis do php começam com "$"
* A seta "->", serve para acessar variáveis de um objeto E chamar funções dentro de um objeto



## Variáveis :
### Criando variáveis :
* Todas as variáveis do php iniciam com "$".
* EX:
	```PHP
	<?php
	$nome = "Ronaldo";
	$sobre_nome = "Silva";
	echo "Ola, meu nome é $nome e meu sobre nome é $sobre_nome"
	?>

	```
### Citando variáveis : 
* Existem 2 maneiras de retornar o valor de alguma variável, sendo eles : 
	* Simplesmente escrevendo seu nome : 
		```PHP
		$nome = "Ronaldo";
		echo "Meu nome é $ronaldo";
		```
	* Ou colocando o "$" com a variável entre coxetes (Útil caso ocorra algum problema de sintaxe) :
		```PHP
		<?php
		$lista = [
		"nome" => "Ronaldo",
		"idade" => 19,
		];
		echo "Meu nome é ${lista["nome"]} e tenho ${lista["idade"]} de idade";
		?>
		``` 


### Variáveis referenciadas : 
* No php, é possível fazer uma variável referenciar outra, significando que toda mudança na variável referenciada, afetará a variável que referenciou, e vice versa.
* Para isso, basta colocar "&" e a variável que irá ser referenciada.
* Nesse tipo de variável, ela não aceita nenhum outro valor além da variável referenciada. 
* EX:
	```php
	<?php
	$idade = 19;
	$idade_do_user = &$idade;

	$idade = 67;
	echo "A idade do usuario é $idade_do_user";
	// RETORNA = A idade do usuario é 67
	?>
	```
## Vetores :
### Arrays :
#### Criando Arrays : 
* [-- LINK --](https://www.php.net/manual/en/language.types.array.php)
* Sua sintaxe de array não muda muita coisa em relação as outras linguagens. 
* Para printar arrays, use a função ==var_dump($lista)==.
*  No PHP, você pode criar arrays utilizando dum sistema de **Key** e **valor**, aonde você define a "key" para acessar seu "valor", ao invés de definir somente o "valor" para a array. 
* Caso você não defina uma **key**, a "key" dela seguira o padrão das outras linguagens (0,1,2...) 
* Existe **duas** sintaxes para criar uma array, sendo :
	* Assim :
	```PHP 
	// criando normalmente : 
	$lista_de_nomes_normal = array("Ronaldo","Felipe");
	
	// usando key e valor :
	$lista_de_nomes = array(  
	1 => "Ronaldo",  
	2 => "Felipe",  
	);
	```
	* Ou assim :
	```PHP
	// criando normalmente : 
	$lista_de_nomes_normal = ["Ronaldo","Felipe"];
	
	// usando key e valor :
	$lista_de_nomes = [
	1 => "Ronaldo",
	2 => "Felipe",
	];
	```
* Um exemplo usando array mais complexo :
	```PHP 
	<?php
	$var = 3;
	
	$lista = [
	1 => 1, 
	2 => "Ronaldo",
	"Tres" => $var
	];
	echo "$lista[1] <br>";
	echo "$lista[2] <br>";
	echo "${lista["Tres"]} ";
	?>
	```
#### Funções básicas sobre arrays :
* Printar alguma array :
	* **var_dump($lista)** : Ela printa a array amostrando suas **keys** e seus **valores**. 
* Amostrar quantos itens existem na array :
	* **sizeof($array)** : Retorna como numero inteiro a quantidade de itens existem na array.
* Adicionar um novo item a array :
	* **array_push($lista, $valor)** : Adiciona um novo item a lista no ultimo andar. 
* DELETAR :
	* Deletar o primeiro item da lista :
		* **array_shift($array)** : Remove o primeiro item da lista.
	* Deletar o ultimo item da lista : 
		* **array_pop($array)** : Remove o ultimo item da lista. 
	* Deletar um item especifico da lista : 
		* **unset(\$array\[$key])** : Remove um item especifico da lista. Quando deletado, não organiza a ordem dos itens da lista, para ajustar a ordem, use a função ==array_values(\$lista)==. 
* Ajustar a posição dos itens da array : 
	* **$lista =  array_values(\$lista)** : Essa função retorna uma array com os itens organizados da array de seu parâmetro.


## Class e objetos : 

# Mexendo com bancos de dados : 
## [[MySQL]] : 



