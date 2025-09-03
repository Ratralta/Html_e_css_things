# Sobre Interagir com o Usuário
## window...
>  ***window.prompt***("") -->  Gera um popup na tela do usuário, que retorna o que o usuário escreveu como **string**. 
>  EX:
```
variavel = window.prompt("qual seu nome?") 
```






# Mexer nas variáveis :
## String : 
> ***texto.charAt(3)*** --> Função ligada a alguma string, RETORNA como string a posição do texto que você colocou no PARÂMETRO. 
> EX: 
```js
let texto = "sou um texto";
	for(var i=0;i<texto.lenght;i++)
	{
	document.write(texto.charAt(i));
	}
```


# Coisas legais : 
## Data, hora e mês : 
------ **Para pegar dados como data , hora e ETC,  da para criar um objeto especial com JS, e usar funções nele.**
```js
// CRIANDO OBJETO DO TEMPO
tempo = new Date();
document.write(tempo) // isso vai amostrar todas as informações sobre o tempo.
```

------ FUNÇÕES :
> 