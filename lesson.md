# Bracket vs Dot Notation Lesson

## Learning Objectives
1. Access values in an object using bracket and dot notation
2. Identify when to use bracket notation vs dot notation 
3. Explain how JavaScript handles dot notation vs bracket notation

## Warm Up
Use [this Jam Board](https://jamboard.google.com/d/1nEAvHoxvjDAw7wqQDA1D8AlJ1jS-7vZD8gUQAOT5lDY/edit?usp=sharing) to tell me everything you know about dot and bracket notations.

Use page 2 to note any questions/confusion you have.

## Review the basics

<details>
<summary>Dot notation</summary>
<br>

- simple, clear way to access a value within an object when you know the exact text string of the key.  

```
var car = {
    make: "Honda",
    model: "Civic",
    year: 2003,
    color: "red"
};

console.log(car.color);
// "red"
```

</details>

<details>
<summary>Bracket notation</summary>
<br>

- used to access values in an object in more complex scenarios like when the key may be represented by a variable instead of the *exact text* string.  
    - **JavaScript evaluates whatever is between the brackets before going to find the value its looking for.**

```
var car = {`
    make: "Honda",
    model: "Civic",
    year: 2003,
    color: "red"
};

console.log(car["color"]);
// "red"

var carDetail = "color";
console.log(car[carDetail]);
// "red"
```

</details>

<details>
<summary>When can't you use dot notation and have to use bracket notation instead? </summary>
<br>

1. You don't have the exact text string of the key
1. You are using a variable/parameter to represent the key
1. The key is not a simple one-word string 
    1. Key is a number, [JS reserved word](https://www.edureka.co/blog/javascript-reserved-words/), symbol
    1. Key is multiple words with space(s) between

</details>

## Let's Party
Join the party by forking [this repl](https://repl.it/@hfaerber/Bracket-vs-Dot-Notation-Review-Sample-Lesson)

## Documentation
[Property Accessors - Bracket Notation & Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_Accessors): ways to access a value from an object
