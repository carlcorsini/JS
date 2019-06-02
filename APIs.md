# Working With External APIs in Javascript

## **A**pplication **P**rogramming **I**nterface

**API** is a term that can be used for anything that falls under the definition of **Application Programming Interface**

We will use an external API to reuest data from a server

[What is an API?](https://medium.freecodecamp.org/what-is-an-api-in-english-please-b880a3214a82)

External APIs will serve as an interface in the form of different **URL's** that will *respond* with the data requested in the form of **JSON**

We will find a few API *endpoints*, make a *request* to an endpoint using JavaScript, then convert that **JSON** data so that JavaScript may consume and display that data using HTML

We won't be writing our APIs in this course, but we will access some available APIs so that we can have some data to work with

In your browser go to this link: [`http://beer-me-python-backend.herokuapp.com/beers`](http://beer-me-python-backend.herokuapp.com/beers)

Notice how that **endpoint** returns this data in a form you may have seen before. This data format is JSON. We'll use JavaScript to convert that JSON for JavaScript to consume. 

*use the [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en) Chrome extension to help make the data a little easier to read*

This data is an *array* of *objects*

### Before JSON Formatter
<img src="https://i.imgur.com/GAZ15Xk.png" title="source: imgur.com" width="750"/>

### After JSON Formatter
<img src="https://i.imgur.com/ImLVjHm.png" title="source: imgur.com" width="750" />

We will loop through this **array** and append all of this data to HTML


# Exercise

1. Create a new repository titled something along the lines of "API-Playground"



2. Clone this repository into your *projects* folder and `cd` into that directory



3. Create an `index.html` and `index.js` file



4. Connect the two files and confirm they are linked by writing a `console.log` and opening up your JS dev tools.



5. Copy this HTML into the `head` of your `index.html`:

    ```html
    <link rel="stylesheet" type="text/css" href="semantic/dist/semantic.min.css">
    <script
    src="https://code.jquery.com/jquery-3.1.1.min.js"
    integrity="sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8="
    crossorigin="anonymous"></script>
    <script src="semantic/dist/semantic.min.js"></script>
    ```
    - We will be using a CSS framework called [Semantic-UI](https://semantic-ui.com/introduction/getting-started.html)
    - This framework will help style our webpage



6. In the `index.html` file we will use the [Card](https://semantic-ui.com/views/card.html) component to display information received from an external api.

<img src="https://i.imgur.com/VSctiN7.png" title="source: imgur.com" width="300" />


7. This is the HTML code for the card component:

    ```html
    <div class="ui card">
        <div class="image">
            <img src="/images/avatar2/large/kristy.png">
        </div>
        <div class="content">
            <a class="header">Kristy</a>
            <div class="meta">
                <span class="date">Joined in 2013</span>
            </div>
            <div class="description">
                Kristy is an art director living in New York.
            </div>
        </div>
        <div class="extra content">
            <a>
                <i class="user icon"></i>
                22 Friends
            </a>
        </div>
    </div>
    ```


8. Insert the above HTML into your `index.html`
    - Comment out the `script` and `link` tags we inserted in step 5
    - notice

