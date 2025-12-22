# O QUE É :
* São conjunto de dados formados através das "colunas". 
* Você cria colunas para criar um "item". 
* EX:
```SQL
CREATE TABLE pessoas(
id INT AUTO_INCREMENT PRIMARY KEY,
nome VARCHAR(40),
idade INT
);
-- Tabela "pessoas", com colunas : "id", 'nome" e "idade"

INSERT INTO pessoas(nome,idade)
VALUES("ronaldo",19);
/* Criou um novo item. que possui : 
id = 1
nome = ronaldo
idade = 19
*/
```

