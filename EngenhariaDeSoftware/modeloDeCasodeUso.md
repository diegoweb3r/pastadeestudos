# 🧑‍💻 Modelo de Caso de Uso

<p align="justify">
O <strong>Modelo de Caso de Uso</strong> é uma técnica da UML (Unified Modeling Language) utilizada para representar os requisitos funcionais de um sistema sob a perspectiva do usuário. Ele descreve como os atores interagem com o sistema para alcançar determinados objetivos.
</p>

<p align="justify">
Esse modelo é composto por dois elementos principais:
</p>

* **Diagrama de Caso de Uso:** representação gráfica dos atores, casos de uso e seus relacionamentos.
* **Especificação de Caso de Uso:** descrição textual detalhada de cada caso de uso.

<p align="justify">
O modelo é elaborado durante o levantamento de requisitos, envolvendo desenvolvedores e usuários do sistema, permitindo compreender claramente quais funcionalidades devem ser implementadas.
</p>

---

## Objetivos

<p align="justify">
O principal objetivo do Modelo de Caso de Uso é especificar, visualizar, construir e documentar o comportamento esperado do sistema. Sua utilização proporciona diversos benefícios durante o desenvolvimento.
</p>

Entre seus principais objetivos estão:

* Descrever os requisitos funcionais do sistema.
* Definir claramente o escopo do sistema.
* Auxiliar na elaboração do Diagrama de Classes.
* Facilitar futuras alterações e extensões do sistema.
* Servir como base para criação de casos de teste.
* Identificar os diferentes perfis de usuários.
* Definir condições de início, término e exceções de cada funcionalidade.

---

## Elementos do Diagrama de Caso de Uso

<p align="justify">
Um Diagrama de Caso de Uso é composto por alguns elementos básicos responsáveis por representar a interação entre os usuários e o sistema.
</p>

### Caso de Uso

<p align="justify">
Representa uma funcionalidade oferecida pelo sistema que produz um resultado observável para um ator.
</p>

**Representação:** Elipse (oval).

---

### Ator

<p align="justify">
Representa qualquer elemento externo que interage com o sistema. Um ator pode ser uma pessoa, outro sistema ou até mesmo um dispositivo.
</p>

**Representação:** Boneco de palito.

---

### Associação

<p align="justify">
Representa a comunicação entre um ator e um caso de uso, indicando que aquele ator participa da execução da funcionalidade.
</p>

**Representação:** Linha simples.

---

## Relacionamentos

### Generalização entre Atores

<p align="justify">
Permite representar herança entre atores. O ator filho herda todas as características e interações do ator pai.
</p>

**Representação:** Linha com seta de triângulo vazio.

---

### Generalização entre Casos de Uso

<p align="justify">
Ocorre quando dois ou mais casos de uso possuem comportamentos semelhantes, permitindo reutilizar funcionalidades por meio da herança.
</p>

---

### Include

<p align="justify">
Indica que um caso de uso sempre executa outro caso de uso durante sua realização. O comportamento incluído é obrigatório.
</p>

**Exemplo:**

```
Realizar Compra
       │
   <<include>>
       │
Autenticar Usuário
```

---

### Extend

<p align="justify">
Indica um comportamento opcional que pode ser executado durante outro caso de uso, dependendo de uma determinada condição.
</p>

**Exemplo:**

```
Finalizar Compra
        │
    <<extend>>
        │
Aplicar Cupom
```

---

## Como Elaborar um Diagrama de Caso de Uso

### Passo 1 — Identificar os Atores

<p align="justify">
Liste todos os usuários e sistemas externos que interagem com o sistema.
</p>

Perguntas úteis:

* Quem utiliza o sistema?
* Quem fornece informações?
* Quem consulta informações?
* Quem administra o sistema?
* Existem outros sistemas que interagem com este?

---

### Passo 2 — Identificar os Casos de Uso

<p align="justify">
Defina quais objetivos cada ator deseja alcançar utilizando o sistema.
</p>

Perguntas úteis:

* O ator deseja cadastrar informações?
* Deseja consultar dados?
* Deseja alterar ou excluir registros?
* Precisa receber notificações?
* Precisa comunicar-se com outro sistema?

---

### Passo 3 — Construir o Diagrama

<p align="justify">
Desenhe os atores, os casos de uso e seus relacionamentos.
</p>

Ao finalizar, verifique:

* Todo ator participa de pelo menos um caso de uso.
* Todo caso de uso possui pelo menos um ator associado.
* Não existem elementos redundantes.

---

## Especificação de Caso de Uso

<p align="justify">
Além do diagrama gráfico, cada caso de uso deve possuir uma documentação textual descrevendo seu funcionamento detalhadamente.
</p>

Uma especificação normalmente contém:

* Nome do caso de uso
* Objetivo
* Breve descrição
* Atores envolvidos
* Pré-condições
* Fluxo principal
* Fluxos alternativos
* Fluxos de exceção
* Pós-condições

---

## Exemplo de Especificação

| Campo | Descrição |
|--------|-----------|
| Nome | Realizar Login |
| Objetivo | Permitir o acesso ao sistema |
| Ator | Usuário |
| Pré-condição | Usuário cadastrado |
| Fluxo Principal | Informar usuário e senha → Validar credenciais → Acessar sistema |
| Fluxo Alternativo | Senha incorreta |
| Pós-condição | Usuário autenticado |