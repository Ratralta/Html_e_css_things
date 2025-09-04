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

-- O JavaScript ler tags do html.
## Criando variáveis 
-- Na hora de criar uma variável, ela pode ter 3 tipos.
const : Valor constante que nunca muda.
var : Cria uma variável.
let : Cria uma variável local.

## Pegando Tags do HTML e lendo no JS : 
### Pegando pela ID :
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
> innerHTML ---> Inserindo conteúdo html para essa tag. 