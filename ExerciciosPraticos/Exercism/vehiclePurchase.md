# Vehicle Purchase

### Instructions

### Introduction

#### Comparison

<p align="justify">

In JavaScript, numbers can be compared using the following relational and equality operators.

</p>

| **Comparison**         | **Operator** |
| :--------------------- | :----------- |
| Greater than           | `a > b`      |
| Greater than or equals | `a >= b`     |
| Less than              | `a < b`      |
| Less than or equals    | `a <= b`     |
| (Strict) Equals        | `a === b`    |
| Not (strict) equals    | `a !== b`    |

<p align="justify">

The comparison result is always a boolean value: `true` or `false`.

</p>

```javascript
1 < 3;
// => true

2 !== 2;
// => false

1 === 1.0;
// => true
// All numbers are floating-points, so this is different syntax for
// the exact same value.
```

<p align="justify">

In JavaScript, the comparison operators above can also be used to compare strings. In that case, a dictionary (lexicographical) order is applied.

</p>

```javascript
'Apple' > 'Pear';
// => false

'a' < 'above';
// => true

'a' === 'A';
// => false
```

#### Conditionals

<p align="justify">

A common way to conditionally execute logic in JavaScript is the `if` statement. It consists of the `if` keyword, a condition wrapped in round brackets and a code block wrapped in curly brackets. The code block will only be executed if the condition evaluates to `true`.

</p>

```javascript
if (condition) {
  // code that is executed if "condition" is true
}
```

<p align="justify">

It can be used stand-alone or combined with the `else` keyword.

</p>

```javascript
if (condition) {
  // code that is executed if "condition" is true
} else {
  // code that is executed otherwise
}
```

<p align="justify">

To nest another condition into the `else` statement, you can use `else if`.

</p>

```javascript
if (condition1) {
  // code that is executed if "condition1" is true
} else if (condition2) {
  // code that is executed if "condition2" is true
  // but "condition1" was false
} else {
  // code that is executed otherwise
}
```

### Task 1 - Determine if a License is Needed

<p align="justify">

In this exercise, you will write some code to help you prepare to buy a vehicle.

</p>

<p align="justify">

You have three tasks, one to determine if you will need to get a license, one to help you choose between two vehicles and one to estimate the acceptable price for a used vehicle.

</p>

<p align="justify">

Some kinds of vehicles require a driver's license to operate them. Assume only the kinds `'car'` and `'truck'` require a license, everything else can be operated without a license.

</p>

<p align="justify">

Implement the `needsLicense(kind)` function that takes the kind of vehicle and returns a boolean indicating whether you need a license for that kind of vehicle.

</p>

```javascript
needsLicense('car');
// => true

needsLicense('bike');
// => false
```

### Task 2 - Choose Between Two Vehicles

<p align="justify">

You evaluate your options of available vehicles. You manage to narrow it down to two options but you need help making the final decision.

</p>

<p align="justify">

Implement the function `chooseVehicle(option1, option2)` that takes two vehicles as arguments and returns a decision that includes the option that comes first in dictionary order.

</p>

```javascript
chooseVehicle('Wuling Hongguang', 'Toyota Corolla');
// => 'Toyota Corolla is clearly the better choice.'

chooseVehicle('Volkswagen Beetle', 'Volkswagen Golf');
// => 'Volkswagen Beetle is clearly the better choice.'
```

### Task 3 - Calculate the Resell Price

<p align="justify">

Now that you made your decision you want to make sure you get a fair price at the dealership. Since you are interested in buying a used vehicle, the price depends on how old the vehicle is.

</p>

<p align="justify">

For a rough estimate, assume if the vehicle is less than 3 years old, it costs 80% of the original price it had when it was brand new.

</p>

<p align="justify">

If it is more than 10 years old, it costs 50%.

</p>

<p align="justify">

If the vehicle is at least 3 years old but not older than 10 years, it costs 70% of the original price.

</p>

<p align="justify">

Implement the `calculateResellPrice(originalPrice, age)` function that applies this logic using `if`, `else if` and `else` (there are other ways if you want to practice).

</p>

```javascript
calculateResellPrice(1000, 1);
// => 800

calculateResellPrice(1000, 5);
// => 700

calculateResellPrice(1000, 15);
// => 500
```

### Solução

```
export function needsLicense(kind) {
  if (kind == 'car' || kind == 'truck'){
    return true
  } else{
    return false
  };
}

export function chooseVehicle(option1, option2) {
  if(option1 < option2){
    return option1 + " is clearly the better choice."
  } else{
    return option2 + " is clearly the better choice."
  };
}

export function calculateResellPrice(originalPrice, age) {
  if (age < 3){
    return originalPrice * 0.8;
  } else if(age >= 3 && age <= 10){
    return originalPrice * 0.7;
  } else{
    return originalPrice * 0.5;
  }
}
```
