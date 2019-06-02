# [Javascript Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations)



------

## What is a variable?

We all remember variables in algebra; Solve for x!

 `y = mx + b` If you ever came across this equation then you've seen variables!

- In programming variables are not much different than in math.



- In programming variables can be much more than just numbers.



- Variables represent different data types like: strings, arrays, objects.



- There are many ways to declare variables, one declaration you will come across frequently in JavaScript is `let`:

`let variableName = "the variable"`



there are other ways to declare variables like:

```javascript
const name = "Luke"
var lastName = "Skywalker"
let names = ["Luke", "Yoda", "Obi Wan"]
```

You may notice variables are written in "camelCase" this is the most commonly used syntax for variable naming in JavaScript.
There is also "snake_case" which is the standard in other languages like Python and Ruby.

Neither way is wrong or right, they are merely standards that programmers have accepted as convention.

The different ways of declaring variables affect the "scope" (global scope, function scope, block scope) of each variable, scope is a difficult concept to understand off the bat, just remember there is a pretty sizable difference between the three declaration types.

### Here is a great [article and video](https://tylermcginnis.com/var-let-const/) to help you understand the difference between var, let and const.

### Now let's put those variables to use!

### Docs: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations

---

# Exercise

1. Open up a JavaScript repl.it



2. Copy this code into your repl, before clicking "run", what do you think will be displayed in your console?:
  ```javascript
  let name = "Luke"
  let lastName = "Skywalker"
  let names = ["Luke", "Yoda", "Obi Wan"]
  console.log(name)
  ```



3. Change the name `"Luke"` to your name and click run



4. Change the variable within the parenthesis of the `console.log` so that the console displays "Skywalker"



5. Replace the `console.log(name)` with `console.log(names[0])`
  - What happened there? You printed the first item of the `names` array. Don't worry, we will go into much more detail about arrays later, this is merely a sample.



6. Now let's `console.log` a sentence that includes your name. Copy and paste this code:

  ```javascript
  let name = "YOUR NAME HERE"
  console.log(`Hello ${name}! Thanks for coming to Stripe Foundations!`)
  ```

  - What happened here? We used a [Template-Literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) to weave the *name* variable into a sentence and print it to your console.
  - There is a lot happening here at once so don't worry if you're a little overwhelmed with information. We'll break things down further for a better understanding, but for now these exercises will help you get comfortable with JavaScript.
