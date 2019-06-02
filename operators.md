# JavaScript Operators

------

## What's an Operator?

### Answer: `+=-/*`

Different types of operators:

- [assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Assignment_operators)
- [arithmetic operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Arithmetic)
- [comma operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Comma_operator)
- [comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Comparison_operators)
- [logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Logical)
- [conditional (ternary) operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Conditional_%28ternary%29_operator)
- and more!

Luckily if you've ever heard of math, then you're probably familiar with these many of these operators!

---

# [Arithmetic Operators]((https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Arithmetic) `+-*/`

Plus, minus, multiply, divide are no different than your calculator, you'll find yourself using these operators frequently

You may use the `+` sign to add two strings together: `'hello' + ' world'` = `'hello world'`

### Modulo Operator `%`

The *modulo operator* is similar to division, but returns the **remainder**, so:

```javascript
console.log(5 % 2)
// returns 1 because 5/2 will have a remainder of 1

console.log(4 % 2)
// returns 0 because 4/2 divides perfectly to 2 with no remainder
```

The modulo operator is useful to determine if a number is even or odd because if **a number** `%` **2** returns **0** then that number must be even

**Assignment Operators** are used to set the value of a variable `let x = 3`

### Arithmetic Assignment `+= -= *= /=`

Addition assignment: `let x += 3`  breaks down to `let x = x + 3` Wow! JavaScript is cool.

This works the same way with all arithmetic operators


### Increment `++`

You can increment a variable using `++`

For instance each time through a `for loop`:

### for (let i = 0; i < array.length **`i++`**)

We will cover loops in much further detail later on

`i++` is used to increment the variable `i` by **1** each time through the loop

You can decrement with `i--` as well



We won't break down every single operator. We'll focus on comparison and logical operators, these are vital concepts to when using JavaScript.



---

# [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Comparison_operators)

These shouldn't be too unfamiliar to you either, but if so here is a refresher:

### `<`: less than

##### It almost looks like an L ;)

### `>`: greater than

### `<=` less than or equal to

### `>=` greater than or equal to

___

*There are some different types of comparisons available in JavaScript.*

*The purpose of comparison operators is to compare two values, the comparison itself we will refer to as an `expression`*

*The name for either side of the comparison are referred to as the `operands`*
___

### Equal `1 == 1 returns true`

returns true if both operands are equal

this expression will return true because 1 does in fact equal 1
___

### Strict Equal `1 === '1' returns false`

returns true if both operands are equal and of the same type

this expression will return false because although both operands are `1`, the left side is of type **number** and the right is of type **string**
___

### Does Not Equal `1 != 1 returns false`

returns true if both operands are not equal

this expression will return true because 1 does equal one
___

### Strict Does Equal `1 !== '1' returns true`

returns true if both operands are not equal and of different type

this expression will return true because although both operands are `1`, the left side is of type **number** and the right is of type **string**

Keep in mind there is a big difference between **comparison** `==` and **assignment** `=`

---

# [Logical Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Logical)

`&& || !`

Logical Operators are a way to combine conditional statements/expressions

### And `&&`

The `and` operator allows us to compare 2 expressions

Separating conditions with the `and` operator forces **both** conditions to be true in order for the expression to return true

```javascript
let a = true && true
let b = true && false

console.log(a === true)
// will return true because a is both true and true

console.log(b === true)
// will return false because b is true and false
```

You may separate as many conditions as you'd like with the && operator, but it's usually poor practice to use more than a few
___

### Or (Pipes) `||`

Separating conditions with the `or` operator forces **at least one** condition to be true in order for the expression to return true

You may have multiple conditions separated by or, but as long as one is true, your expression will return true:

```javascript
let a = false || false || null || 0 || true

console.log(a === true)
// a will return true because at least of of the conditions defining a is true
```
___

### ! (Bang) `!`

Bang is a sort of short hand for checking to see if some value is falsey.

you place the `!` at the beginning of the variable you'd like to check for instance:

```javascript
let a = true

console.log(!a)
//this statement will return false because a is not false
```

Explore the many other operators offered by JavaScript!

DOCS: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Operators

---

# Exercise

1. Open up a JS repl.it



2. Let's play around with some **Arithmetic Operators**:
  ```javascript
  console.log(5 + 10, '<<1')
  console.log('string' + ' & ' + 'another string', '<<2')
  console.log(10/5, '<<3')
  console.log(12*2, '<<4')

  let a = 2
  a+=2
  console.log(a, '<<5')
  ```
  - Try multiplying a *string* by a *string*, and what happens?
  - JavaScript does not allow **all** arithmetic operators on strings, other languages do.
  - Play around with some of the other arithmetic operators and move on to the next step



2. **Comparison Operators**:
  ```javascript
  let x = 1
  let y = 2
  let x1 = '1'

  console.log(x == x1, '<<6')
  // returns true because the number 1 loosely equals the string of 1

  console.log(x === x1, '<<7')
  // returns false because the operands are the same number of x different type

  console.log(x < y, '<<8')
  console.log(y >= 2, '<<9')

  console.log(x != 1, '<<9')
  // returns false because both operands are the same number

  console.log(x !== x1, '<<10')
  // returns true because both operands are the same number but of a different type
  ```

  *You may be wondering about the two expressions separated by a comma within each `console.log`: **`'<<1'`**. This is a useful trick to keep track of your `console.logs`, especially when learning.*



3. **Logical Operators**:
  ```javascript
  let c = true
  let d = false

  console.log(c && d === true)
  //returns false because both operands must be true

  console.log(c || d === true)
  // returns true because at least one operand is true

  console.log((true && false) || (false && false) || (true || false))
  // returns true because at least one of the expressions separated by the pipes and wrapped in parenthesis was true, which one is it?

  ```



4. **Challenge**: Assign the following variables to **true** or **false** values, you may only assign one variable to be true, the other 2 must be false:
  ```javascript
  let var1
  let var2
  let var3

  console.log((var1 || var2) || (var2 && var3 ) || (var3 || var1) === true)
  ```

5. **Challenge**: Use the **modulo** operator so this statement evaluates to true:
  ```javascript
  let var1
  let var2

  console.log(var1 % var2 === 0)
  ```
