# 🧑‍💻 Diagrama de Classes

<p align="justify">
O <strong>Diagrama de Classes</strong> é um dos principais diagramas da UML (Unified Modeling Language). Ele representa, de forma visual, a estrutura de um sistema orientado a objetos, mostrando suas classes, atributos, métodos e os relacionamentos existentes entre elas.
</p>

---

## Classe x Objeto

<p align="justify">
Antes de compreender um diagrama de classes, é importante diferenciar os conceitos de <strong>classe</strong> e <strong>objeto</strong>.
</p>

### Classe

<p align="justify">
Uma <strong>classe</strong> é a estrutura fundamental da Programação Orientada a Objetos (POO). Ela funciona como um modelo que define quais atributos e comportamentos (métodos) seus objetos possuirão.
</p>

### Objeto

<p align="justify">
Um <strong>objeto</strong> é uma instância de uma classe, criada durante a execução do sistema. Cada objeto possui seus próprios valores para os atributos definidos pela classe.
</p>

> **Exemplo:** A classe **Pessoa** pode possuir os atributos **nome** e **idade**. João e Maria são objetos dessa classe.

---

## Estrutura Básica

<p align="justify">
Uma classe é representada por um retângulo dividido em três partes:
</p>

1. Nome da classe
2. Atributos
3. Métodos

### Nome da Classe

<p align="justify">
O nome da classe normalmente é um substantivo, escrito no singular e seguindo o padrão <strong>PascalCase</strong>, onde cada palavra inicia com letra maiúscula.
</p>

**Exemplos:**

* Cliente
* Pedido
* ContaBancaria

### Atributos

<p align="justify">
Representam as características que os objetos daquela classe possuem. Geralmente começam com letra minúscula e seguem o padrão <strong>camelCase</strong>.
</p>

**Exemplos:**

* nome
* idade
* dataNascimento

### Métodos

<p align="justify">
Representam os comportamentos ou ações que os objetos da classe podem executar. Correspondem às funções da Programação Orientada a Objetos.
</p>

**Exemplos:**

* cadastrar()
* calcularTotal()
* realizarPagamento()

---

## Visibilidade

<p align="justify">
A visibilidade define quem pode acessar os atributos e métodos de uma classe.
</p>

| Símbolo | Visibilidade | Descrição |
|----------|--------------|-----------|
| + | Pública | Pode ser acessado por qualquer classe. |
| - | Privada | Apenas a própria classe possui acesso. |
| # | Protegida | Pode ser acessado pela classe e suas subclasses. |

---

## Relacionamentos

<p align="justify">
Os relacionamentos representam como duas ou mais classes interagem dentro do sistema.
</p>

### Associação

<p align="justify">
É o relacionamento mais comum entre classes. Indica que uma classe conhece, utiliza ou está conectada a outra.
</p>

**Representação:** Linha simples.

Características:

* Geralmente possui um nome (normalmente um verbo).
* Pode ser unidirecional ou bidirecional.
* Deve possuir cardinalidade.

**Cardinalidades:**

* 0..1
* 1
* 0..\*
* 1..\*

---

### Agregação

<p align="justify">
Representa uma relação de <strong>todo e parte</strong>, onde as partes podem existir independentemente do todo.
</p>

**Representação:** Losango vazio.

**Exemplo:** Departamento e Funcionário.

---

### Composição

<p align="justify">
Representa uma relação forte entre duas classes. A classe "filha" depende totalmente da classe principal para existir.
</p>

**Representação:** Losango preenchido.

**Exemplo:** Casa e Cômodo.

---

### Generalização (Herança)

<p align="justify">
Representa uma relação de herança entre classes, onde uma classe filha herda atributos e métodos da classe pai.
</p>

**Representação:** Seta com triângulo vazio.

Exemplo:

```text
Animal
   ▲
   │
──────────────
│            │
Cachorro    Gato
```

---

## Exemplo de Classe

```text
-------------------------
|        Animal          |
-------------------------
| - nome : String        |
| - numero : int         |
| - idade : int          |
-------------------------
| + comer()              |
| + correr()             |
| + tomarSol()           |
-------------------------
```

---

## Exemplo de Diagrama de Classes

<p align="justify">
O exemplo abaixo representa um diagrama de classes para um sistema de hospital veterinário.
</p>

![Exemplo de Diagrama de Classes](/2%20Semestre/Modelagem%20de%20Software/Images/Exemplo%20Diag.%20Classe.png)