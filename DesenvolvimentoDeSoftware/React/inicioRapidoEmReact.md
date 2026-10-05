# 🧑‍💻 Início rápido React

### Criação e aninhamento de componentes
<p align="justify">
Os aplicativos React são compostos por componentes. Um componente é uma parte da interface do usuário (UI) que possui sua própria lógica e aparência. O tamanho do componente pode variar, ser desde um simples botão como uma página completa.
</p>
<p align="justify">
Os componentes REact são funções JavaScript que retornam marcações:

```
function MyButton() {
  return (
    <button>I'm a button</button>
  );
}
```
E pode ser aninhado:

```
export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```
Em regra, o nome do componente começa com maiúscula, diferente das tags em HTML.
</p>

### Marcações com JSX
<p align="justify">
A sintaxe de JSX é opcional porém, muito usada em React, incluindo suporte nativo. JSX é mais restritivo, todas as tags precisam ser fechadas, mesmo as que em HTML não sao necessárias.
</p>

### Adicionando estilos
<p align="justify">
Em React, você especifica uma classe em CSS com "className". Funciona da mesma forma que "class" em uma tag HTML.

```
<img className="avatar" />

.avatar {
  border-radius: 50%;
}
``` 

Para adicionar arquivos CSS, pode-se utilizar da forma tradicional, com um link tag ao HTML.

</p>

### Exibição de dados
<p align="justify">
JSW permite inserir marcação em JavaScript. As chaves permite escapar de volta (como se estivesse saindo da marcação HTML e retornando ao JS puro) para o JavaScript, possibilitando incorporar variáveis do código e exibir ao usuário. Pode-se usar também, esses escapes para atributos. Nota-se que deve utilizar {}

```
return (
  <h1>
    {user.name}
  </h1>
);
```
</p>

### Renderização condicional
<p align="justify">
Em React, não existe sintaxe especial para condições. Em vez disso, você usará as mesmas técnicas que usa em JS comum. 

```
let content;
if (isLoggedIn) {
  content = <AdminPanel />;
} else {
  content = <LoginForm />;
}
return (
  <div>
    {content}
  </div>
);
```

</p>

### Lista de renderização
<p align="justify">
Você utilizará recursos do JS, como o for e a função .map para renderizar listas de componentes. Exemplo:

```
const products = [
  { title: 'Cabbage', id: 1 },
  { title: 'Garlic', id: 2 },
  { title: 'Apple', id: 3 },
];

const listItems = products.map(product =>
  <li key={product.id}>
    {product.title}
  </li>
);

return (
  <ul>{listItems}</ul>
);
```

Perceba que o item li possui um atributo key, ele é obrigatório. Para cara item em uma lista, precisa ter uma string ou numero que identifique exclusivamente esse item. Geralmente essa chave vem do banco de dados e o React usa para saber o que aconteceu se você inserir, excluir ou reordenar.
</p>

### Respondendo a eventos
<p align="justify">
Você pode responder a eventos declarando funções de tratamento de eventos dentro de seus componentes:

```
function MyButton() {
  function handleClick() {
    alert('You clicked me!');
  }

  return (
    <button onClick={handleClick}>
      Click me
    </button>
  );
}
```
No onClick nao há parametros (parênteses), pois não é pra chamar a função, será chamada somente no click do botão.
</p>

### Atualizando a tela
<p align="justify">
Muitas vezes, você vai querer que seus componentes lembrem de algumas informações. O número de vezes que um botão foi chamado, por exemplo. Para fazer isso é só adicionar um estado em React. Primeiro, importe o useState, depois você pode declarar uma variável de estado dentro do componente:

```
import { useState } from 'react';

function MyButton() {
  const [count, setCount] = useState(0);
  // ...
```
Você obterá duas coisas de useState: o estado atual (count), e a função que permite atualiza-lo (setCount). Você pode dar a elas qualquer nome, mas a convenção é "algumaCoisa", "setAlgumaCoisa"; A primeira vez que o botão for exibido, count será 0 (você passou 0) e quando quiser alterar, chame o metodo setCount e passe o novo valor:

```
function MyButton() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <button onClick={handleClick}>
      Clicked {count} times
    </button>
  );
}
```

### Usando ganchos
<p align="justify">
Funções que começam com 'react' use são chamadas de Hooks. useState é um Hook integrado e fornecido pelo React. Você pode encontrar outros Hooks integrados. Você também pode escrever seus próprios Hooks combinando os existentes. Hooks são ainda mais restritivos que as funções. Só pode ser chamada no início dos seus componentes. Se quiser usar useState em uma condição ou em um loop, cri um novo componente e insira-o lá.
</p>

### Compartilhamento de dados entre componentes
<p align="justify">
No exemplo anterior, cada botão "myButton" tinha seu próprio valor independente de count, e ao clicar em cada botão, somente o count desse era alterado. Porém, muitas vezes você precisará de componentes que compartilhem dados e sejam atualizados em conjunto. Para isso, precisa mover o estado dos botões individuais "pra cima" ate o componente mais próximo que os contenham.

```
import { useState } from 'react';

export default function MyApp() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <div>
      <h1>Counters that update together</h1>
      <MyButton count={count} onClick={handleClick} />
      <MyButton count={count} onClick={handleClick} />
    </div>
  );
}

function MyButton({ count, onClick }) {
  return (
    <button onClick={onClick}>
      Clicked {count} times
    </button>
  );
}
 ```
</p>