# Coisas Básicas
## Coisas verdadeiramente básicas 
-- No check de condições, para checar se é "igual", usa "\=\=\=".

-- Tudo que foi escrito no JS, só vai ser lido UMA vez.

-- Para adicionar um código javascript no html, você pode usar a tag "\<script>", e usar a propriedade 'src="pasta/arquivo.js"', assim você "importa" o código.
EX: \<script src="pasta/arquivo.js">\</script>

-- Para pegar uma variável dentro de um bloco de string, use " `${variavel}`.

-- Quando você usa  \`\` ,  tudo dentro dele funciona como uma string.

-- O JavaScript consegue ler as tags do HTML, o jeito que ele as ler é como se fossem "objetos", podendo rodar funções neles através do ponto(.). O documento html também é lido como objeto, então você consegue pegar tags especificas somente com o ponto(.)
EXEMPLO :
```js 
let titulo_do_site = document.title;
document.write("O titulo do site é : " + titulo_do_site);
// document.title PEGA a tag <title>, os dados que ela no caso é somente o que tem escrito nele.
```
## Criando variáveis 
-- Na hora de criar uma variável, ela pode ter 3 tipos.
const : Valor constante que nunca muda.
var : Cria uma variável.
let : Cria uma variável local.



# Pegando Tags e Classes do HTML : 
## Class :
