# O que é : 
* Data Base Object(DBO), é um objeto do banco de dados apos fazer uso do constructor especial "SQLite3".
* Com ele é possível manipular o data base através da função "exec" do DBO. 
# Exemplos manipulando o DBO

## Criação de tabela básica :
```PHP
$conn = new SQLite3('data_base.db');

$conn->exec('
CREATE TABLE pessoas(
id INT AUTO_INCREMENT PRIMARY KEY,
nome VARCHAR(40),
idade INT
)
');
```

## Inserindo conteúdo na tabela  :
```PHP
$conn->exec('
INSERT INTO pessoas(nome,idade) VALUES("Ronaldo",19);
INSERT INTO pessoas(nome,idade) VALUES("Felipe",41);
INSERT INTO pessoas(nome,idade) VALUES("Paulo",22)
');
```

