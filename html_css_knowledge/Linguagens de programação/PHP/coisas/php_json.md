# O que é : 
* Java Script Object Notation(Json), é uma maneira de transmitir dados entre outras linguagens. 
* Neste arquivo, amostra-rá as funções relacionadas a manipulação de Json.
* [-- LINK --](https://www.youtube.com/watch?v=MYMGMg1StVk)
# Operações básicas com Json : 
## Serializar um Objeto : 
* Para serializar um json você usará a função "json_encode($object)" e irá colocar no parâmetro dela o objeto que deseja serializar. 
* EX:
```PHP
class Pessoas
{
public $nome;
public $idade;
}
  
$pes1 = new Pessoas(); // objeto
$pes1->nome = "Ronaldo";
$pes1->idade = 30;
  
$pes1_json = json_encode($pes1); // objeto serializado
echo "$pes1_json";
``` 
* ==Parâmetros extras :== 
	* Esta função possui alguns parâmetros extras, para adicionar mais de 2 parâmetros extras, você precisa usar "|". 
	* Os parâmetros extras são :  
		* **JSON_PRETTY_PRINT** : Deixa o json mais legível.
		* **JSON_UNESCAPED_UNICODE** : Caracteres mult byte (como "Ç" e "ã") são mostrados para visualização. 
		* **JSON_UNESCAPED_SLASHES** : As barras são mostradas para visualização 

## Deserializar um Json : 
* Para deserializar um texto json, você fara uso da função "decode($json)", onde no parâmetro da função você irá colocar o texto json. 
* A função normalmente retornará o json como Objeto. 
* EX: 
```PHP
$json_text = '{"nome":"Ronaldo","idade":30}';// texto json
$json_obj = json_decode($json_text); // transformando texto json em objeto

print_r($json_obj); // printando 
```
* ==Parâmetros extras :==
* Esta função possui alguns parâmetros extras. 
* Sendo eles : 
	* **true** : Retorna o texto json como uma array ao invés de um objeto.  
## Ver erros do Json : 
* Caso na hora de deserializar um json ocorra algum erro, você pode usar a função "json_last_error()", que retorna o erro como valor numérico.
* Para ver mais, olhe este [-- LINK --](https://youtu.be/MYMGMg1StVk?si=fY9gxZ0PwDhUrZq1&t=1443)  