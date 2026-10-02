# 🧑‍💻 Aprenda CSS

## Modelo de Caixa
<p align="justify">
Todo elemento de HTML é tratado como uma caixa com 4 partes: 
<ul>
<li> Margin: Espaço externo entre a caixa e outros elementos </li>
<li> Border: Borda da caixa </li>
<li> Padding: Espaço entre o conteúdo e a borda</li>
<li> Content: Conteúdo do elemento </li>
</ul>

Exemplo: 
```
<p>I am a paragraph of text that has a few words in it.</p>

p {
  width: 100px;
  height: 50px;
  padding: 20px;
  border: 1px solid;
}
```
Esse conteúdo vai sair do elemento.

O modelo de caixa é essencial no CSS. 
### Conteúdo e dimensionamento
As caixas têm comportamento diferente com base no valor display, nas dimensões definidas e no conteúdo que contêm. O conteúdo afeta o tamanho da caixa por padrão. Pode ser controlado através do dimensionamento extrínseco ou intrínseco para permitir que o navegador tome decisões com base no tamanho do conteúdo.
O padrão dos navegadores é contabilizar o padding e borda como parte do conteúdo, aumentando seu tamanho. Para controlar melhor o tamanho, indica-se utilizar o box-sizing: border-box, que exclui do calculo padding e borda.
</p>

## Seletores
<p align="justify">
Seletores são utilizados para selecionar partes especificas do HTML.

### Seletores simples
O grupo mais direto de seletores tem como alvo elementos HTML, classes e id.
<ul>
<li>Universal: [ * ] Seleciona todos os elementos
<li>Tipo: [ elemento HTML ] Seleciona diretamente todos os elementos HTML correspondentes
<li>Classe: [ .classe ] Seleciona todos os elementos que contenham a classe
<li>ID: [ #id ] Seleciona o elemento que contenha o ID
<li>Atributo: [ atributo=valor] Seleciona todos os atributos com o valor específico 
</p>