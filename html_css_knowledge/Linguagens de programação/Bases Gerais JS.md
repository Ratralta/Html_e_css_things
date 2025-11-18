# Coisas Básicas
## Coisas verdadeiramente básicas 
*  Para inserir conteúdo dentro de uma tag html, basta usar o **método de variável**  "innerHTML", fazendo algo como :  ==tag_variavel.innerHTML = "lorem ipsolon dolor"==.

*  No check de condições, para checar se é "igual", usa "\=\=\=".

*  Tudo que foi escrito no JS, só vai ser lido UMA vez.

*  Para adicionar um código javascript no html, você pode usar a tag "\<script>", e usar a propriedade 'src="pasta/arquivo.js"', assim você "importa" o código.
EX: \<script src="pasta/arquivo.js">\</script>

* É possível criar objetos no javascript SEM precisar de um CLASS. 

* Para pegar uma variável dentro de um bloco de string, use " `${variavel}`.

* Quando você usa  \`\` ,  tudo dentro dele funciona como uma string.

* O JavaScript consegue ler as tags do HTML, o jeito que ele as ler é como se fossem "objetos", podendo rodar funções neles através do ponto(.). O documento html também é lido como objeto, então você consegue pegar tags especificas somente com o ponto(.)
EXEMPLO :
```js 
let titulo_do_site = document.title;
document.write("O titulo do site é : " + titulo_do_site);
// document.title PEGA a tag <title>, os dados que ela no caso é somente o que tem escrito nele.
```


## Criando Variáveis 
### Palavras-chaves da variável :
-- Na hora de criar uma variável, você **pode** definir 3 palavras-chaves, que são :
>***CONST*** : Valor constante que nunca muda.
>EX: 
```js
const nome_da_pessoa = "Willian";
nome_da_pessoa = "Zilian";
console.log(nome_da_pessoa); // RETORNA : "Willian" --> string 
```

>***VAR*** : Cria uma variável local, essa variável pode ser redeclarada diversas vezes (Use "let" ao invés desse). 
>EX:
```js
var bixo = "sou texto";
var bixo = 455;
console.log(bixo) // RETORNA : 455 --> int
```

>***LET***: Cria uma variável local, ela não pode ser redeclarada (Recomendado de usar ao invés do "var").
>EX:
```js
let bixo = 455;
bixo = "sou texto"; 
console.log(bixo) // RETORNA : "sou texto" --> string
```

### Características : 
-- Se você tentar somar uma **string** com um **int/float**, tudo vai aparecer como se fosse string.
EX: 
```js 
let texto = "sou texto";
let numero = 67;
console.log(texto+numero) // RETORNA : "sou texto67" --> string 
```

-- Você pode definir varias variáveis sem colocar seu valor.
EX: 
```js
let var_a,var_b,var_c; // criou essas 3 variaveis.
var_b = 10; // atribui-o  valor a uma delas.
console.log(var_b); 
```

## Criando Vetores : 
### Arrays : 
Para criar um array, é só usar "new Array(5)" e atribuir em uma variável. 
EX: 
```js 
let meuVetor = new Array(5); 
console.log("essa array possui " + meuVetor.length + " itens");
```



## Class :
### Criando Class :
* Para criar um class, é possível seguir uma logica similar ao do **C#**, aonde você usa uma palavra chave let/var, define o nome e iguala ela a uma class do nome que você deu a ela. Como no exemplo : 
~~~js
 let Retangulo = class Retangulo
{
	altura = 9;
    largura = 15;
};
~~~

* Para usar constructor é desse jeito : 
~~~js
let Retangulo = class Retangulo 
{
	constructor(altura, largura) 
	{
	this.altura = altura;
	this.largura = largura;
	}  
};
~~~

### Palavras chaves duma Class : 
#### Static : 
* Colocada em funções duma classe, ela é igual ao static de **C#**, permite com que uma função possa ser chamada SEM PRECISAR instanciar um objeto a class. 

# Pegando Tags do HTML e lendo no JS : 
## Pegando pela ID :
--- Para pegar uma tag pelo atributo "ID" dela, com o objeto "document", use a função  "getElementById()" e coloque no parâmetro entre aspas a "ID" da tag que você quer. 
EX:
```html
<!-- DENTRO DE UM BODY -->
<h1> TITULO </h1>
<p id="texto"> </p> <!-- Vai escrever algo atraves do JS -->
<p id="outro_texto"></p>

<script>
    let texto_do_html = document.getElementById("texto"); // pegando a tag <p> com id "texto"
    texto_do_html.innerHTML = "lorem ipsolon dolor" // inserindo conteudo para a tag com id "texto"
</script>
```
> \<script> ---> Tag para abrir uma área de código JavaScript.
> document ---> É o "objeto" da sua pagina html, que contem as suas tags.
> document.getElementById("texto") ---> Pegando a tag com a id "texto".
> innerHTML ---> Inserindo conteúdo html para essa tag. 

## Pegando pela Class :
--- FE

## Pegando através de um FORM : 
* No seu form, você vai precisar :
	* Definir um atributo "methed", que a maneira que ele vai mandar o form (GET ou POST).
	* Aonde ele vai mandar o form, através do atributo "**action = "arquivo.html"**".
	* Somente os inputs com o atributo "name", serão guardados no form.
	* EX :  
	 ```html
	  <!DOCTYPE html>
		<html>
			<form action="home.html" method="GET">
				<input type ="text" name="user_nome">
				<input type ="passowrd" name="user_senha">
			</form>
		</html>
	  ```

* Agora, no seu JavaScript, uma maneira de pegar os dados enviados ao seu arquivo html (muito parecido com o PHP), é usando o objeto especial **"URLSearchParams(window.location.search)"** ele permite retornar como um objeto, **o formulário que foi enviado ao seu html**. Para retornar as informações desse objeto do formulário, você usa ".get" ou ".post".  

* EX: 
```html 
<!-- ARQUIVO "home.html" -->
<html>

<h1 id="retorno"></h1> 

<script>
const form_objeto = new URLSearchParams(window.location.search) 
// "URLSearchParams(window.location.search)" retorna como objeto o form recebido. 
// "form_objeto" é um objeto que possui os dados do form recebido.

let nome_do_user = form.get("user_nome"); // retorna valor de "user_nome"
let senha_do_user = form.get("user_senha"); // retorna valor de "user_senha"
document.getElementById("retorno").innerHTML = nome_do_user + "<br>" + senha_do_user
</script>
</html>
```