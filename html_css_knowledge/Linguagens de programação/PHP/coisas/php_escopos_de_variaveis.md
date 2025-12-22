# O que é : 
* É aonde e como utilizar variáveis em diversos locais. 
* [-- LINK --](https://www.php.net/manual/pt_BR/language.variables.scope.php).
# Escopos : 
* ==Global== : Tudo fora das chaves "{}".  
* ==Local== : Tudo dentro das chaves "{}", como **Classes**, **funções** etc. 
# Exemplos : 
## Usar variável no escopo global em uma função : 
* Se uma função tentar usar qualquer coisa que está no **escopo global**, ela não irá conseguir.  
* Para fazer isso, você precisará usar da palavra chave **"global"** na variável do escopo global que você deseja.
* EX: 
```PHP 
$nome = "Ronaldo"; // variável no escopo global 

function falar()
{
global $nome; // resgatando variável "$nome" para um escopo local.
echo "Meu nome é $nome";
} 

falar();
```
## Usar variável do escopo global em um class :
* Em um class, caso você tente usar um **"global"** para resgatar uma variável do escopo global e coloca-ló num local, isso não será possível. 
* O "global" funciona somente dentro de funções, então se fizer o mesmo numa função de um class irá funcionar. 
* Exemplo funcional :
```PHP
	$variavel = "Valor"; // variável no escopo global
	class pessoas
	{
		function printar()
		{
		global $variavel; // variável no escopo global resgatada para este local 
		echo $variavel;	
		}
	}
	$objeto = new pessoas(); // objeto 
	$objeto->printar();
```
* Exemplo NÃO funcional :  
	```PHP
	$variavel = "Valor"; // variável no escopo gloval
	class pessoas
	{
	global $variavel; // NÃO FUNCIONA, não é possivel resgatar um valor do escopo gloval e coloca-lo num class. 
		function printar()
		{
		echo $variavel;	
		}
	}
	$objeto = new pessoas(); // objeto 
	$objeto->printar();
	```
