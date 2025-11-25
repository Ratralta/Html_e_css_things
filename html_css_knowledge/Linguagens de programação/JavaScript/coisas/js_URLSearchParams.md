# O QUE É :
* Ele é uma classe do javascript
* Serve para ler os [query string](html_query_string) de uma maneira mais fácil, sendo também capaz de transforma-los em objetos.  

# Como faço pra transformar um query string em objeto usando o URLSearchParams :
* Para isso, guarde em uma variável, um URLSearchParams do [query string](html_query_string). 
	* EX : 
		* URL : http://127.0.0.1:5500/check.html?nome=12&senha=12&submit=entrar
		* CÓDIGO  : query_string_legivel = new URLSearchParams(window.location.search) 
* Agora, crie uma outra variável, use a class "Object", com a função "fromEntries", recebendo como parâmetro "query_string_legivel.entries()".
	* EX:
		* CÓDIGO : const objeto = Object.fromEntries(query_string_legivel.entries())
* O resultado final fica :
	* CÓDIGO :
	 ```js
	   query_string_legivel = new URLSearchParams(window.location.search)
	   // cria uma versão legivel do "query string"
	   // "query_string_legivel" é um class 
	   
	   objeto = Object.fromEntries(query_string_legivel.entries())
	   // transforma a class "query_string_legivel" em um objeto
	   ```
	 