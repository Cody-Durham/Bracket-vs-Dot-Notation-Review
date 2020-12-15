# Bracket vs Dot Notation Lesson

## Learning Objectives
1. Identify when to use bracket vs dot notation to access values in an object
2. Explain how JavaScript handles dot notation vs bracket notation
3. Leverage your understanding of bracket & dot notation alongside other tools

## Other Tools
1. [Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys): a method that returns an object's keys in an array.  Our secret weapon to be able to iterate over an *object*.
2. Parameters & Arguments are essentially variables that you declare and assign directly in a function's declaration (parameter) and it's invocation (argument)

## Warm Up
Use [this Jam Board](https://jamboard.google.com/d/1nEAvHoxvjDAw7wqQDA1D8AlJ1jS-7vZD8gUQAOT5lDY/edit?usp=sharing) to tell me everything you know about dot and bracket notations.

List any questions/confusion you have on page 2.

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
Follow along with [this repl](https://repl.it/@hfaerber/Bracket-vs-Dot-Notation-Review-Sample-Lesson) as we access some values.
## Check for understanding

## Documentation
1. [Property Accessors - Bracket Notation & Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_Accessors): ways to access a value from an object