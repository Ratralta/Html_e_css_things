# COMO :
* As colunas normalmente não possuem uma maneira de ser especificada.
* Então para conseguir mexer em colunas especificas, necessário criar uma "id"
* ==ESTA SINTAXE SÓ FUNCIONA PRO [[MySQL]]==
# Criando "id" :
* Para criar uma id, faça isso caso a tabela ainda não tiver sido criada :
```SQL
CREATE TABLE tabela_com_id (
id INT PRIMARY KEY AUTO_INCREMENT,
nome VARCHAR(40)
);
-- id INT PRIMARY KEY AUTO_INCREMENT
-- "PRIMARY KEY" define que essa coluna é uma "chave".
-- "AUTO_INCREMENT" faz com que automaticamente aumente mais 1.
```