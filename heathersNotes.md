
Bracket and Dot notation makes a lot of sense initially.

if you know the exact text/string key that you are trying to get the value for, you use dot notation
If you dont know the exact key or that key might change or you are using a variablet or represent that key, you use bracket notation.

Anytime you can dot notation, you could use bracket instead. Sometimes, bracket notation is the only option.

I remember this all making perfect sense during and even after the lesson at Turing, but getting messy and confusing later when I tried to implement it in more complex scenarios than the lesson covered. I understood it, but only in this silo. It was hard put it to use in real code.

There is no top secret, unground info I can give you today about bracket vs dot notation. But what we can do today is look at some scenarios from project you may have done that give a chance to bring your existing knowledge and understanding a bit deeper by focusing on how we can leverage dot and bracket notation to refactor code to be cleaner, dryer and more efficient. Typically these refactoring opportunities may hand in hand with parameters and arguments. So we will quick review bracket and dot notation AND parameters and arguments then slow down a bit and work through some code examples together for bulk of this lesson.

# Bracket vs Dot Notation Lesson

### Notes

Object - a group, unit, bundle, pile, collection of related key-value pairs (properties).
Key - the name used to access that key's value. Like when you declare a variable and assigned it a value
Value - The value, duh

To access a value that lives as part of an object, we can use two tools - Bracket or Dot Notation

What does that look like?

```
Const recipe = {
    name: "Puppy Chow",
    type: ["dessert", "snack", "holiday treat"],
    ingredients: {
        chex: "1 cup",
        choc chips: "1 cup",
        peanut butter: : "1 cup",
        vanilla: "1 cup",
        powderedSugar: : "1 cup".  ***do i want to show a 2 word key?***
    }
    time: "20 minutes"
}

Have them open a repl? or just think about it?
**How would you access the name of the recipe using dot notation?**
    - console.log(recipe.name)
**How would you access the name of the recipe using bracket notation?
    - console.log(recipe[name])
    - look at the error message in repl
        - ReferenceError: hobbies is not defined
    at /home/runner/Dot-Notation-Practice-1/index.js:25:19
    at Script.runInContext (vm.js:130:18)
    at Object.<anonymous> (/run_dir/interp.js:209:20)
    at Module._compile (internal/modules/cjs/loader.js:1137:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1157:10)
    at Module.load (internal/modules/cjs/loader.js:985:32)
    at Function.Module._load (internal/modules/cjs/loader.js:878:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:71:12)
    at internal/main/run_main_module.js:17:47Hint: hit control+c anytime to enter REPL.

      - have you seen a similar error before? when?  what does it mean?
      - why doesn't this work?
    - console.log(recipe.['name'])
      - interesting, if you are using the exact text of the object's key in bracket notation, you have to quote it like a string.   seems GROSS

Can you combine dot and bracket notation?
Which do you personally like better?  Why?
So when CANT you use dot notation?
When CANT you use bracket notation?

Dot notation - simple, clean, literal

Bracket notation - can handle more complexity. flexible.  variables.  JS evaluates what is in the brackets before going to find that key's value

ask them prefer concatenation or interpolation.

for loop practice is good but i think i want to show them something in the brackets that isnt just [i]

Example ideas
Access something using dot.
Access something using bracket based on the parameter passed

Add a property using dot.  Add a property using bracket notation based on a parameter passed

##Parameters and Arguments
  Essentially just variables that you are declaring and passing directly to a function/method.

```

https://repl.it/@hfaerber/LessonPrepHF#index.js

1- you cant always access every variable due to scope

What to cover?
-JS is evaluating inside the brackets first

-   accessing
-   adding properties
-   when dot notation doesn't work - number, keys with two words, etc

-   Refactor to use Param/Arg
-   Refactor to DRY 3 for loops into 1
-   Refactor to add para so that function can be used for more than just title
-   On your own example

Try it with dot first, will it work? get the error - why? fix with bracket notation

[Dot Notation & Bracket Notation - Property accessors](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_Accessors)
Parameters/Arguments
[find() array prototype method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
[Object.keys() method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)

INTROs
-students only : name, pronouns, module, which is their preference/default? bracket or dot notation


Ask them to explain the diff.  
Ask them to add to the chat when you mUST use bracket

When I go to the recipe REPL

1. review the example
- Why is public blue?
- why is 100 green?
- why are their quotes arond the nested object's keys? (console.log(recipe)to see that some are in quotes)

2. For each thing, ask 
- give me a thumbs up if you think it will work

3. after recipe[name] fails, read the error, put quotes, say its gross, expplain that quotes within the brackets is a clue to use dot notation 