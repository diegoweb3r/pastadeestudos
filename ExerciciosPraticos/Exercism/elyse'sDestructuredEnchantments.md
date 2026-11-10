# Elyse's Destructured Enchantments

### Instructions

### Array Destructuring

<p align="justify">JavaScript's array destructuring syntax is a concise way to extract values from an array and assign them to distinct variables.</p>

<p align="justify">In this example, each value in the <code>numberOfMoons</code> array is assigned to its corresponding planet:</p>

```javascript
const numberOfMoons = [0, 2, 14];

const [venus, mars, neptune] = numberOfMoons;

neptune;
// => 14
```

<p align="justify">In short:</p>

- The syntax allows for naming positioned elements in an array, as well as swapping variables using re-assignment.
- Destructuring syntax is available inside function parameters, and is available on any iterable.
- Leaving a position unnamed (by not writing any variable name) silently ignores that position.

### Object Destructuring

<p align="justify">In JavaScript, there is also destructuring syntax to extract properties from an object and assign them to distinct variables.</p>

<p align="justify">In this example, weather symbols are extracted from the object <code>weather</code>:</p>

```javascript
const weather = {
  sun: '☀️',
  sun_behind_small_cloud: '🌤️',
  sun_behind_cloud: '⛅',
  sun_behind_large_cloud: '🌥️',
  sun_behind_rain_cloud: '🌦️',
  cloud: '☁️',
  cloud_with_rain: '🌧️',
  cloud_with_snow: '🌨️',
  cloud_with_lightning: '🌩️',
  cloud_with_lightning_and_rain: '⛈️',
};

const { sun, cloud, cloud_with_lightning: thunder } = weather;

sun;
// => '☀️'

cloud;
// => '☁️'

thunder;
// => '🌩️'
```

<p align="justify">In short:</p>

- The syntax allows for both extracting properties as well as extracting and renaming them.
- Destructuring syntax is available inside function parameters.

### General Instructions

<p align="justify">Elyse, magician-to-be, continues her training. She has a deck of cards she wants to manipulate.</p>

<p align="justify">To make things easier, she usually only starts with cards numbered 2 to 10, although some of the tricks may involve additional (face) cards.</p>

#### Important Note

<p align="justify">There are many ways to shuffle the cards around, but to keep up the illusion of magic, it is vital that no single method is used. For example, Elyse doesn't use <code>splice</code>, <code>slice</code>, <code>shift</code>, <code>unshift</code>, <code>push</code>, or <code>at</code>.</p>

<p align="justify">The array accessor <code>array[index]</code> and object accessor (<code>object[key]</code> and <code>object.key</code>) are also never to be used.</p>

### Advanced

<p align="justify">Every function can be implemented using the parameters and a function body with a single return expression.</p>

### Task 1 - Get First Card

<p align="justify">Elyse will summon the first card in the deck without using the <code>array[index]</code>, <code>.at(index)</code>, or <code>.shift()</code>. It's just like magic.</p>

```javascript
const deck = [5, 9, 7, 1, 8];

getFirstCard(deck);
// => 5
```

### Task 2 - Get Second Card

<p align="justify">Elyse performs sleight of hand and summons the second card in the deck without using the <code>array[index]</code> or <code>.shift()</code>.</p>

```javascript
const deck = [3, 2, 10, 6, 7];

getSecondCard(deck);
// => 2
```

### Task 3 - Swap Two Cards

<p align="justify">Elyse will make the two cards of the deck switch places. She doesn't need to call a single function.</p>

```javascript
const deck = [10, 7];

swapTwoCards(deck);
// => [7, 10]
```

### Task 4 - Shift Three Cards Around

<p align="justify">In order to perform some more sleight of hand, Elyse takes three cards and quickly moves the top card to the back, making the middle card the first card and the old bottom card the middle card. She doesn't need to call a single function.</p>

```javascript
const deck = [2, 6, 10];

shiftThreeCardsAround(deck);
// => [6, 10, 2]
```

### Task 5 - Pick Named Pile

<p align="justify">Elyse will separate the deck into two piles. She then asks the observer to pick one of the two piles, which we'll name <code>chosen</code>. The disregarded pile is no longer relevant, which she makes disappear. She doesn't need to call a single function.</p>

```javascript
const deck = [5, 4, 7, 10];

const chosen = [5, 4];
const disregarded = [7, 10];

pickNamedPile({ chosen, disregarded });
// => [5, 4]
```

### Task 6 - Swap Named Piles

<p align="justify">Unfortunately the observer keeps picking the "wrong" pile, but with some clever fast magic, Elyse renames the chosen pile to be disregarded and the disregarded pile to be the chosen pile. She doesn't need to call a single function.</p>

```javascript
const deck = [5, 4, 7, 10];

const chosen = [5, 4];
const disregarded = [7, 10];

swapNamedPile({ chosen, disregarded });
// => { chosen: [7, 10], disregarded: [5, 4] }
```

### Solução

```
export function getFirstCard(deck) {
  const [firstCard, secondCard, thirdCard] = deck;
  return firstCard;
}

export function getSecondCard(deck) {
  const [firstCard, secondCard, thirdCard] = deck;
  return secondCard;
}

export function swapTwoCards(deck) {
  let [firstCard, secondCard] = deck;
  [firstCard, secondCard] = [secondCard, firstCard];
  const newDeck = [firstCard, secondCard];
  return newDeck;
}

export function shiftThreeCardsAround(deck) {
  let [topCard, middleCard, bottomCard] = deck;
  [topCard, middleCard, bottomCard] = [middleCard, bottomCard, topCard];
  const newDeck = [topCard, middleCard, bottomCard];
  return newDeck;
}

export function pickNamedPile(piles) {
  // 🚨 Do NOT use piles.chosen or piles.disregarded.
  const {chosen, disgregarded} = piles;
  return chosen;
}

export function swapNamedPile(piles) {
  // 🪄 Don't break the magic.
  // 🚨 Do NOT use piles.chosen or piles.disregarded.
  // 🚨 Do NOT touch the next line or Elyse will accidentally reveal the trick.
  const {chosen: disregarded, disregarded: chosen} = piles;
  return { chosen, disregarded };
}

```