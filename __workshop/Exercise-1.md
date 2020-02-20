# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything.

Take the time to explain it to each other.

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here

/*
1. create server.js file, index.html file, css / scss files

2. in the index.html file:
 !doctype

 <head>
   </head>
 <header>TODO List</header>
   <body>
<div>
   <form>
     <input>
     <button>
   </form>
 </div>

<div>
 <ul>
  //js fil that list all input after being submitted with the button
  </ul>
</div>
   </body>


3. create list function in server.js
4. style with css / scss
*/

```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here

/*
it is a middleman
it takes the the HTTP request body

"Using body parser allows you to access req.body from within your routes, and use that data for example to create a user in a database." - Hugo Di Francesco
https://www.quora.com/What-exactly-does-body-parser-do-with-express-js-and-why-do-I-need-it

AFAIK


line 18 : .use(bodyParser.json())

*/

```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here
/*
23 - Jordan
24 - Bryant

.get - requests the data inputed
.post - takes  data and sends to server
*/
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here
/*
new:              its assigning multible variables from ./handlers(.js)
what it do:       it assigns each variable that has the same variable name in the './handlers.js file.

ex: const handleHomePage = requires('./handlers).handleHomepage;
  -------
  const handleHomePage = (req, res) => {
    res.render('pages/homepage', { items: items })
}


*/
```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here
/*

items is an array

1. in handleFormData, it takes the item/value from the form and pushes it into the items array

then

2. in handleHomePage, we are assign the key called items in the homepage and assigning the 'items'/value to it


*/


```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here
// so that we can refresh the page with the items that we have pushed

```

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here
/*
1. - if you nav into the server using the browswer, you will get a 404,
   - it will declare it status as 404,
   - render the pages/fourOhFour page and return the path given

ex. localhost:8000/hello
it will return pages/fourOhFour and displays the path in the body /hello

*/

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here

/*
todoInput.ejs is an extract of an html

 line 1: open form tag, assign method as 'POST', assign action as '/form-data'

 line 2: open label tag, assign for as 'item', innerText as 'TODO Item' close label tag

 line 3: open input tag, type - text, name - item, placeholder - 'Item Description' (what is written in the input before user inputs anything), close input tag

 line 4: open button tag, type - submit, innerText - 'Submit', close button tag

 line 5 - close form tag


homepage.ejs is an extract of an html
 line 1: imports html extract from partials/header
 line 2: create first div tag
 line 3: imports html extract from partials/todoInput
 line 4: close  first div tag
 line 5: open second div tag,set class as content
 line 6: open unordered list tag with class 'todo-list'
 line 7: open tag to accept a js .forEach method
 line 8: adds a newly created list item tag with class name 'todo-list--item and sets the innerText as the item. close
 line 9: close .forEach method
 line 10: close unordered list tag
 line 11: close div tag
 line 12: imports html extract from partials/footer

*/

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here
/*
these are variables with values stored in them
useful when youre defining the same background color everywhere and then one day want to change the color, you can just change it in the variable declaration

*/

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here
/*

it calculates the value stored in the content-width declared in the styles.scss and substacts 60px to it and sets the result to width

width : 340px;

*/
```
