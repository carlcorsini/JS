# [Conditional Statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Conditional_statements)

------

In JavaScript you will come across **conditions** in which:
  - if one statement is **true**, run a set of instructions
  - if another this is **true**, run a different set of instructions.
  - **otherwise**, run another set of instructions

A lot of programming boils down to this logical idea.

There are different types of **Conditional Statements** including [`if else`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statements, [`switch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch) statements and the [`ternary`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) operator

We will focus on the `if else` statement for now

## [If, Else Statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)

### Syntax:

```javascript
if (condition) {

  do something

} else if (another condition) {

  do something else

} else {

  otherwise do something else

}
```

Every `if else` statement must start with **if**, followed by parenthesis surrounding a condition, then curly braces to open up a code block to be executed if that condition is true.

Let's think of a real world example of when we would use an if else statement.

When trying to access an ATM using your PIN there are two possible outcomes:

  - You enter the correct PIN, and are allowed access into your account or
  - You enter the incorrect PIN and are not allowed access to the account.

Let's break those steps down into **Pseudo Code**

```javascript
set the correct pin to 1234

if user enters pin of 1234

log in user to ATM and grant access to account

if user enters any other pin besides 1234

do not grant access to account
```

We first establish the correct pin number as 1234

Now lets turn that **Pseudo Code** into JavaScript!

```javascript
let correctPin = 1234

if (submittedPin === 1234) {

    console.log('correct pin')

} else {

    console.log('incorrect PIN')

}
```

There is still more to an `if, else` statement! There is also the possibility that you have two separate conditions you'd like to monitor.

In our example let's implement a feature that will also lock the user's account if they try an incorrect pin 3 times

We will accomplish this feat using a third condition, named `else if`

```javascript
let correctPin = 1234
let loginAttempts = 0
let submittedPin

if (submittedPin === 1234) {

    console.log('correct PIN')

} else if (submittedPin !== 1234 && loginAttempts < 3)  {
    // if pin number does not equal 1234 AND loginAttempts are less than 3

    loginAttempts++ // increase loginAttempts counter by 1

    console.log('incorrect PIN')

} else {

    console.log('incorrect PIN')

    console.log('Your account has been locked due to 3 incorrect login attempts.')

}
```

We added our `else if` statement as the 2nd statement of the conditional statement

The second condition is checking to see if the submitted PIN matches the correct PIN, also making sure there hasn't been 3 incorrect login attempts.

#### DOCS: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#Conditional_statements

---

# Exercise

1. Open a JavaScript repl.it



2. Copy and paste this code:
  ```javascript
  let sky = 'blue'

  if (sky === 'blue') {

    console.log(`the sky is ${sky}`)

  } else {

    console.log(`Interesting... I guess the sky is ${sky} today`)

  }
  ```
  - change the value of the `sky` variable to another color
  - notice how the else block is triggered when the sky variable no longer strictly equals blue
  - **Note**: inside these `console.logs` we are using [**template literals**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) to insert variables inside of strings. The same effect could've been created using: `console.log('the sky is ' + sky)`, but if you can get comfortable with template literals they will save you time in the long run. The important thing to understand about **template literals** is they are surrounded by "back-ticks" ``` `` ```, and to access variables inside of template literals we use `${}`:
    ```javascript
    let var1 = 'World!'
    console.log(`Hello ${var1}`)
    ```



3. **Challenge**: Create an `if else` statement that will `console.log('less than 2')` if a variable is less than 2, and otherwise will `console.log('greater than or equal to 2')`
  - **BONUS**: Modify the `if else` statement so that it has 3 conditions:
    - if the variable is **less than 2** `console.log` 'less than 2'
    - if the variable is **equal to 2** `console.log` 'the variable is 2'
    - if the variable is **greater than 2** `console.log` 'greater than 2'

  *hint: `<`*



4. **Challenge** Create an `if else` statement that will `console.log('odd number')` if a variable is odd, and otherwise will `console.log('even number')`

  *hint: `%`*
