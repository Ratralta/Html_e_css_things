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
> **parseInt/parseFloat(valor,Opicional)** --> Ele ler o valor recebido da esquerda para direita, parando quando detecta uma letra, **ele retorna os números lidos como int/float**. 
> EX:
```js
let texto = "1000 coisas"
let texto_int = parseInt(texto) // RETORNA --> 1000 int
console.log(texto_int);
console.log("Letra 455"); // RETORNA --> NaN
```


# Métodos dos Objetos :
## VARIÁVEL  : 
* ***variavel.charAt(3)*** --> Função ligada a alguma string, RETORNA como string a posição do texto que você colocou no PARÂMETRO. 
	EX: 
	```js
	let texto = "sou um texto";
		for(var i=0;i<texto.lenght;i++)
		{
		document.write(texto.charAt(i));
		}
	```

* **variavel.replace(/\[^0-9.]/g,"")** --> Retorna o valor de "variavel", substituindo o que está no primeiro parâmetro da função, pelo o que está no segundo parâmetro da função.  
	 O primeiro parâmetro possui algumas palavras chaves, para usa-las use as barras (**//**) ao invés de espaço, as palavras chaves são :  
	 ---- (/x/**g**) --> substitui globalmente a letra dentro das barras ("g" precisa está fora das barras).
	 
	 ---- (**\[^a-z.]**) && (**\[^0-9.]**)--> substitui **TODOS** que não são entre os valores colocados dentro das barras. No caso o primeiro exemplo tira **todos que não são letras**, o segundo exemplo tira **todos que não são números**. 
	 EX: 
	```js
	fruta = "banana";
	fruta = fruta.replace("a","u");
	console.log(fruta); // RETORNA --> bunana
	```

* variavel.split(" ") --> Retorna uma variável de **texto** numa **array**, usando como critério de separação o que você colocou no parâmetro (entre aspas), pode receber um segundo parâmetro , ele que faz com que a array retornada tenha a quantidade de itens colocado nele.
	EX: 
	```js
	let nome = "Ronaldo Felipe Jr"
	let nome_array = nome.split(" ") // critério de separação é o espaço (" ")
	console.log(nome_array) // printou a array "nome_array"
	```
## [-- window --](Objetos_JS)  

# Funções de Bibliotecas  : 
## Data, hora e mês : 
------ **Para pegar dados como data , hora e ETC,  da para criar um objeto especial com JS, e usar funções nele.**
```js
// CRIANDO OBJETO DO TEMPO
tempo = new Date();
document.write(tempo) // isso vai amostrar todas as informações sobre o tempo.
```

------ FUNÇÕES :



## Math :
------  Possui funções relacionadas a números.

>  ***Math.random***() --> Gera um numero  aleatório , que é real e menor que 1.  
>  EX:
```js
let numero_aleatorio = Math.round(Math.random() * 100); // gera numero aleatorio E arredonda ele.
console.log(numero_aleatorio); // printa o numero no console
```

>  ***Math.round***(variavel) --> Arredonda o numero "variavel". 
>  EX:
```js
let numero_aleatorio = Math.round(Math.random() * 100); // gera numero aleatorio E arredonda ele.
console.log(numero_aleatorio); // printa o numero no console
```

> **Math.max(var_1,var_2) && Math.min(var_1,var_2)** --> Math.max retorna o maior número dentro de seu parâmetro,  Math.min retorna o menor valor dentro de seu parâmetro. 


# Coisas Uteis : 
> ***isNaN(valor)*** --> Função que retorna True ou False CASO o "valor" seja um NaN. 
> EX: 
```js
let variavel = parseInt("lá ele"); // retorna NaN

if (isNaN(variavel)) // se "variavel" for NaN
{
console.log("erro")
}
```