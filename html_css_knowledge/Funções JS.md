# ==Saída de Dados== :
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







# ==Entrada de Dados :==
> **parseInt/parseFloat(valor,Opicional)** --> Ele ler o valor recebido da esquerda para direita, parando quando detecta uma letra E retornando os números lidos como int/float. 
> EX:
```js
let texto = "1000 coisas"
let texto_int = parseInt(texto) // RETORNA --> 1000 int
console.log(texto_int);
console.log("Letra 455"); // RETORNA --> NaN
```


# Relacionado a valores de variáveis :
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



## Interagir com o usuário : 
### window...
>  ***window.prompt***("") -->  Gera um popup na tela do usuário, que retorna o que o usuário escreveu como **string**. 
>  EX:
```js
const variavel = window.prompt("qual seu nome?") 
```




# Coisas Uteis : 
> ***isNaN(valor)*** --> Função que retorna True ou False CASO o "valor" seja um NaN. 
> EX: 
```js
let variavel = parseInt("lá ele");

if (inNaN) // se for true 
{
console.log("Deu erro");
}

```