# 🧑‍💻 Banco de Dadoos
<p align="justify">
Bacno de dados é um sistema organizado para armazenar, gerenciar e recuperar informações de forma eficiente e segura. Essencial em praticamente todos o s sitemas modernos.
</p>

---

## Sistema de gerenciamento (SGBD)
<p align="justify">
Para controlar um banco de dados, utilizamos um software que chamados de Sistema de Gerenciamento de Banco de Dados, conhecido como SGBD, alguns exemplos:
<ul>
    <li>MySQL</li>
    <li>PostgresSQL</li>
    <li>MongoDB</li>
</ul>
</p>

## Tipos de Banco de Dados
<p align="justify">
Existem dois principais tipo de banco de dados:

### Banco de dados relacional (SQL)
É o modelo mais tradicional, onde os dados ficam organizados em tabelas e planilhas onde as <strong>linhas são os registros e as colunas os atributos</strong> sendo uma esrtutura bem organizada e facil de consultar.
| ID | Nome | Idade |
|-------------|-------------|--------------|
| 1         | Ana        | 20           |
| 2           | Bruno   | 22           |

### Banco de dados não relacionais (NoSQL)
Não usa tabelas fixas Os dados podem ser armazenados de maneira mais flecivel, escalando melhor para grandes volumes, hoje em dia muito usado em apps modernos. Alguns formatos usados são os:
<ul>
    <li>JSON</li>
    <li>Chave Valor</li>
    <li>Grafos</li>
</ul>

~~~
{
    JSON
  "nome": "Ana",
  "idade": 20,
  "notas": [8, 9, 10]
}
~~~
</p>

## O que é SQL
<p align="justify">
SQL ou Structured Query Language é a linguagem usada para interagir com banco de dados relacionais. Os principais comandos:

  * SELECT: buscar dados
    ~~~
    SELECT * FROM alunos
    --------------------
    SELECT nome, email 
    FROM clientes 
    WHERE cidade = 'São Paulo';
    ~~~
* INSERT: inserir dados
    ~~~
    INSERT INTO clientes (nome, cidade)
    VALUES ('Ana', 'Rio de Janeiro')
    ~~~
* UPDATE: atualizar dados existente
    ~~~
    UPDATE clientes 
    SET cidade = 'Belo Horizonte' 
    WHERE id = 1;
    ~~~
* DELETE: deletar dados existente
    ~~~
    DELETE FROM clientes 
    WHERE id = 1;
    ~~~
    
<strong>É importante tomar cuidado e usar WHERE para não comandar sobre todos os dados da tabela</strong>
</p>

### Data Definition Language (DDL)
<p align="justify">
Comando utilizados para a definição da estrutura do bando de dados em si, como criar o banco de dados, acessos, alterações e etc.

* CREATE TABLE: cria tabela
  ~~~
  CREATE TABLE clientes (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE,
    cidade VARCHAR(50),
    data_cadastro DATE);
    ~~~
* ALTER TABLE: altera tabela
    ~~~
    ALTER TABLE clientes 
    ADD telefone VARCHAR(20);
    ~~~
* DROP TABLE: exclui tabela
    ~~~
    DROP TABLE clientes;
    ~~~
    
    </p>
