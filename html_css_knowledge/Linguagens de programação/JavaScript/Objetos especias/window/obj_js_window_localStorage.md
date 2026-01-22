* [LINK DE EXPLICAÇÃO](https://www.youtube.com/watch?v=rCnC-yfZprM)
# Informações : 
* As informações do localStorage ficam salvas no [browser](html_diferenca_entre_pagina_web_site_servidor_web_e_mecanismo_de_busca) do usuário, significa que mesmo que o usuário saia, as informações ainda serão guardadas. 
* O jeito que é guardado os dados é em formato de "Item", onde através do nome do item, eu consigo acessar os valores dele. 
* Tudo armazenado dentro dele será uma "string".
# Funções : 
* **setItem(item_name, value)** --> Adiciona uma novo item para o "localStorage", com o nome "key_value" e de valor "value" 
	EX:
	```js
	let nome = "Ronaldo";
	window.localStorage.setItem("Nome do user",nome) 
	// agora no localStorage do seu dominio, possui a key "Nome do user" de valor "Ronaldo"
	```
	
* **getItem(item_name)** --> Retorna o valor do item "item_name".
	EX: 
	```js
    window.localStorage.setItem("User","Não gosta de fruta"); 
    // adicionando um item no "localStorage".
    // o nome do item é "User"
    const valor = window.localStorage.getItem("User") // pegando valor do item "User"
    console.log(valor)
	```
	
* **removeItem(item_name)** --> Remove do localStorage o item "item_name". 
	EX: 
	```js
	window.localStorage.setItem("User","123456789") // criando item pro localStorage
	const user_senha = window.localStorage.getItem("User") // retornando valor do item criado
	window.localStorage.removeItem("User") // deletando item do localStorage 
	console.log(user_senha) // printando variavel "user_senha"
	```
	
* **clear()** --> Deleta todos os itens do localStorage. 
	EX: 
	```js
    window.localStorage.setItem("User1","caua"); // criando vários itens
    window.localStorage.setItem("User2","ronaldo");
    window.localStorage.setItem("User3","felipe");
    window.localStorage.setItem("User4","skarner");

    const users = new Array(4); 

    for(i=0;i<users.length;i++) // colocando todos os itens numa array
    {
    let user_especifico = "User" + (i+1);
    console.log(user_especifico)
    users[i] = window.localStorage.getItem(user_especifico);
    }
    window.localStorage.clear(); // deletando todos os itens 
    console.log(users); // pritando array
	```
