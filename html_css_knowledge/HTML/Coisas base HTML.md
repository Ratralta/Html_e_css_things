# Dicas :
## Coisas :
-  \<!-- --> : É assim que deixa um comentário no HTML.

-  a tag \<p>, é um boa tag se você quiser escrever algum texto E guardar ele dentro de uma tag.

-  com a tag \<a> e o atributo <href ="link/arquivo">, você faz com que quando a tag for clicada, direcione o usuário para o "href"

-  Lembre de no input, colocar uma "ID", pois com ela é possível pegar seu valor e retorna-lo para ser usado alguma linguagem de programação.

* Com o atributo "onClick ="funcao()" ", você chama uma função existente do [javascript](JavaScript.md).



# Form 
## O que um form :
Para mandar dados para um outro arquivo, é preciso fazer uso da tag \<form>.
A tag "form" cria uma área onde vai armazenar os dados das tags \<input> colocadas pelo usuário, para criar ele precisa principalmente dos atributos  :
> action --> local do arquivo que você quer mandar os dados.
> method = "post **OU** get" --> como ele vai mandar esses dados. ("post" é mais protegido)
> name --> qual é seu nome para ser pego usando alguma linguagem de programação

EX DE FORM E INPUT : 
```html 
<form action="/outro_arquivo" method="post" name="cadastro">
	<p> Coloca seu nome ai </p>
	<input type="text" name="nome_do_usuario"> 
	<input type="submit"> 
</form>
```

EX O QUE APARECE NO SITE :
<form action="/outro_arquivo" method="post" name="cadastro">
	<p> Coloca seu nome ai </p>
	<input type="text" name="nome_do_usuario"> 
	<input type="submit"> 
</form>
## Tipos de input :
### De escolha : 
#### Radio 
Input de escolha com itens, **você só pode escolher um** dos itens determinados por você.   
EX:
ESCRITO NO HTML :
****
```html
<p> Qual sua comida favorita ? </p>
<input type="radio" name="comida" value="lasanha" checked> Lasanha </input>
<input type="radio" name="comida" value="wingslompson"> Wingslompson</input>
<input type="radio" name="comida" value="tapioca"> Tapioca </input>
```
****
APARECE NO SITE :
****
<p> Qual sua comida favorita ? </p>
<input type="radio" name="comida" value="lasanha" checked> Lasanha 
<input type="radio" name="comida" value="wingslompson"> Wingslompson
<input type="radio" name="comida" value="tapioca"> Tapioca 
****
> input type --> Tipo do input  
> name --> De qual "input radio" esse input pertence. (Qual é seu pai) 
> value --> Valor que vai retornar no ***submit*** CASO você clique nele  

#### Checkbox 
Input de seleção de itens, **você pode escolher quantos itens você quiser**.
EX:
ESCRITO NO HTML:
****
```html
<p> Quais características você tem? </p>
<input type="checkbox" name="caracteristicas" value="forte"> Forte </input>
<input type="checkbox" name="caracteristicas" value="rapido"> Rapido </input>
<input type="checkbox" name="caracteristicas" value="smart"> Smart </input>
```
****
APARECE NO SITE:
****
<p> Quais características você tem? </p>
<input type="checkbox" name="caracteristicas" value="forte"> Forte 
<input type="checkbox" name="caracteristicas" value="rapido"> Rapido 
<input type="checkbox" name="caracteristicas" value="smart"> Smart 
****
  >input type --> Tipo do input  
> name --> De qual "input checkbox" esse input pertence. (Qual é seu pai) 
> value --> Valor que vai retornar no ***submit*** CASO você clique nele  
#### Select && Opition 
"Input" de seleção que quando clica nele , aparece diversos itens, você só pode escolher um item. 
EX:
ESCRITO HTML:
****
```html
<p> Qual seu animal favorito ? </p>
<select name="animais">
	<option value="gato"> Gato </option>
	<option value="cachorro"> Cachorro </option>
	<option value="humano"> Humanos </option>
	<option value="dragao_de_komodo"> Dragão de Komodo </option>
</select>
```
****
O QUE APARECE NO SITE:
****
<p> Qual seu animal favorito ? </p>
<select name="animais">
	<option value="gato"> Gato </option>
	<option value="cachorro"> Cachorro </option>
	<option value="humano"> Humanos </option>
	<option value="dragao_de_komodo"> Dragão de Komodo </option>
</select>
****

> select name --> Criando uma área "select", com o atributo "nome" único deste select 
> option --> Um item que você pode escolher no "select"
> option value --> O valor que vai retornar no ***submit*** caso esse "option" seja clicado. 
### De preencher texto : 
### De Texto :
Input que cria uma área de escrever o texto, **retorna no submit o que você escreveu**.
EX: 
ESCRITO NO HTML:
****
```html
<p> Coloque seu nome</p> 
<input type="text" name="nome_da_pessoa"> </input>
```
****
O QUE APARECE NO SITE:
****
<p> Coloque seu nome</p> 
<input type="text" name="nome_da_pessoa"> 
****
> input type --> Tipo do input  
> name --> Nome desse input, que serve para identifica-lo, e conseguir pegar seu valor em outros arquivos (caso tenha dado **submit**)



## Atributos de inputs
* **onblur ="funcao_js()"** ---> Executa o código dentro dele APÓS o usuário tiver clicado em um input , e depois clicar fora dele. 

* **onclick = funcao_js()** ---> Executa o código dentro dele APÓS clicar na tag com esse atributo.

* **required** ---> Faz o input com esse atributo seja obrigatório ser preenchido para dar "submit".



# HTPP : 
* [LINK SOBRE GET,FORM E HTPP](https://www.alura.com.br/artigos/diferencas-entre-get-e-post?utm_term=&utm_campaign=&utm_source=google&utm_medium=cpc&campaign_id=23211518344__&utm_id=23211518344__&hsa_acc=7964138385&hsa_cam=&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=google&hsa_ver=3&gad_source=1&gad_campaignid=23211519973&gbraid=0AAAAADpqZIBwpm62DOpA_jHWnEoP5jtT3&gclid=CjwKCAiA24XJBhBXEiwAXElO39ECAdipzvOW1wOMK8xJz92bvO8QcWNabCA3Jnh7pGN1x37jsPWMgRoCNYgQAvD_BwE)
## O que é : 
* Quando você está usando algum site, constantemente acontece uma conversa entre o navegador do usuário e o servidor. 
* O que conduz essa conversa entre ambos é o HTPP.
* Ele possui 2 métodos principais, o **GET**, e o **POST**. 

## Método GET : 
* O método(função) get é usado pelo navegador do usuário, ele **solicita** ou **recupera dados** do servidor, é possível também com o get acionar funções do servidor, porem requer certas maracutaias.
* Tudo que o navegador pede para o servidor (através do método GET) é mostrado na URL do navegador, é chamado de [query string](html_query_string)
* As informações amostradas no URL do navegador seguem está sintaxe :
	* variavel=valor&outra_variavel=outro_valor
* EX : 
	* No Google, quando você pesquisa alguma coisa, você está preenchendo um formulário, quando você envia você faz um "commit".
	* Ao enviar, seu navegador através do GET pede ao servidor o dado da sua pesquisa, isso pode ser provado assim : 
		* URL da pesquisa : https://www.google.com/search?q=gato&rlz=1C1GCEA_enBR1131BR1131&oq=gato&gs_lcrp=EgZjaHJvbWUqBwgAEAAYjwIyBwgAEAAYjwIyCggBEC4YsQMYgAQyEAgCEC4YxwEYsQMY0QMYgAQyCggDEC4YsQMYgAQyDQgEEC4Y1AIYsQMYgAQyDQgFEC4Y1AIYsQMYgAQyCggGEAAYsQMYgAQyCggHEC4YsQMYgAQyCggIEC4YsQMYgAQyCggJEAAYsQMYgATSAQk3NDMyajBqMTWoAgCwAgA&sourceid=chrome&ie=UTF-8
		* "https://www.google.com" é o endereço do servidor.
		* "search?" é uma função do servidor
		* "q=gato" é uma variável, que nesse caso, é um parâmetro da função "search?"
		* O resto são outras variáveis.

## Método POST : 
* O método(função) get é usado pelo navegador do usuário, ele **solicita** ou **recupera dados** do servidor, é possível também com o get acionar funções do servidor, porem requer certas maracutaias.
* O método(função) post é usado pelo navegador do usuário, ele envia