# 🧑‍💻 Arquitetura de um SGBD
<p align="justify">
Sistema de Gerenciamento de Banco de Dados é um software utilizado para gerencias banco de dados.
---

## Modelos de dados
<p align="justify">
Os modelos de dados são utilizados na descrição e na construção lógicas e fisica de banco de dados. Os tipos de dados que tem relação entre eles e suas restrições são conhecidos como estrutura ou nivel:

<ul>
    <li>Alto Nível: Denominado como modelo de dados conceituais ou modelo Entidade-Relacionamento, o seu principal conceito é uma projeção dos dados com uma maior proximidade possível da visão que os usuário obtém dele</li>
    <li>Baixo Nível: Modelo de dados de caráter físico, pois fornece uma visão detalhada da maneira em como os dados armazenados em um local.</li>
</ul>
</p>

## Esquemas
<p align="justify">
Esquema é uma estrutura lógica que organiza e agrupa objetos do banco de dados, como tabelas, views, índices, procedimentos armazenados e funções. Uma maneira simples é pensar que:
<ul>
    <li>Bando de dados: um armário</li>
    <li>Schema: uma gaveta do armário</li>
    <li>Tabela: os documentos dentro da gaveta</li>
</ul>
Assim, um banco de dados pode conter vários schemas, organizando objetos relacionados

```text
Empresa (Banco de Dados)
│
├── vendas (Schema)
│   ├── clientes (Tabela)
│   ├── pedidos (Tabela)
│   └── produtos (Tabela)
│
├── rh (Schema)
│   ├── funcionarios (Tabela)
│   ├── salarios (Tabela)
│   └── departamentos (Tabela)
│
└── financeiro (Schema)
    ├── contas_pagar (Tabela)
    └── contas_receber (Tabela)
```
Esse processo de concepção de um esquema se chama modelagem de dados, e existem dois estilos mais utilizados para os esquemas de banco de dados:
<ul>
    <li><strong>Esquema de banco de dados lógico:</strong> Abrange restrições de caráter lógico aplicadas aos dados armazenados. Pode, entre outras definições, cobrir as restrições de integridade, exibição e tabelas.</li>
    <li><strong>Esquema de banco de dados físico:</strong> Contempla a forma de armazenagem física no sistema de armazenamento, incluindo os arquivos e índices.</li>
</ul>

## Instâncias
<p align="justify">
Instâncias são registros em banco de dados, estruturas de memória que formam a área de uma memória compartilhada, denominada de área global do sistema. Essas instâncias atuam em processos de segundo plano. Os processos rodam sempre no servidor, localizados na memória RAM e no processador. A instância pode existir de forma independente dos arquivos de um banco de dados. Em outras palavras, a instância corresponde aos dados armazenados na tabela naquele instante, então, como a tabela pode mudar, a instância também muda com o tempo.

| Esquema (Schema) | Instância |
|------------------|-----------|
| Define a estrutura do banco. | Representa os dados armazenados. |
| Muda raramente. | Muda frequentemente. |
| Contém tabelas, colunas, tipos de dados, restrições etc. | Contém os registros (linhas) das tabelas. |
</p>

## Tipos de arquivos
<p align="justify">
Para a composição de banco de dados, é necessário que os arquivos sejam gerados no momento da elaboração do banco. Existindo basicamente três tipos de arquivos:
<ul>
    <li><strong>Primários:</strong> Contém informações responsáveis pela inicialização do banco de dados. Os dados de usuário e objetos podem estar contidos nesse arquivo. Os primários são de criação de usuário.</li>
    <li><strong>Secundário:</strong> São arquivos definidos pelo usuário e costumam armazenar seus dados.</li>
    <li><strong>Log de Transações:</strong> Logs constituem em arquivos que armazenam informações de logs. Utilizadas na restauração de banco de dados.</li>
</ul>
</p>