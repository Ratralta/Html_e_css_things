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

# Animações : 
## Atributo "animation" : 
### Como funciona : 
* O atributo "animation" serve para usar um **"keyframe"** e aplicar alguns modificadores para mudar o jeito que a animação ocorrerá. 
* O **keyframe** é o que a animação irá fazer.
	* Exemplo de criação de um keyframe : 
		```CSS
		@keyframe animacao { /* nome do keyframe*/
			from { /* a animação irá começar com isso : */
			opacity : 1;
			}
			to { /* irá terminar com isso */
			opacity : 0;
			}
		}
		```
* "animation" precisa de no minimo 2 parâmetros :
	* nome do "keyframe". 
	* tempo que irá durar. 

### Exemplo pratico : 
```CSS
@keyframe texto_sumir { /* nome do keyframe */
	from {
	opacity : 1;
	}
	to {
	opacity : 0;
	visibility: hidden; /* torna a tag inutilizável */
	}
	
	p { /* mexendo na tag "<p>" */
	animation : texto_sumir 1s linear forwards;
	/* "linear" --> mexe na fluidex da animação  */
	/* "forwards" --> faz com que a animação não seja um loop */ 
	animation-delay : 1s;
	/* "animation-delay" --> Tempo que a animação irá começar */ 
	}
}
```
### Modificadores para "animation" : 
* Fazer com que a animação NÃO seja um loop : 
	* ==forwards== 

### Atributos relacionados a "animation" :
* Fazer a animação começar a partir de algum tempo : 
	* ==animation-delay : 1s== 


## Condições de ativação de CSS: 
### Mouse : 
* Passando o mouse na tag e ativando CSS : 
	* ==:hover== :  Quando você citar um objeto do html, e colocar ":hover", as alterações do css SOMENTE serão aplicadas quando o usuário passa o mouse passa por cima do objeto html.  
	* EX :
		```css
		#cancel:hover{
		transition: 0.3s; /*tempo para aplicar as alterações  */
		background-color: #3a3b3d;
		cursor :pointer; /*mudando ponteiro do mouse para "pointer" */
		}
		```




