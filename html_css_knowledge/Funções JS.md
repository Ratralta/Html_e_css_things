# Sobre Interagir com o Usuário
## window...
>  ***window.prompt***("") -->  Gera um popup na tela do usuário, que retorna o que o usuário escreveu como **string**. 
>  EX:
```js
const variavel = window.prompt("qual seu nome?") 
```

## Amostrar pro usuário :  
> **alert("Texto popup na tela")** --> Aparece um texto na tela como um popup. 
> EX:
```js
alert("BUUUUUUU")
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


# Saída de Dados  :
> **alert("Texto popup na tela")** --> Aparece um texto na tela como um popup. 
> EX:
```js
alert("BUUUUUUU")
```

> **document.write("Texto no HTML")** --> Amostra no html o que você escreveu no parâmetro. 
> EX:
```html
<h1> Em baixo de mim tem um texto escrito com JS </h1>
<u> <!-- O dado que saiu do document.write está dentro desta tag "<u>" -->
<script>
    document.write("Sou escrito com JS")
</script>
</u>
```

> **console.log("Esse texto tá no console")** --> Escreve o que você colocou no parâmetro NO "console".
> EX:
```js
let calculo = 5 * 3;
console.log("O calculo resultou em " + calculo);
```
