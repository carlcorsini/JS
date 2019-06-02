# JavaScript Loops

------

### Loops are an important concept in JavaScript.

### Say we had a class roster in the form of an array, and we were writing a program that would append each students name onto a list on an HTML document.

### Loops would be a perfect tool to complete this challenge.

### In programming, groups of data are stored in arrays or objects, in order to traverse this information we must loop or iterate through it.

### Loops work differently in arrays and objects, we'll focus on arrays:

## [The For Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#for_statement)
```javascript
for ([initialExpression]; [condition]; [incrementExpression])
  statement
```



```javascript
let students = ['Lauren', 'Barry', 'Andre', 'Jose', 'Liz']

for (let i = 0; i < students.length; i++){

	console.log(students[i])

}
```

- In this example we are using a `for loop` to loop through the `students` array, and `console.log` each of the student's names



- To begin a `for loop` you simply start with the word `for (....)`, then a pair of opening and closed parenthesis



- *At first glance understanding what is happening in a for loop can be a difficult concept to grasp*



- Within the parenthesis we first set the value of the **initial expression** `let i = 0;`



- This will guarantee the loop begins at `0` or in this case specifically, the **first** index of the array.



- Next we set the **condition**:
	- If the expression (`i`) is less than the length of the array we are looping through `i < array.length;`, continue looping.



- The last step is to increment the **increment expression** `i++`, so that each time through the loop we increase the index until the iterator is eventually not less than the length of the array



- Once we set the constraints of the `for loop` we open up curly braces`{}` within which we are able to manipulate or traverse the array. It is important to note that each 'constraint' is separated by a **semi colon** `;`



- In this case we are simply console logging each of the students names



- This is the most basic set up of a `for loop` but you can change any of the constraints within the the parenthesis to better suit your needs.



Explore the many other types of iterators and loops below!

##### DOCS: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration

---

# Exercise

1. Open a JS repl.it



2. Fix the syntax errors in these `for loops` so they print each element of the array to the console:

	```javascript
	let fruits = ['apple', 'orange', 'kiwi', 'mango', 'banana']

	for (let i = 0, i < fruits.length, i++) {
		console.log(fruits[i])
	}
	```

  ```
	let trees = ['maple', 'redwood', 'sequoia', 'cypress', 'pine']

	for (i = 0; i > array.length; i-- {
		console.log(trees[i])
	}
	```



3. **Challenge** Now it's time to put a few things together:
  - Create a for loop that will search through the following array, and `console.log` a success message if the keyword `"JACKPOT!"` is found:
  - `let challengeArray = ['nope', 'no dice', 'yahtzee', 'JACKPOT!']`
  - Test your solution by removing `'JACKPOT!'` from the array and ensuring your success message is not triggered.
  - *hint*: `for loop` + `if else`



4. **BONUS** Create a for loop that finds the sum of all of the numbers in the following array, and `console.log` the sum.
  - `let numbers = [1, 2, 3, 4, 5]`
  - *hint*: `+=`
