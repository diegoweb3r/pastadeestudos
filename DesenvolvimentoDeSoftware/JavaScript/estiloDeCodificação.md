# 🧑‍💻 Estilo de codificação
<p align="justify">
Nosso código deve ser o mais limpo e fácil de ler. Essa talvez seja a tarefa da programação: escrever tarefas complexas de forma correta e legível para seres humanos.
</p>

## Sintaxe
<p align="justify">
Existem algumas regras de escrita, inclusive algumas sugeridas.

### Chaves
Na maioria dos projetos em JS, as chaves são escritas no chamado "egípcio", com a chave de abertura na mesma linha da palavra chave correspondente. Também deve haver um espaço antes da chave de abertura.

```
if (condition) {

}
```

Construções na mesma linha, como if (condition) doSomething(), é um caso especial. Geralmente usado para códigos curtos.

## Cumprimento da linha
A crase permite dividir a string em várias linhas, e geralmente se convencionam a quantidade de caracteres por linha.

## Indentação
Existem dois tipos de indentação:
<ul>
<li>Indentação horizontal 2 ou 4 espaços: pode ser feita com 2 ou 4 espaços ou o tab. Atualmente os espaços são mais usados, uma vantagem é que eles permitem configurações mais flexíveis de indentação. </li>
<li> Indentação vertical: livas vazias para separar blocos lógicos. Até uma mesma função pode ser dividida em blocos, ajuda a manter o código mais legível.</li>

## Ponto e virgula
Um ponto e vírgula deve estar presente após cada instrução, mesmo quando ele pode ser omitido. Existem linguagens que é opcional e raramente utilizados, mas em JS, existem situações que uma quebra de linha não é interpretada como um ponto e vírgula e pode deixar o código sujeito a erros.


## Níveis de aninhamento
Tente evitar muitos aninhamentos no código. Por exemplo, em um loop, ás vezes é uma boa ideia utilizar a instrução continue para evitar níveis extras de aninhamento. Pode-se usar de maneira semelhante o return.

</p>