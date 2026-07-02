# 🧑‍💻 Conceitos básicos de React
<p align="justify">
React é uma biblioteca JavaScript criada pela Meta para desenvolver interfaces de usuário (UI), principalmente para aplicações web de página única (SPA - Single Page Application)
</p>

---

## Conhecendo o React
<p align="justify">
O React é uma biblioteca de código aberto desenvolvida em JavaScript voltada para construção de interfaces de usuário. Criado pela Meta em 2013, se tornou o padrão no mercado por resolver problemas de lentidão na manipulação do DOM.
<ul>
    <li><strong>Biblioteca vs. Framework</strong>: O React é uma biblioteca, Foca apenas na camada Visual. Não dita como você deve fazer requisições HTTP ou gerenciar rotas. Você tem liberdade de acoplar outras ferramentas ao projeto conforme necessidade.</li>
    <li><strong>Mentalidade declarativa</strong>: No JS tradicional (Imperativo), você descreve o passo a passo de como o navegador deve alterar o HTML. no React (Declarativo), você descreve o que quer ver na tela baseado nos dados atuais. Se os dados mudam, o React atualiza automaticamente.</li>
    <li><strong>O virtual DOM</strong>: Para evitar custo computacional de redesenhar a página a cada alteração, o React mantém uma cópia leve do DOM na memória. Quando ocorre uma mudança, ele gera um novo virtual DOM, compara com a anterior através de um algoritmo diferenciação (Diffing), agrupa as modificações (Batching) e atualiza cirurgicamente apenas o que mudou no DOM real do navegador.</li>
</ul>
</p>

### Empacotadores (Bundlers) e Compiladores do React
<p align="justify">
Um navegador moderno não entendo a sintaxe moderna do React nativamente, não entende arquivos .JSX, importações de arquivos CSS dentro do JS ou imagens tratadas como módulos. E é aqui onde entrar os Compiladores e Empacotadores.
<ul>
    <li><strong>Compiladores (Babel/SWC)</strong>: Atua como um tradutor de código. Pega sintaxe avançada do React e a transforma em uma versão mais antiga do JS, que qualquer navegador possa executar.</li>
    <li><strong>Empacotador/Bundler (Webpack/Rollup)</strong>: Uma aplicação do React possui dezenas ou centenas de arquivos separados. O papel do Bundler é rastrear todas as dependências da aplicação, ler, e empacota-los em poucos arquivos finais consolidados para que o navegador possa baixa-lo de forma eficiente.</li>
</ul>
</p>

### Create React App (CRA) vs. Vite
<p align="justify">
Para iniciar um projeto React, você não configura compiladores e empacotadores manualmente, usa-se uma ferramenta de Scaffolding e as duas mais conhecidas são:
<ul>
    <li><strong>Create React App (CRA)</strong>: Desenvolvido pela própria Meta, foi padrao de muitos anos. Utiliza internamente o Babel para compilar e Webpack para empacotar, mas, ele compila e empacota toda a aplicação antes de iniciar o servidor de desenvolvimento. À medida que o projeto cresce, o tempo de inicialização e de atualização de tela se torna lento. Foi descontinuado oficialmente.</li>
    <li><strong>Vite</strong>: Ferramenta mais moderna e padrão da indústria atual. Criado por Evan You, o Vite revolucionou o desenvolvimento por ser rápido. O Vite usa Native ESM (módulos nativos do navegador). Ele faz com que o próprio navegador requisite os arquivos sob demanda. Também usa Esbuild para pré-empacotar dependências, sendo até 100 vezes mais rápidos.</li>
</ul>
</p>

## Sintaxe, arquivos e exibição de dados

### Componentes funcionais do React
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