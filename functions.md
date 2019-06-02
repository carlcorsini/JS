# JavaScript Functions

---

### Functions are a fundamental building block to JavaScript

### Functions are like a set of instructions or directions

### Let's think about if we were giving our friend Stephen directions to our favorite Irish Pub: _Kate Murphy's_ in San Francisco:

```
hey, Stephen

go straight

turn left in 2 blocks

go straight

turn right in 4 blocks

arrive at destination
```

### Now let's break those directions down into "Pseudo Code", a great practice for solving programming challenges

```javascript
let user = "Stephen"

let blocks = 6

initiate walk loop

if user walks 2 blocks: turn left

if user walks 6 blocks: turn right

if user arrives at "Kate Murphy's": enter & purchase french fries
```

### Now lets write what the function may look like in JavaScript

### *We are assuming the user variable has a few made up methods like direction and purchase, so don't try to copy and paste this code into a repl, it won't work*

```javascript
function directions(user) {
  let blocks = [1, 2, 3, 4, 5, 6]

  for (let i = 0; i < blocks.length; i++) {
    if (blocks[i] === 2) {
      user.direction = 'left'
    } else if (blocks[i] === 6) {
      user.direction = 'right'
    }

    user.purchase('french fries')

    return user
  }
}
```

---

## Declaration

* There are multiple ways to declare functions.
* For now we will focus on the ES5 style, but we will also introduce the most current ES6 functional declaration.
* Feel free to use either one, you may like the newer style more, but it is important to understand both kinds of declarations.

### ES5 Functions

#### Syntax for an ES5 function:

```javascript
function sayMessage(parameter) {
  console.log(parameter)
  return parameter
}

sayMessage('Hello World!')
```

### ES6 "Fat-Arrow" Functions

#### Syntax for an ES6 function:

```javascript
let sayMessage = parameter => {
  console.log(parameter)
  return parameter
}

sayMessage('Hello World!')
```

### Compare the two declarations side by side, in ES6 you no longer need to write the word "function" in order to declare a function.

### Some important components of a function to understand:


* **Function Name**
  * in *ES5* it is the variable name right after the word function, this is a variable that represents the function you are creating
  * in *ES6* the function name is after the `let` the same way you would declare any other variable



* **Parameter**
  * Labeled "parameter" in the example `sayMessage()` function
  * its purpose is the **input** of the function
  * what ever you place between the parenthesis after the function name will be accessible within the code block
  * functions may have an infinite amount of parameters



- **Code Block**
  * The code block is what lies within the `{}` after the parameter
  * This is where the logic of your function will reside.
  * Usually a function will end with a **return** statement, although it does not have to.
  * The return statement is the **output** of the function.
  * Within this example we are console logging the parameter, then returning the parameter.
  * What is the difference between `console.log` and **return**?



* **Invocation** `sayMessage('Your Message Here')`
  * Lastly to invoke a function means "calling" a function you've created.
  * By placing a message string within the parenthesis of our `sayMessage` function, we will initiate the function.
  * the `'Your Message Here'` string is called the **argument** when invoking a function
  * When writing a function we call that area of a function the **parameter**, but when invoking a function it is referred to as the **argument**

### Docs: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions

---

# Exercise

1.  Open a JS repl.it



2.  Copy and paste this code:
    ```javascript
    function sayMessage(parameter) {
      console.log(parameter)
      return parameter
    }

    sayMessage('Hello World!')
    ```
    - change the string, notice how the word `parameter` is simply a variable that represents the argument passed into the function
    - try creating a variable and passing that variable in as an **argument** rather than the `'Hello World!'` string
    - change the name of the `parameter` variable to whatever you like, notice how the function still runs, no matter what you name your parameter



2.  Create a function that takes 2 numbers as the input, finds the sum, and returns the sum as the output



3.  Create a function that take an array as the input, and returns the sum of the array as the output



4.  Create a function that takes a a number as the input, and returns true if the number is found in the following array:

    `[0, 1, 2, 4, 5, 9, 11, 12, 21, 23, 28, 30, 32, 34, 35]`



5.  Create a function that takes a number as an input and returns the players **full name** if found in the following **array** of **objects** named **gsw**:
  - **BONUS**: Create a function that takes a **string** representing a player's *position* as the input and return an array with all player's who play that position as the output
  - **BONUS**: Create a function that searches through this array of objects in another way and share it with your neighbor!

```javascript
let gsw = [
  { firstName: 'Demarcus', lastName: 'Cousins', position: ['C'], number: 0 },
  { firstName: 'Damion', lastName: 'Lee', position: ['G'], number: 1 },
  { firstName: 'Jordan', lastName: 'Bell', position: ['F'], number: 2 },
  { firstName: 'Quinn', lastName: 'Cook', position: ['PG'], number: 4 },
  { firstName: 'Kevon', lastName: 'Looney', position: ['C'], number: 5 },
  { firstName: 'Andre', lastName: 'Igoudala', position: ['G', 'F'], number: 9 },
  { firstName: 'Klay', lastName: 'Thompson', position: ['G'], number: 11 },
  { firstName: 'Andrew', lastName: 'Bogut', position: ['C'], number: 12 },
  { firstName: 'Jonas', lastName: 'Jerebko', position: ['F'], number: 21 },
  { firstName: 'Draymond', lastName: 'Green', position: ['F'], number: 23 },
  { firstName: 'Alfonzo', lastName: 'McKinnie', position: ['F'], number: 28 },
  { firstName: 'Marcus', lastName: 'Derrickson', position: ['F'], number: 32 },
  { firstName: 'Shaun', lastName: 'Livingston', position: ['G'], number: 34 },
  { firstName: 'Kevin', lastName: 'Durant', position: ['F'], number: 35 },
]
```
