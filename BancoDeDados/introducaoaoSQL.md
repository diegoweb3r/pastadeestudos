# 🧑‍💻 Introdução ao SQL

## O que é SQL?
<p align="justify">
SQL ou linguagem de consulta estruturada é uma linguagem  projetada para permitir que usuários com ou sem conhecimento consultem, manipular ou transformem dados em um banco de dados relacional. E por sem simples, o SQL é o banco de dados de muitas aplicações na web. Existem muitos bancos de dados SQL: SQLite. MySQL, Oracle e etc. Todos suportam o padrão de linguagem SQL comum.
</p>


## Banco de dados relacionais
<p align="justify">
Um banco de dados relacional representa uma coleção de tabelas relacionadas. Cada tabela é semelhante a uma planilha do Excel, com um número fixo de colunas nomeadas e um numero variável de linhas de dados. Exemplo: <br>
O departamento de veículos poderia ter um banco de dados com os veículos do estado armazenando, nome do modelo, tipo, numero de portas e rodas. Pode haver ainda tabelas adicionais dos motoristas de cada carro por exemplo. 
</p>

## Noções básicas de consultas SELECT
<p align="justify">
Para recuperar dados de um banco de dados SQL, precisamos usar o comando SELECT, também chamada de consultas. Uma consulta em si é apenas uma instrução que declara quais dados estamos procurando. 

```
Selecione uma consulta para colunas específicas.
SELECT column, another_column, …
FROM mytable;
```

</p>

## Consultas com restrições
<p align="justify">
Sabe-se usar o Select, porém, em uma tabela com milhares de dados somente isso seria ineficiente. Para filtra determinados resultados e impedir que sejam retornados, deve-se usar a cláusula WHERE. Ela é aplicada a cada linha de dados, verificando valores de colunas específicas para determinar se ela deve ou não ser incluída.

```
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;[
    ]
```
Cláusulas mais complexas podem ser construídas combinando várias palavras chave AND e OR. Abaixo segue alguns operadores lógico:

| **Operador** | **Descrição** | **Exemplo de SQL** |
| :--- | :--- | :--- |
| `=`, `!=`, `<`, `<=`, `>`, `>=` | Operadores numéricos padrão | `col_name != 4` |
| `BETWEEN ... AND ...` | O número está dentro de um intervalo de dois valores (inclusive). | `col_name BETWEEN 1.5 AND 10.5` |
| `NOT BETWEEN ... AND ...` | O número não está dentro do intervalo de dois valores (inclusive). | `col_name NOT BETWEEN 1 AND 10` |
| `IN (...)` | O número existe em uma lista. | `col_name IN (2, 4, 6)` |
| `NOT IN (...)` | O número não existe na lista. | `col_name NOT IN (1, 3, 5)` |

Além de tornar os resultados mais fáceis de entender, escrever cláusulas para restringir o conjunto de linhas retornadas também permite que a consulta seja executada mais rapidamente devido a redução de dados retornados.

Ao escrever WHERE com colunas contendo dados de texto, o SQL oferece suporte a diversos operadores úteis para realizar tarefas como comparação de strigns sem distinção de maiúsculas e minúsculas e correspondência de padrões curinga.

| **Operador** | **Descrição** | **Exemplo** |
| :---: | :--- | :--- |
| `=` | Comparação exata de strings que diferencia maiúsculas de minúsculas (observe o sinal de igual único). | `col_name = "abc"` |
| `!=` ou `<>` | Comparação de desigualdade exata de strings que diferencia maiúsculas de minúsculas. | `col_name != "abcd"` |
| `LIKE` | Comparação exata de strings sem distinção entre maiúsculas e minúsculas. | `col_name LIKE "ABC"` |
| `NOT LIKE` | Comparação de desigualdade exata de strings que ignora maiúsculas e minúsculas. | `col_name NOT LIKE "ABCD"` |
| `%` | Utilizado em qualquer lugar de uma string para corresponder a uma sequência de zero ou mais caracteres (apenas com `LIKE` ou `NOT LIKE`). | `col_name LIKE "%AT%"`<br>(corresponde a `"AT"`, `"ATTIC"`, `"CAT"` ou `"BATS"`) |
| `_` | Utilizado em qualquer lugar de uma string para corresponder a um único caractere (apenas com `LIKE` ou `NOT LIKE`). | `col_name LIKE "AN_"`<br>(corresponde a `"AND"`, mas não a `"AN"`) |
| `IN (...)` | A string existe em uma lista. | `col_name IN ("A", "B", "C")` |
| `NOT IN (...)` | A string não existe na lista. | `col_name NOT IN ("D", "E", "F")` |

Atente-se que as strings devem estar entre aspas.

</p>