# JavaScript Events

------

## Time for the fun part!

### We use JavaScript to manipulate and interact with a web page

### In other words JavaScript can manipulate the Document Object Model or [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document)

### There are no libraries needed, this can all be done with "vanilla" JavaScript

### [jQuery](https://jquery.com/) was created to ease this process but has mostly been phased out due to JavaScript adopting some jQuery features, and due to other front-end frame works like [React](https://reactjs.org/) that have eased the whole process of creating a dynamic web page.

### Important concepts to understand in terms of the DOM are _selectors_ and _events_

---

## Selectors

- [querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)

- [getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)

Selectors allow JavaScript to *select* HTML elements depending on that HTML element's attributes.

We access *methods* off of the **Document Object Model/DOM** to select HTML elements.

For instance lets say we had an HTML **button** we would like to select in order to add functionality via JavaScript:

`<button id="ourButton">`

we can *select* this button and store it in a variable to reference later like so:

```
let ourButton = document.getElementById('ourButton')

or

let ourButton = document.querySelector('#ourButton')
```

Both lines of code are selecting the button element with an id named `ourButton` and defining it with a variable name `ourButton`

There are other ways to select elements other than by ID, explore the other ways to select an element such as by tag name or class name

we can also select groups of elements with the same attributes, this would return an array of different HTML elements you may now manipulate

---

## [Events](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Events) & [Event Listeners](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

Every time a user interacts with the page it sets off an **event**

there are many types of events:

- click
- mouse over
- mouse off
- scroll

These are all events we fire off every day without knowing, these events can be *listened* for using Javascript

We'll take the button from the last code snippet and add an `onClick` event listener that will console log the "event target" and a message whenever clicked.

```javascript
ourButton.addEventListener('click',function(event){

	console.log(event.target)

	console.log('I was clicked!')                        

})
```

Here we are accessing the button we selected earlier and adding an **event listener**

Every time that button is clicked it will fire off the event within the code block, in this case a console log of the **event target** and a message

instead of a **click** event you could replace **mouseover** which would in turn set off the event when ever the button was hovered over with the mouse.

Explore the many types of events available in the DOM!

---

# Exercise

### No more repl!

We are moving back to our text editor to add some JavaScript to our webpage

This will involve creating a new project folder and linking a `.js` file with an **HTML** file

Let's get started!

## Part One: JavaScript and HTML Combine Forces

1. Create a new repository, name it something along the lines of "javascript events playground", up to you



2. Clone that repository to your projects folder



3. Open up your repository in VSCode



4. Create two files, `index.html` and `index.js`



5. Create a **script** tag and link your `index.html` to your `index.js`:

	`<script src="index.js" type="text/javascript" charset="utf-8"></script>`



6. Now in your `index.js` file `console.log` a message and save the file



7. Use live server to open your `index.html` file in your browser or use command: `$ open index.html`



9. Open up the **JavaScript Console**. In *Chrome* shortcut is `command + option + j`
	- you can access the *Developer Console* in Chrome by right clicking and selecting inspect
	- also by using the top menu bar: `View > Developer > JavaScript Console`


10. Do you see your message? Refresh the page to make sure your message appears!
	- So what? We may have only made a `console.log` in the browser, but next we will use the connected files to access the **Document Object Model**
	- If so give yourself a pat on the back, and move on to Part Two!


## Part Two: The Return of the _Document Object Model_

Now we will have to work between the `index.html` and `index.js` file.

The goal is to create a button that will change the color of a square `div`

1. In your `index.html` create a **button** tag and a **div** tag
	- set the button `type` attribute to `button`
	- use **CSS** or `style` tags to give the **div** a *height* and *width* of `250px` and a *border*
	- give the **button** an `id` of `changeColor`
	- give the **div** an `id` of `colorDiv`
	- you may also give your page a Header/Title
	- you should have something that looks like this:

	<img src="https://i.imgur.com/fH0iSuP.png" title="source: imgur.com" width="500" />

2. In your `index.js` file we will start accessing the **DOM**
	- copy and paste this code into the `index.js`:
	```javascript
	document.addEventListener('DOMContentLoaded', function(){

	})
	```
	- in those lines of code we are essentially telling the document: "wait until you're done loading, then run this code"
	- we add an *event listener* using the `addEventListener` method of the **DOM**: `document.addEventListener()`
	- we specify the `'DOMContentLoaded'` event by adding a string of `'DOMContentLoaded'` as the first argument of that method
	- we use an **anonymous function** as the second argument of the **addEventListener** method
	- move your `console.log` to within that function block



3. Let's map out what we will do next using *Psuedo Code*

	```javascript
	select the "change color button" and store it in a variable named changeColorButton

	select the "change color div" and store it in a variable named colorDiv

	add a 'click' event listener to the changeColorButton

	within the 'click' event function block:

	change the background color of the div to green
	```

	Now in JavaScript:

	```javascript
	document.addEventListener('DOMContentLoaded', function(){

	  let changeColorButton = document.querySelector('#changeColor')

	  let colorDiv = document.querySelector('#colorDiv')

	  changeColorButton.addEventListener('click', function(){

	      colorDiv.style.background = 'green'

	  })

	})
	```

	- Did the `div` change color? Woo hoo! But wait! There's more...
	- Since we stored the `colorDiv` in a variable, we are able to access the attributes of that `div` using JavaScript.
	- In this case we accessed the **style** attribute and then the **background** and set it equal to green!
	- You can do much more than change colors of HTML elements of course, you can create HTML elements with JavaScript, you can add a class to an HTML element or change it's `innerHTML`
	- Check out the [Core Interfaces of the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#Core_Interfaces_in_the_DOM) from MDN



4. **Challenge**: add an `if else` statement that will toggle color between *green* and *white*



5. **BONUS**: add a `mouseover` *event listener* on the changeColor div that will change the background to another color besides green, go crazy!



6. **BONUS** instead of using an **anonymous function** try adding your logic to a **named function**, and pass that function as the second argument of the `DOMContentLoaded` *event listener*


7. But wait... there is another way
	- add this code to the `index.js` file, this time we'll change the color to red
	- we create a named function called `changeColor` and will assign it to the `onclick` attribute of **another** button
	```javascript
	function changeColor(){

		let colorDiv = document.querySelector('#colorDiv')

		colorDiv.style.background = 'red'

	}
	```

8. Now add another `button` element to your `index.html` and give it an `onclick` attribute and set the value of that attribute to `changeColor()`
	- by giving the `onclick` attribute a value of `changeColor()` we are letting that button know, when clicked, run the `changeColor()` function
	- 2 different ways to make this happen, knowledge is power!

## Great Work! You've passed JavaScript 101
