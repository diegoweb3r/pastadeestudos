# Fun with Numbers

### Instructions

#### Type Conversion

<p align="justify">JavaScript does not have a construct to cast into a (different) type like many other languages but some built-in helpers can be used instead. Most notably, <code>Boolean</code>, <code>Number</code> and <code>String</code> can be used as functions to convert a value to the respective type.</p>

#### Converting to a Boolean (Truthy/Falsy Values)

<p align="justify">With <code>Boolean(value)</code> you can convert any value to a boolean. There is a fixed set of values, so called <em>falsy</em> values, that convert to <code>false</code>. Most importantly, <code>false</code>, <code>0</code>, empty string, <code>null</code>, <code>undefined</code> and <code>NaN</code> are falsy.</p>

<p align="justify">For all other values, <code>Boolean</code> returns <code>true</code>. These values are called <em>truthy</em>.</p>

```javascript
Boolean(-1);
// => true

Boolean(0);
// => false

Boolean(' ');
// => true

Boolean('');
// => false
```

<p align="justify">Note that because of the described rules, <code>'0'</code>, <code>'false'</code>, <code>[]</code> and <code>{}</code> are <strong>truthy</strong> in JavaScript.</p>

#### Converting to a Number

<p align="justify"><code>Number(value)</code> can be used to convert a value to a number. Whitespaces at the beginning and the end of a string are ignored and an empty string is converted to <code>0</code>. If you try to convert a non-primitive value or a string that does not represent a number, the result is <code>NaN</code> (<em>Not-A-Number</em>).</p>

```javascript
Number('  -12.34  ');
// => -12.34

Number('1,2');
// => NaN

Number('');
// => 0

Number({ num: 123 });
// => NaN
```

#### Converting to a String

<p align="justify">With <code>String(value)</code> you can convert a value to a string. The result is what you would expect it to be for primitive values.</p>

```javascript
String(12.34);
// => '12.34'

String(false);
// => 'false'

String(null);
// => 'null'

String(undefined);
// => 'undefined'
```

<p align="justify">For arrays, the <code>String</code> function will apply the string conversion for each element and join the results with a comma. You can also apply the <code>join</code> method yourself to customize the separator. Note that in these cases <code>null</code> and <code>undefined</code> will be converted to an empty string.</p>

```javascript
String([42, null, true, 'abc']);
// => '42,,true,abc'
```

<p align="justify">For objects, by default <code>String</code> returns an unhelpful text.</p>

```javascript
String({ key: 'value' });
// => '[object Object]'
```

#### Type Coercion

<p align="justify">In certain contexts, JavaScript will automatically convert a value to another data type before it evaluates some statement. This implicit conversion is called <em>type coercion</em>.</p>

#### Boolean Context

<p align="justify">When a non-boolean value is used in a boolean context, JavaScript will apply the same rules as the <code>Boolean</code> function to implicitly convert the value.</p>

<p align="justify">Coercion to boolean commonly occurs for:</p>

* the condition of an <code>if</code> statement;
* the first operand of the ternary operator <code>?</code>;
* the operand of the logical NOT operator <code>!</code>;
* the operands of the logical AND <code>&&</code> and OR <code>||</code> operators.

```javascript
const num = 0;

if (num) {
  // this block is NOT executed because 0 is falsy
}
```

#### String Context

<p align="justify">If the addition operator <code>+</code> is used for primitive values and one operand is a string, the other one will be coerced into a string as well. The conversion logic is the same as when using the <code>String</code> function. Afterwards, the two strings are concatenated.</p>

```javascript
let name;

'hello ' + name;
// => 'hello undefined'
```

#### Numeric Context

<p align="justify">Many operators coerce the operands into numbers according to the logic of the <code>Number</code> function explained above.</p>

<ul>
<li>Arithmetic operators: <code>+</code> (if no string is involved), <code>-</code>, <code>*</code>, <code>/</code>, <code>%</code>, <code>**</code></li>
<li>Unary plus and unary negation operators: <code>+</code>, <code>-</code></li>
<li>Relational operators (for non-string operands): <code>&gt;</code>, <code>&gt;=</code>, <code>&lt;</code>, <code>&lt;=</code></li>
<li>Bitwise operators: <code>|</code>, <code>&amp;</code>, <code>^</code>, <code>~</code></li>
</ul>

<p align="justify">To avoid mistakes, it is good practice to always call <code>Number</code> explicitly before applying those operators.</p>

#### Task 1 - Sum of Two Numbers

<p align="justify">One of the games on Kojo's website looks like a slot machine that shows two groups of wheels with digits on them. Each group of digits represents a number. For the game mechanics, Kojo needs to know the sum of those two numbers.</p>

<p align="justify">Write a function <code>twoSum</code> that accepts two arrays as parameters. Each array consists of one or more numbers between 0 and 9. The function should interpret each array as a number and return the sum of those two numbers.</p>

```javascript
twoSum([1, 2, 3], [0, 7]);
// => 130

// [1, 2, 3] represents 123 and [0, 7] represents 7.
// 123 + 7 = 130
```

#### Task 2 - Lucky Numbers

<p align="justify">Another game on the website is a little quiz called "Lucky Numbers". A user can enter a number and then sees whether the number belongs to some secret sequence or pattern. The sequence or pattern of the "lucky numbers" changes each month and each user only has a limited number of tries to guess it.</p>

<p align="justify">This month's lucky numbers should be numbers that are palindromes. Palindromic numbers remain the same when the digits are reversed.</p>

<p align="justify">Implement the new <code>luckyNumber</code> function that accepts a number as a parameter. The function should return <code>true</code> if the number is a palindrome and <code>false</code> otherwise. The input number will always be a positive integer.</p>

```javascript
luckyNumber(1441);
// => true

luckyNumber(123);
// => false
```

#### Task 3 - Error Message

<p align="justify">In various places on the website, there are input fields where the users can enter numbers and click a button to trigger some action. Kojo wants to improve the user experience of his site. He wants to show an error message in case the user clicks the button but the field contains an invalid input value.</p>

<p align="justify">If the user types something into a field, the associated value is always a string even if the user only typed in numbers.</p>

<p align="justify">If the user types something but deletes it again, the variable will be an empty string.</p>

<p align="justify">Before the user even started typing, the variable can be <code>undefined</code> or <code>null</code>.</p>

<p align="justify">Write a function <code>errorMessage</code> that accepts the user input as a parameter.</p>

<p align="justify">If the user did not provide any input, <code>errorMessage</code> should return <code>'Required field'</code>.</p>

<p align="justify">If the input does not represent a non-zero number, according to the JavaScript conversion rules, <code>'Must be a number besides 0'</code> should be returned.</p>

<p align="justify">In all other cases, you can assume the input is valid, and the return value should be an empty string.</p>

```javascript
errorMessage('123');
// => ''

errorMessage('');
// => 'Required field'

errorMessage('abc');
// => 'Must be a number besides 0'
```

### Solução

```


```
