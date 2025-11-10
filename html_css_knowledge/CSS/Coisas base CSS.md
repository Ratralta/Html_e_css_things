# Dicas :
## Coisas
- /* texto comentário\*/ : É assim que deixa um comentário no CSS.
- O html **já vem** com algumas configurações de css.  
## Medidas : 
As medidas que existem e como elas funcionam : 
* px : Se baseia em pixels.
* vw : Ele ocupa porcentagem da tela, diferente do "%", ele se ajusta com o tamanho do site.


## Variáveis : 
Para criar uma variável, você usa "--" , depois o nome da variável, e dois ponto com seu valor.
EX: --variavel : 35;

Para chamar ela use "var()", assim retorna o valor dela.
EX :
```css
.sou_class{
--variavel : 35;
background-color : rgb(0,0,var(--variavel))
}
```

Para criar uma variável global, defina ela dentro de um ":root", esse ":root" é a base, literalmente é o a tag "\<html>" do arquivo.
EX : 
```css
:root {
--sou_variavel_global : black
}
```

## Objeto html : 
* ***Objeto html*** é um termo que eu **inventei**, ele se refere a quando você mexe em alguma tag/class/id do html **no css**.
* EXEMPLO: 
![[objeto_hrml.png]]
## Atributo : 
* ***A*tributo*** é um termo que eu **inventei**, ele se refere aos atributos que você coloca em um ***objeto html***. 
* EXEMPLO : 
![[Atributo.png]]
# Mexendo nas Class e Ids : 
## Como mexer nas Class e Id :
- Div serve para organizar coisas outras tags para serem mexidos no html.

- Para pegar um ID no CSS, use "#id_name".
-  Para pegar um CLASS no CSS, use ".class_name".
-  Para pegar uma TAG QUALQUER, só coloque o a tag.

- Se você usar um asterisco "\*", o css vai mexer em todo o arquivo html.

## Como alinhar os itens de um class : 
- Para usar propriedades de alinhar como "align-items" e entre outros, use antes, a propriedade  "display: flex;", e escolha um tipo (como "flex", "grid" etc) para ativar elas.

-  A propriedade "align-algumacoisa", alinha os itens de sua classe VERTICALMENTE.

- A propriedade "justify-algumacoisa", alinha os itens de sua classe HORIZONTALMENTE.

- Se você quiser centralizar um "block", que é uma área demarcada por uma \<div>, você pode usar "margin: 0 auto", que vai automaticamente centralizar seu "block" no centro da pagina.

* A propriedade "margin-algumacoisa", mexe o item em **alguma direção em pixels** (ou outras medidas)  

# Animation : 
## TAG\:hover : 
* Quando você citar um objeto do html, e colocar ":hover", as alterações do css SOMENTE serão aplicadas quando o mouse passa por cima do objeto html.  


