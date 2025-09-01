# Dicas :
## Coisas :
-  \<!-- --> : É assim que deixa um comentário no HTML.

-  a tag \<p>, é um boa tag se você quiser escrever algum texto E guardar ele dentro de uma tag.

-  com a tag \<a> e o atributo <href ="link/arquivo">, você faz com que quando a tag for clicada, direcione o usuário para o "href"

-  Lembre de no input, colocar uma "ID", pois com ela é possível pegar seu valor e retorna-lo para ser usado alguma linguagem de programação.

* Com o atributo "onClick ="funcao()" ", você chama uma função existente do [javascript](JavaScript).



# Tipos de input :
## De escolha : 
### Radio 
Input de escolha com itens, **você só pode escolher um** dos itens determinados por você.   
EX:
ESCRITO NO HTML :
****
```html
<p> Qual sua comida favorita ? </p>
<input type="radio" name="comida" value="lasanha"> Lasanha </input>
<input type="radio" name="comida" value="pao"> Pão</input>
<input type="radio" name="comida" value="tapioca"> Tapioca </input>
```
****
APARECE NO SITE :
****
<p> Qual sua comida favorita ? </p>
<input type="radio" name="comida" value="lasanha"> Lasanha 
<input type="radio" name="comida" value="pao"> Pão
<input type="radio" name="comida" value="tapioca"> Tapioca 
****
> input type --> Tipo do input  
> name --> De qual "input radio" esse input pertence. (Qual é seu pai) 
> value --> Valor que vai retornar no ***submit*** CASO você clique nele  

### Checkbox 
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
### Select && Opition 
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
## De preencher texto : 
### Text 
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

