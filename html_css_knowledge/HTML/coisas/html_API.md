# O que é uma API : 
* [-- LINK --](https://www.youtube.com/watch?v=WFyHHspjS8M)
* É um sistema duma aplicação que permite com que terceiros consigam se interagir com a aplicação. Como por exemplo :
	* Caso deseje criar uma aplicação que mostre a temperatura da sua cidade, para isso, você fará o uso de alguma API de temperatura, dependendo do tipo da API você fará um [HTTP request](html_HTTP) para a API, e essa irá retornar a temperatura do jeito que você pediu.  
* Você pode criar API's ou usa-las. 
* Possui tipos, sendo eles :
	* **REST :** Utiliza o protocolo [HTTP](html_HTTP]) para se comunicar (mais utilizado). 
	* **SOAP** : Utiliza o protocolo "XML" para se comunicar. 
	* **GraphQL** : Tipo de API criado pela "META". 
* Uma API pode ser interpretada como um contrato, onde você pode fazer certas coisas seguindo a documentação da API em especifica. 

# Exemplo prático (rest) : 
* A API usada como exemplo será a "https://www.weatherapi.com/", com o objetivo de pegar a previsão do tempo , usando o "Postman" para fazer e visualizar o "GET".   
* No Postman, irá fazer uma requisição "GET" seguindo a sintaxe da API , que é : 
	* -- http://api.weatherapi.com/v1/forecast.json --
	* http://api.weatherapi.com/v1/ : URL base.
	* **forecast.json** : Request especifico que será usado .
* O request "forecast.json" pede no minimo 2 parâmetros, para colocar os parâmetros siga esta logica : 
	* **?** : Indica que está iniciando os parâmetros. 
	* **&** : Adiciona mais um parâmetro. 
* O que os parâmetros do request pedem são a "API KEY" e o nome da cidade (pode ser outras coias também), então você ira colocar no Postman : 
	* http://api.weatherapi.com/v1/forecast.json?key=aa1231dsssafaweawesq&q=Fortaleza
* Apos enviar, você poderá visualizar a resposta da API em "json" no PostMan. 


