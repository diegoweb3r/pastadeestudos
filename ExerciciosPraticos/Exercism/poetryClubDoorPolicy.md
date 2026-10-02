# Poetry Club Door Policy

### Instructions

#### Creating a String

<p align="justify">

A *string* is the JavaScript data type to store text data.

</p>

<p align="justify">

You create a string by wrapping the text in single quotes or double quotes. On Exercism, single quotes are used.

</p>

```javascript
'Hello, World!'
"Hello, World!"
```

#### Strings as Lists of Characters

<p align="justify">

A string can be treated as a list of characters where the first character has index `0`. You can access an individual character of the string using square brackets and the index of the letter you want to retrieve.

</p>

```javascript
'cat'[1];
// => 'a'
```

<p align="justify">

You can determine the number of characters in a string by accessing the `length` property.

</p>

```javascript
'cat'.length;
// => 3
```

#### Concatenation and Methods

<p align="justify">

The simplest way to concatenate strings is to use the addition operator `+`.

</p>

```javascript
'I like' + ' ' + 'cats.';
// => "I like cats."
```

<p align="justify">

Strings provide a lot of helper methods, see [**MDN Docs on String Methods**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#Instance_methods) for a full list. The following list shows some commonly used helpers.

</p>

* [**`toUpperCase`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase) and [**`toLowerCase`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase) - change the case of all characters
* [**`trim`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/Trim) - remove whitespace at the beginning and end
* [**`includes`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [**`startsWith`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/startsWith) and [**`endsWith`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/endsWith) - determine whether another string is part of the given string
* [**`slice`**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) - extract a section of the string

<p align="justify">

Strings are immutable in JavaScript. So a "modification", e.g. by some of the methods above, will always create a new string instead.

</p>

<p align="justify">

A new poetry club has opened in town, and you're thinking of attending. Because there have been incidents in the past, the club has a very specific door policy which you'll need to master, before attempting entry.

There are two doors at the poetry club, a front and a back door, and both are guarded. To gain entry, you'll need to work out the password of the day.

The password is always based on a poem and can be derived in a two-step process.

1. The guard will recite the poem, one line at a time and you have to respond with an appropriate letter of that line.
2. The guard will now tell you all the letters you responded with at once, and you need to write them down on a piece of paper in a specific format.

The details of the process depend on which door you are trying to enter.

</p>

#### Task 1 - Determine the front door response

<p align="justify">

To determine the letters for the front door password, you need to respond with the first letter of the line of the poem, that the guard recites to you.

To end up with a nice password, the members of the poetry club like to use *acrostic* poems. This means that the first letter of each sentence forms a word. Here is an example by one of their favorite writers Michael Lockwood.

</p>

```text
Stands so high
Huge hooves too
Impatiently waits for
Reins and harness
Eager to leave
```

<p align="justify">

So when the guard recites **Stands so high**, you'll respond **S**, when the guard recites **Huge hooves too**, you'll respond **H**.

Implement the function `frontDoorResponse` that takes a line of the poem as an argument and returns the first letter of that line.

</p>

```javascript
frontDoorResponse('Stands so high');
// => "S"
```

#### Task 2 - Determine the front door password

<p align="justify">

Now that you have all the correct letters, all you need to do to get the password for the front door is to correctly capitalize the word.

Implement the function `frontDoorPassword` that accepts a string (the combined letters you found in task 1) and returns it correctly capitalized.

</p>

```javascript
frontDoorPassword('SHIRE');
// => "Shire"

frontDoorPassword('shire');
// => "Shire"
```

#### Task 3 - Determine the back door response

<p align="justify">

To determine letters for the back door password, you need to respond with the last letter of the line of the poem that the guard recites to you.

The members of the poetry club are really clever. The poem mentioned before is also *telestich*, which means that the last letter of each sentence also forms a word:

</p>

```text
Stands so high
Huge hooves too
Impatiently waits for
Reins and harness
Eager to leave
```

<p align="justify">

When the guard recites **Stands so high**, you'll respond **h**, when the guard recites **Huge hooves too**, you'll respond **o**.

Note that sometimes the guard does stylistic pauses (in the form of whitespace) at the beginning or at the end of a line. You will need to ignore those pauses to derive the correct letter.

Implement the function `backDoorResponse` that takes a line of the poem as an argument and returns the last letter of that line that is not a whitespace character.

</p>

```javascript
backDoorResponse('Stands so high');
// => "h"

backDoorResponse('Stands so high   ');
// => "h"
```

#### Task 4 - Determine the back door password

<p align="justify">

To enter the poetry club via the back door, you need to be extra polite. So to derive the password, this time you need to correctly capitalize the word and add `', please'` at the end.

Implement the function `backDoorPassword` that accepts a string (the combined letters you found in task 3) and returns the polite version of the capitalized password.

</p>

```javascript
backDoorPassword('horse');
// => "Horse, please"
```

### Solução

```
export function frontDoorResponse(line) {
  return line[0];
}

export function frontDoorPassword(word) {
  return word[0].toUpperCase() + word.slice(1).toLowerCase();
}

export function backDoorResponse(line) {
 return line.trim().at(-1);
}

export function backDoorPassword(word) {
  return word[0].toUpperCase() + word.slice(1).toLowerCase() + ", please"
}
```
