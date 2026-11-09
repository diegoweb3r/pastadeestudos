# Elyse's Enchantments

### Instructions

### Arrow Functions

<p align="justify">Besides function declarations and function expressions, JavaScript also has another very concise syntax for defining a function. These functions are called arrow functions.</p>

<p align="justify">Here is a comparison between a function declaration and an arrow function:</p>

```javascript
function addUpTwoNumbers(num1, num2) {
  return num1 + num2;
}

// function keyword removed and => added

const addUpTwoNumbers = (num1, num2) => {
  return num1 + num2;
};
```

<p align="justify">If the function body contains only a return statement, like in the example above, the <code>{}</code> and the <code>return</code> keyword can be omitted. If there is only one parameter, the parenthesis <code>()</code> can be omitted as well.</p>

```javascript
const addUpTwoNumbers = (num1, num2) => num1 + num2;

const square = num => num * num;
```

<p align="justify">Arrow functions are often used to define short callback functions directly in the function call.</p>

```javascript
applyToSquare(number => number * number);
```

### Array Analysis

<p align="justify">Arrays have built-in methods to analyse the contents of the array. Most of these methods take a function that returns <code>true</code> or <code>false</code> as an argument. Such a function is called a predicate.</p>

<p align="justify">The built-in methods are meant to be used instead of a <code>for</code> loop or the built-in <code>forEach</code> method.</p>

#### Example of analysis using a for loop

```javascript
const numbers = [1, 'two', 3, 'four'];

for (var i = 0; i < numbers.length; i++) {
  if (numbers[i] === 'two') {
    return i;
  }
}
// => 1
```

#### Example of analysis using a built-in method

```javascript
const numbers = [1, 'two', 3, 'four'];

numbers.indexOf('two');
// => 1
```

<p align="justify">Some other helpful built-in methods that are available to analyse an array are shown below. See MDN for a full list of array methods.</p>

#### includes

<p align="justify">The <code>includes(value)</code> method determines whether an array includes a certain value. It returns <code>true</code> when the value is included, <code>false</code> otherwise.</p>

```javascript
const numbers = [1, 'two', 3, 'four'];

numbers.includes(1);
// => true

numbers.includes('one');
// => false
```

#### every

<p align="justify">The <code>every(predicate)</code> method takes a function which is a predicate. It tests whether all elements in the array return <code>true</code> when passed to the predicate. In other words, the method tests that all its elements pass the test passed to the function call. It returns <code>true</code> when every element passes the predicate test, <code>false</code> otherwise.</p>

```javascript
const numbers = [1, 3, 5, 7, 9];

numbers.every((num) => num % 2 !== 0);
// => true
```

#### some

<p align="justify">The <code>some(predicate)</code> method is the same as the <code>every</code> method, but returns <code>true</code> if at least one item in the array passes the predicate test.</p>

```javascript
const numbers = [1, 3, 5, 7, 9];

numbers.some((num) => num % 2 !== 0);
// => true
```

#### find

<p align="justify">The <code>find(predicate)</code> method returns the value of the first element in the array that passes the predicate test. Where <code>some()</code> returns <code>true</code> when it passes, <code>find()</code> returns the actual value in the array. The method returns <code>undefined</code> when none of the elements in the array pass the predicate test.</p>

```javascript
const numbers = [1, 3, 5, 7, 9];

numbers.find((num) => num < 5);
// => 1
```

#### findIndex

<p align="justify">The <code>findIndex(predicate)</code> method is the same as the <code>find()</code> method, but it returns the (first) index of the element that passes the predicate test instead of the value. The method returns <code>-1</code> when none of the elements in the array pass the predicate test.</p>

```javascript
const numbers = [1, 3, 5, 7, 9];

numbers.findIndex((num) => num > 7);
// => 4

numbers.findIndex((num) => num > 9);
// => -1
```

### Task 1 - Get Card Position

<p align="justify">Elyse, magician-to-be, continues her training. She will be given several stacks of cards that she needs to perform her tricks. To make things a bit easier, she only uses the cards 1 to 10.</p>

<p align="justify">In this exercise, use built-in methods to analyse the contents of an array.</p>

<p align="justify">Elyse wants to know the position (index) of a card in the stack.</p>

```javascript
const card = 2;

getCardPosition([9, 7, 3, 2], card);
// => 3
```

### Task 2 - Check if Stack Includes Card

<p align="justify">Elyse wants to determine if a card is present in the stack — in other words, if the stack contains a specific number.</p>

```javascript
const card = 3;

doesStackIncludeCard([2, 3, 4, 5], card);
// => true
```

### Task 3 - Check if Each Card is Even

<p align="justify">Elyse wants to know if every card is even — in other words, if each number in the stack is an even number.</p>

```javascript
isEachCardEven([2, 4, 6, 7]);
// => false
```

### Task 4 - Check if Stack Includes an Odd Card

<p align="justify">Elyse wants to know if there is an odd number in the stack.</p>

```javascript
doesStackIncludeOddCard([3, 2, 6, 4, 8]);
// => true
```

### Task 5 - Get First Odd Card

<p align="justify">Elyse wants to know the value of the first card that is odd.</p>

```javascript
getFirstOddCard([4, 2, 8, 7, 9]);
// => 7
```

### Task 6 - Get First Even Card Position

<p align="justify">Elyse wants to know the position of the first card that is even.</p>

```javascript
getFirstEvenCardPosition([5, 2, 3, 1]);
// => 1
```

### Solução

```
export function getCardPosition(stack, card) {
  return stack.findIndex((item) => item == card);
}

export function doesStackIncludeCard(stack, card) {
  return stack.includes(card);
}

export function isEachCardEven(stack) {
  return stack.every((item) => item % 2 == 0);
}

export function doesStackIncludeOddCard(stack) {
  return stack.some((item) => item % 2 !== 0);
}

export function getFirstOddCard(stack) {
  return stack.find((item) => item % 2 !== 0);
}

export function getFirstEvenCardPosition(stack) {
 return stack.findIndex((item) => item % 2 == 0);
}

```