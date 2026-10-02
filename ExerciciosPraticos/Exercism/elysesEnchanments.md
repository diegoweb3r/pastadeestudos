# Elyse's Enchantments

### Instructions

<p align="justify">

As a magician-to-be, Elyse needs to practice some basics. She has a stack of cards that she wants to manipulate.

</p>

<p align="justify">

To make things a bit easier she only uses the cards 1 to 10 so her stack of cards can be represented by an array of numbers. The position of a certain card corresponds to the index in the array. That means position 0 refers to the first card, position 1 to the second card etc.

</p>

### Introduction

<p align="justify">

In JavaScript, an array is a list-like structure with no fixed length which can hold any type of primitives or objects, even mixed types.

</p>

<p align="justify">

To create an array, add elements between square brackets `[]`. To read from the array, put the index in square brackets `[]` after the identifier. The indices of an array start at zero.

</p>

For example:

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers[2];
// => 3
```

<p align="justify">

To retrieve the number of elements that are in an array, use the `length` property:

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.length;
// => 4
```

<p align="justify">

To change an element in the array, you assign a value at the index:

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers[0] = 'one';
numbers;
// => ['one', 'two', 3, 'four']
```

### Methods

<p align="justify">

Some of the methods that are available on every Array object can be used to add or remove from the array. Here are a few to consider when working on this exercise:

</p>

#### push

<p align="justify">

A `value` can be *added* to the end of an array by using `.push(value)`. The method returns the new length of the array.

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.push(5); // => 5
numbers;
// => [1, 'two', 3, 'four', 5]
```

#### pop

<p align="justify">

The *last* `value` can be *removed* from an array by using `.pop()`. The method returns the removed value. The length of the array will be decreased because of this change.

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.pop(); // => four
numbers;
// => [1, 'two', 3]
```

#### shift

<p align="justify">

The *first* `value` can be *removed* from an array by using `.shift()`. The method returns the removed value. The length of the array will be decreased because of this change.

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.shift(); // => 1
numbers;
// => ['two', 3, 'four']
```

#### unshift

<p align="justify">

A `value` can be *added* to the beginning of an array by using `.unshift(value)`. The method returns the new length of the array.

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.unshift('one'); // => 5
numbers;
// => ['one', 1, 'two', 3, 'four']
```

#### splice

<p align="justify">

A `value` at a specific `index` can be *removed* from an array by using `.splice(index, 1)`. The method returns the removed element(s).

</p>

```javascript
const numbers = [1, 'two', 3, 'four'];
numbers.splice(2, 1, 'one'); // => [3]
numbers;
// => [1, 'two', 'one', 'four']
```

#### Advanced

<p align="justify">

These methods are more powerful than described:

</p>

* Both `push` and `unshift` allow you to push or unshift multiple values at once, by adding more arguments. That is not necessary to complete this exercise.
* Splice can remove multiple values by increasing the second argument. That is not necessary to complete this exercise.
* Splice can also add multiple values by adding them as arguments after the `deleteCount`. This can be used to replace values, or insert values in the middle of an array (for example by removing 0 elements). That is not necessary to complete this exercise.

### Note

<p align="justify">

All but two functions should update the array of cards and then return the modified array - a common way of working known as the Builder pattern, which allows you to nicely daisy-chain functions together.

</p>

<p align="justify">

The two exceptions are `getItem`, which should return the card at the given position, and `checkSizeOfStack` which should return `true` if the given size matches.

</p>

#### Task 1 - Get an Item

<p align="justify">

To pick a card, return the card at index `position` from the given stack.

</p>

```javascript
const position = 2;
getItem([1, 2, 4, 1], position);
// => 4
```

#### Task 2 - Set an Item

<p align="justify">

Perform some sleight of hand and exchange the card at index `position` with the replacement card provided. Return the adjusted stack.

</p>

```javascript
const position = 2;
const replacementCard = 6;
setItem([1, 2, 4, 1], position, replacementCard);
// => [1, 2, 6, 1]
```

#### Task 3 - Insert an Item at the Top

<p align="justify">

Make a card appear by inserting a new card at the top of the stack. Return the adjusted stack.

</p>

```javascript
const newCard = 8;
insertItemAtTop([5, 9, 7, 1], newCard);
// => [5, 9, 7, 1, 8]
```

#### Task 4 - Remove an Item

<p align="justify">

Make a card disappear by removing the card at the given `position` from the stack. Return the adjusted stack.

</p>

```javascript
const position = 2;
removeItem([3, 2, 6, 4, 8], position);
// => [3, 2, 4, 8]
```

#### Task 5 - Remove an Item from the Top

<p align="justify">

Make a card disappear by removing the card at the top of the stack. Return the adjusted stack.

</p>

```javascript
removeItemFromTop([3, 2, 6, 4, 8]);
// => [3, 2, 6, 4]
```

#### Task 6 - Insert an Item at the Bottom

<p align="justify">

Make a card appear by inserting a new card at the bottom of the stack. Return the adjusted stack.

</p>

```javascript
const newCard = 8;
insertItemAtBottom([5, 9, 7, 1], newCard);
// => [8, 5, 9, 7, 1]
```

#### Task 7 - Remove an Item from the Bottom

<p align="justify">

Make a card disappear by removing the card at the bottom of the stack. Return the adjusted stack.

</p>

```javascript
removeItemAtBottom([8, 5, 9, 7, 1]);
// => [5, 9, 7, 1]
```

#### Task 8 - Check the Size of the Stack

<p align="justify">

Check whether the size of the stack is equal to `stackSize` or not.

</p>

```javascript
const stackSize = 4;
checkSizeOfStack([3, 2, 6, 4, 8], stackSize);
// => false
```

### Solução

```
export function getItem(cards, position) {
  return cards[position];
}

export function getItem(cards, position) {
  return cards[position];
}

export function getItem(cards, position) {
  return cards[position];
}

export function removeItem(cards, position) {
  cards.splice(position, 1);
  return cards;
}

export function removeItemFromTop(cards) {
  cards.pop();
  return cards;
}

export function insertItemAtBottom(cards, newCard) {
  cards.unshift(newCard);
  return cards;
}

export function removeItemAtBottom(cards) {
  cards.shift();
  return cards;
}

export function checkSizeOfStack(cards, stackSize) {
  return cards.length == stackSize
  
}
```
