# Bracket vs Dot Notation Lesson

## Learning Objectives
1. Access values from an object using bracket and dot notation
2. Identify when to use bracket vs dot notation
3. Leverage understanding of bracket and dot notation to refactor for DRYer code

## Vocab
1. Object: a grouping/unit of related key-value pairs (properties).
2. [Property Accessors - Bracket Notation & Dot Notation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_Accessors): ways to access a value from an object
3. [Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys): a method that returns an object's keys in an array.  Our secret weapon to be able to iterate over an *object*.
4. [Array prototype method `find()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find): a method that iterates over an array and returns the first element that meets the condition set in the method's callback function. 
5. Parameters & Arguments:  essentially variables that are being declared and assigned directly in a function's declaration (parameter) and it's invocation (argument)

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
In your breakout rooms, go through each Learning Objective and explain what you've learned.  Post any remaining questions/confusion to the chat.
