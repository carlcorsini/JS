# Javascript Data Types

------

### Data Types are a great place to start picking apart the JavaScript language.

### Each data type has its own defining properties and methods.

### Methods allow you to manipulate and navigate each data type in particular ways specific to each one.

### There are 6 different data types in Javascript. (There is technically a 7th named [symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol), but we will not be using that data type)


1. [Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) `let the skyIsBlue = true or let theSkyIsFalling = false`
  - Booleans are either `true` or `false`
  - Do not wrap a `true` or `false` with quotes `''`
  - Comparisons and some pieces of data will evaluate to true/false, or have a *truthy* or *falsey* value
  - **Falsey** values:
    - strings of length 0 `''`
    - the number `0`
    - null
    - undefined
    - NaN
  - **Truthy** values:
    - strings of greater length than 0 `' '`
    - all numbers besides `0`
    - empty arrays and objects
    - non empty arrays and objects



2. [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) `let aVariableName = "string"`
   - Strings are defined by wrapping characters in single `''` or double quotes  `""`, or with back-ticks ``` `` ```
   - Note there is a key difference between `let one = "1" and let one = 1`
   - Strings have their own set of methods, for example `string.split('')` will return an array of each character of the string.
   - Explore the different methods available for strings



3. [Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)  `let theLoneliestNumber = 1`
   - Numbers are numbers!
   - We can use mathematical operators on numbers like `console.log(1+1)`
   - In JavaScript numbers include floating point numbers (floats) or numbers with decimals.



4. [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
   - Arrays, Objects, and even null are of the object data-type
   - you can check a data type using `typeof`: `console.log(typeof '{hello: 'world'}')`
   - Objects include both objects and arrays, so we'll break the two down further



- [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array): `let fruits = ['apples', 'oranges', 'bananas', 'mangos']`
  - **arrays** are groups of data surrounded by brackets `[]`
  - each piece of data is separated by a comma
  - the data inside an array does not have to be the same data type, you could have an array like: `[1,'string', ['1', 2, 'three]]`
  - that's right you can put arrays inside of arrays, you can even put objects inside arrays, and vice versa!
  - each element of an array has an **index**
  - indexes start at `0`, so index `0` of this array `[1,2,3]` would be the number `1`
  - arrays are very useful and important for organizing data.
  - In Javascript you will often `loop` through arrays in order to perform an operation on each **index** of an array, we will cover loops in a later section.
  - useful array **methods** include *map*, *forEach*, *filter*, *sort*, *find* and many more!
   ```javascript
   [1,2,3].find(each=>{

   	return each === 1

   })
   ```
  - The **find** array method will return the first `1` found in the array, *don't worry* this is a complex 3 lines of code



- [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object): `let anObject = {key: 'value}'`
  - Objects are usually the most difficult data type to grasp when first learning about programming.
  - Objects are made up of `key: "value"` pairs
  - Objects allow developers to further organize large pieces of data.
  - An example of an object would be for a user:
  ```javascript
  let user = {
              firstName: 'Steph',
              lastName: 'Curry',
              email: 'sc3@warriors.org',
              password: 'goWarriors',
              jerseyNumber: 30,
              favoriteFoods: ['popcorn', 'The Rockets', 'Curry']
            }
  ```
  - Notice how each key value pair is separated by a comma, and that each value may be of a different data type.
  - Objects *do not* have **indices** the same way that arrays have, so you cannot loop in the same way as arrays, although there are other ways to loop through objects.
  - The important different between *arrays* and *objects* is that arrays are **enumerated** and objects **are not**, in objects the order of elements differs depending on which [environment you are working in](https://stackoverflow.com/questions/6316618/do-javascript-arrays-and-objects-have-a-set-order)
  - Objects have their own set of methods, for example [Object.keys](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys) will return an **array** of the given objects "keys":
  ```javascript
  let userKeys = Object.keys(user)
  console.log(userKeys)
  ```
  - Explore the available methods for objects



5. [Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) `undefined`
   - Undefined is what it sounds like, undefined, but there is definitely more intricacies than that
   - You can set variables to `undefined` if you'd like to use it later on but don't want to declare the value right away
   - `undefined` is different than an empty array `[]`
   - Want proof? `console.log([] === undefined)` What this expression is essentially asking is does an empty array equal undefined? We'll go further in depth later about what `===` means



6. [Null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null)
  - Null is a little different than undefined
  - Null is it's own distinct value which represents nothing, it indicates that a variable points to no object



DOCS: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures

---

# Exercise

Let's play around with some data-types!

The important the important thing to learn in this lesson is how to access information depending on the data-type

1. Open up a JavaScript repl.it



2. copy and paste this code into your repl.it:
  ```javascript
  let aNumber = 1
  let anotherNumber = 2
  let aString = "Hello World"
  let anotherString = "!"
  let anArray = [1,2,3,4,5]
  let anObject = {a: 1, b: 2, b: 3}
  ```



3. Try console logging each of these variable names and make sure the data is displayed in your console `console.log(aNumber)`



4. Try adding the first 2 variables `aNumber` and `anotherNumber` within a console log using the `+` sign. What happens?
  - Do the same with the 2 string variables
  - You can use *operators* on variables like the `+` sign! We'll go further into detail about *operators* later on.



5. Now let's access some data out of *Arrays* and *Objects*, paste this code into your repl.it:
  ```javascript
  console.log(anArray[0])
  ```
  - To access a single element out of an *Array* we use **Bracket Notation** `[]`
  - Don't forget about the indexing rule: the first index of an *Array* is the **"0th"** index, not the **1st**



6. Copy and paste this code in your console
  ```javascript
  console.log(anObject.a)
  ```  
  - To access a single element out of an *Object* we use **Dot Notation**
  - We can also use **Bracket Notation** for objects: `console.log(anObject['a'])`
  - We will almost always use dot notation to access information out of objects, but there are situations where bracket notation is needed



7. Let's say we have an *Array* within an *Array* or an *Object* within an *Array* and so on. You can access nested information by "stacking" **Dot Notation/Bracket Notation**. Copy and paste this code:
  ```javascript
  let nestedArray = [[1,2,3],["red", "blue", "yellow"]]

  console.log(nestedArray[1][2])
  ```
  - to access the nested data we select the first index of the `nestedArray` then the second index of the array we previously selected.



8. Copy and paste this code:
  ```javascript
  let nestedObject = {
    cars: ['Toyota', 'Honda', 'Subaru'],
    cities: ['San Francisco', 'Oakland', 'Berkeley'],
  }

  console.log(nestedObject.cars[2])
  ```



9. Copy and paste this code and `console.log` "Hello World!" using Bracket and Dot Notation
  ```javascript
  let challenge = {
    key: 'value',
    almost: 'there',
    here: [
      {
        thisIs: 'getting',
        a: 'little',
        tricky: ['Hello Earth', 'Hello Detroit', 'Hello World!'],
      },
      {
        too: 'far',
      }
    ]
  }
  ```



10. Now let's play with some data-type specific **methods**:
  - Copy and paste this code:
  ```javascript
  let stringToSplit = 'Hello'
  console.log(stringToSplit.split(''))
  ```
  - the **split** method will split a string into an array, you can specify where you would like the split to happen by placing a string inside the parenthesis:
  ```javascript
  let splitOnTheComma = "Hello, It is nice to meet you, I love JavaScript, it is lit"
  console.log(splitOnTheComma.split(','))
  ```
  - Strings have a large collection of methods, here are a few more to play around with:
  ```javascript
  let upCaseMe = "hello"
  console.log(upCaseMe.toUpperCase())
  ```
  ```javascript
  let sliceMe = "Hello World!!"
  console.log(sliceMe.slice(12))
  ```



11. Now some Array Methods:
  ```javascript
  let pushMe = ['Hello']
  pushMe.push('World!')
  console.log(pushMe)
  ```
  - the **push** array method allows you to add an element to the end of an array

  ```javascript
  let joinMe = ['j','o','i','n','M','e']
  console.log(joinMe.join(''))
  ```
  - the **join** method allows you to join elements of an array together
  - you can specify what you would like to join with similarly to the string split method by placing a character within the parenthesis for instance: `console.log(joinMe.join('-'))`
  ```javascript
  let reverseMe = ['e', 'M', 'e', 's', 'r', 'e', 'v', 'e', 'r']
  console.log(reverseMe.reverse())
  ```
  - the **reverse** method does what it sounds like, it reverses the order of an array
  - you can also chain methods together to do multiple manipulations in one line
  ```javascript
  let wouldYouLookAtThat = ['e', 'M', 'e', 's', 'r', 'e', 'v', 'e', 'r']
  console.log(wouldYouLookAtThat.reverse().join(''))
  ```



12. Now for a **challenge**:
  - take this string `'!dlrow olleh'` and use Array and String methods to output `"HELLO WORLD!"`



Great Work! There are tons of methods for all data-types. There are also sets of methods referred to as "higher-order functions" which allow you to do more complex tasks like search through arrays and perform multiple tasks in one simple step like:
```javascript
[1,2,3].find(each=>{

 return each === 1

})
```
We will focus on the basic methods for now, but we will eventually (hopefully) play around with some higher-order functions as well. Explore some other methods, share with your neighbor and move on!
