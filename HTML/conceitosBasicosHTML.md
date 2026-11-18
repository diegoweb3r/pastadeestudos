# 🧑‍💻 Conceitos básicos de HTML
<p align="justify">
Hypertext Markup Language (HTML) não é uma linguagem de programação, mas uma linguagem de marcação, definindo uma estrutura e significado do conteúdo na web.
</p>

---

## Anatomia de uma página
<p align="justify">
Toda página HTML segue uma estrutura padrão, o navegador usa essas marcações para saber o que exibir.
# Estrutura Básica de HTML

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Página</title>
</head>
<body>

    <h1>Olá, mundo!</h1>
    <p>Este é um documento HTML básico.</p>

</body>
</html>
```
</p>

### Elementos essenciais
<p align="justify">
Elementos ou tags são o que marcam os textos em HTML, normalmente vem em pares: abertura e fechamento, veja algumas tags mais utilizadas:
<ul>
    <li><strong>h1~h6</strong>: Tags de titulo, sendo a 1 o mais importante e 6 o menos.</li>
    <li><strong>p</strong>: Utilizado para paragráfos</li>
    <li><strong>a</strong>: Utilizado para adicionar links a páginas</li>
    <li><strong>div</strong>: Tag utilizada para servir de container</li>
    <li><strong>img</strong>: Usada para adicionar imagens</li>
</ul>
</p>

### Estrutura semântica
<p align="justify">
Tags semânticas são relativamente novas no HTML, são utilizadas para dar sentido para além do visual. Descreve o significado da tag, ajuda a manutenção do código, SEO e acessibilidade. Veja algumas tags:
<ul>
    <li><code>&lt;header&gt;</code> → Cabeçalho da página ou de uma seção.</li>
    <li><code>&lt;nav&gt;</code> → Menu de navegação.</li>
    <li><code>&lt;main&gt;</code> → Conteúdo principal.</li>
    <li><code>&lt;section&gt;</code> → Seção de conteúdo relacionada.</li>
    <li><code>&lt;article&gt;</code> → Conteúdo independente, como um artigo ou postagem.</li>
    <li><code>&lt;aside&gt;</code> → Conteúdo complementar, como uma barra lateral.</li>
    <li><code>&lt;footer&gt;</code> → Rodapé.</li>
</ul>
</p>

### Formulários
<p align="justify">
A filosofia do React baseia-se em dividir a interface em pedaços isolados e reutilizáveis, como blocos de LEGO. No React moderno, a unidade fundamental é o comportamento funcional.
</p>
<p align="justify">
Um componente funcional nada mais é que uma função JS pura que retorna uma descrição de interface. Substituindo completamente os antigos componentes baseados em classes devido a sua simplicidade, legibilidade e facilidade de teste. Opera perfeitamente junto a API e Hooks do React.

```
function BotaoEnviar() {
  return (
    <button className="btn-primario">
      Enviar Dados
    </button>
  );
}
```
</p>

### Arquivos JSX e renderização de arquivos
<p align="justify">
Arquivos com extensão .jsx (ou .tsx se usando TypeScript) permitem misturar a lógica do JS com a estrutura visual do HTML em um unico lugar. Essa união é chamada de Co-location: ideia de que a lógica visual e a estrutura devem viver juntas porque são altamente dependentes.
<ul>
    <li><strong>A Regra do elemento pai</strong>: O JSW restringe a um retorno de um único elemento raiz. Se tiver irmãos soltos, precisará envolver em uma tag container ou Fragment, que agrupa os elementos sem renderizar nenhuma tag extra no HTML real.</li>
    <li><strong>Expressões JSX</strong>: Para injetar a lógica JS (variáveis, cálculos ou chamadas de função) dentro do seu código, utiliza-se chaves {}</li>
</ul>
</p>

### Renderizando listas em React
<p align="justify">
No desenvolvimento web, frequentemente precisamos transformar estruturas de dados (como um array de objetos vindos de um banco de dados) em elementos visuais na tela. No React, não utiliza-se estruturas de repetições tradicionais, como for ou while dentro do JSX. Em vez disso, usa-se métodos funcionais que retornam novos arrays, sendo o .map() o mais usado:

```function ListaDeProdutos() {
  const produtos = [
    { id: 1, nome: 'Teclado Mecânico' },
    { id: 2, nome: 'Mouse Wireless' }
  ];

  return (
    <ul>
      {produtos.map((produto) => (
        <li key={produto.id}>{produto.nome}</li>
      ))}
    </ul>
  );
}
```

<ul>
    <li><strong>A importância da propriedade Key</strong>: Sempre que renderizamos uma lista, o React exige uma propriedade especial chamada key no elemento raiz retornado. Essa chave deve ser um identificador único e estável (como um ID). O React usa essa Key durante o processo de reconciliação (Virtual DOM) para rastrear quais itens foram adicionados, alteradois ou removidos. Sem a Key, o react precisaria renderizar novamente a lista inteira do zero, a cada pequena modificação, destruindo sua performance.</li>
</ul>
</p>