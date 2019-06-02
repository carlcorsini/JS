# Javascript Project

---

You have made it through the Javascript section now it is time to put your knowledge to the test. In this project we will be adding some interaction to the page using javascript.

## Step One - Recap on HTML

---

After the footer we will be placing a form which will collect information about our user to purchase our product from our web page. Let's think about what we need to collect from the user.

- Name
- Email
- Credit Card Number
- Credit Card Expiration Month
- Credit Card Expiration Year
- Credit Card CVC number
- Purchase Button

The HTML structure will look similar to this:

```
-form [action="/pay" method="post" id="payment-form"]
--label [for="email"] {Email:}
--input [type="text" id="email" name="email" placeholder="Please enter your email"]
--label [for="card_number"] {Card Number:}
--input [type="text" maxlength="16" id="card_number" name="card_number" placeholder="Card Number"]
--label [for="card_month"] {Card Expiration Month:}
--input [type="text" maxlength="2" id="card_month" name="card_month" placeholder="Card Expiration Month"]
--label [for="card_year"] {Card Expiration Year:}
--input [type="text" maxlength="2" id="card_year" name="card_year" placeholder="Card Expiration Year"]
--label [for="cvc"] {CVC Number:}
--input [type="text" maxlength="4" id="cvc" name="cvc" placeholder="CVC Number"]
-- button [type="submit"] {Purchase}
```

### COMMIT YOUR CODE AFTER YOU ARE DONE

## STEP TWO - Creating and linking external Javascript file

---

We need to create a new file. Let's call that file app.js

Add this line of code into the app.js file

`alert('hello world');`

After we save our file we must insert the file using a special HTML tag called script

This is placed right above the closing body tag.

so place it above `</body>`

here is the syntax on how to use the script HTML tag.

`<script src="/app.js"></script>`

if everything is working great, then you should get an alert on your index.html page that says hello world!

### COMMIT YOUR CODE AFTER YOU GET THE HELLO WORLD TO POP UP

If you can't get hello world to show up on your web page then open a question on mentimeter so we can review it as a class.

## STEP THREE - Javascript Event

---

As you might have noticed when you push the purchase button we created it goes to an error page. That is because we havn't defined the pay page. We are going to use javascript to stop this form from submitting.

Where you have created your form in the `form` tag we are going to add another special attribute called on submit and then we are going to get it to call a javascript function every time the form is submitted.

For the time being lets continue with our alert. So instead of our alert showing up when we load the page we want the alert to only show up when the user submit the form.

There are a few thing we have to do to accomplish this:

- Create a function
- attach the function to the event listener (onsubmit)
- prevent the web page from going to another page
- Show 'hello world' on the page after someone clicks

Lets start by creating a function.

we will call this function purchaseProduct.

inside our app.js file we will remove the old alert and write the following code.

```
function purchaseProduct() {
    alert('hello world');
}
```

Well nothing is happening on the page just yet but you can see if it actually loaded by opening up your developer console in Google Chome and entering `purchaseProduct()`;

**_ to open developer tools just right click and hit inspect, then navigate to the console tab and enter the code above_**

Next we will create an HTML event listener with the special attribute of onsubmit.

Navigate your way to the form tag and add another attribute called onsubmit and tell the computer to run the purchaseProduct function.

This is what the opening form tag should look like when completed:

`<form action="/pay" method="post" id="payment-form" onsubmit="purchaseProduct()">`

Lets test it to see what happens...

It did show the alert but we still get that pesky error of the page isn't working :(

Our next step is to prevent the form from actually submitting the code.

In order to accomplish that we need to tell the browser to prevent the default action.

How we accomplish this is by passing the event to the javascript function.

it looks like this in the app.js file:

```javascript
function purchaseProduct(event) {
  alert("hello world");
}
```

and in the html it looks like this:

`<form *action*="/pay" *method*="post" *id*="payment-form" *onsubmit*="purchaseProduct(event)">`

I wonder what is in the event?

Well, we could `console.log` the event to see what is inside the object.

now your code in your app.js file should look like this:

```javascript
function purchaseProduct(event) {
  console.log(event);
  alert("hello world");
}
```

If you have your developer tools open and on the console tab you should be able to see the event, but the moment you push okay on the alert you are still redirected to the `/pay` page.

That isn't what we want… We are looking to prevent the default action so we can use Javascript to take care of the payment processing.

All we have to do is tell the event object to prevent its default action.

```javascript
function purchaseProduct(event) {
  event.preventDefault();
  console.log(event);
  alert("hello world");
}
```

And just like that the form has stopped taking us to a different page.

### Commit your code, once you finish this section

## STEP FOUR - Including dependencies

---

For the next part of our tutorial we need to include a couple of dependencies in order for us to start processing payments. As you are aware Stripe offers a wide range of tools and libraries that can make using Stripe easy in multiple projects. We are also going to be using another 3rd party dependency called Bootstrap, which was created by Twitter. Bootstrap will give us additional functionality and styles to make our web page look great while gaining a ton of extra features like modals.

We will be using a CDN that is provided by Stripe.

Place the following code above our other script tag in the `index.html` file.

`<script type="text/javascript" src="https://js.stripe.com/v2/"></script>`

Now to include our other dependencies which is Bootstrap we need to add the following scripts above our Stripe script tag.

```html
<script
  src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
  integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
  crossorigin="anonymous"
></script>
<script
  src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"
  integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1"
  crossorigin="anonymous"
></script>
<script
  src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"
  integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM"
  crossorigin="anonymous"
></script>
```

**_Now its time to test by opening up your browswer and developer tools to see if there are any errors_**

If any errors come up, let us know by creating a question in Mentimeter with the the error message you see.

### COMMIT YOUR CODE AT THIS POINT

## STEP FIVE - HTML UPDATES

---

Including external styles from Bootstrap to make your web page look better but before we begin we need to update our navigation with the proper attributes and include the specific classes to our HTML tags.

In our `index.html` lets go back to the `<nav>` tag and update it with the following structure.

#### Navigation updates

```html
-nav [class="navbar navbar-expand-lg navbar-light bg-light mb-4] --a
[class="navbar-brand" href="/"]{Stripe Foundations} --button
[class="navbar-toggler" type="button" data-toggle="collapse"
data-target="#navbarSupport" aria-controls="navbarSupport" aria-expanded="false"
aria-label="Toggle navigation"] ---span[class="navbar-toggler-icon"]
```

After the navigation is in place we need to fix one more thing before we load in the styles.

#### Carousel Updates

Locate your HTML `<div>` with the id of `carousel-wrapper`. We will need to add a few additional attributes.

We need to add a `class="carousel slide"` and `data-ride="carousel"` to the HTML tag with the `id="carousel-wrapper"`.

So once you've completed the update your tag should now look like this.

`<div id="carousel-wrapper" class="carousel slide" data-ride="carousel">`

#### Include Bootstrap styles

Navigate to the top of the HTML page and inside the `<head>` tag we need to include the following on the line after the `<title>`:

`<link *rel*="stylesheet" *href*="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">`

If everything is correct, then your web page should look similar to this:

<img src="https://i.ibb.co/SBNmXp0/screencapture-127-0-0-1-5500-index-html-2019-03-08-15-51-57.png" alt="screencapture-127-0-0-1-5500-index-html-2019-03-08-15-51-57" border="0">

As you have noticed the form we just created doesn't have any styling but we will tackle that next.

## Recap

---

What did we accomplish in this project.

- we added external javascript files

- added Bootstrap styling

- created a function

- attached the function to the submit event on our form
