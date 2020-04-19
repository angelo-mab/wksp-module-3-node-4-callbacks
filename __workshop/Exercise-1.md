# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything.

Take the time to explain it to each other.

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
// Answer here
<!--
1. create a server.js file
2. import all necessary packages to run the server (express, bodyParser, morgan)
3. set a port for which the server can run on
4. get homepage and set it on '/', handle the hompage from './handlers'
5. when submitting a form, front end will send a post to the backend by running the handleFormData
 -->
```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
// Answer here
<!--  according to https://www.npmjs.com/package/body-parser
Node.js body parsing middleware.

Parse incoming request bodies in a middleware before your handlers, available under the req.body property.

it is related to line 18 in server.js
 -->
```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
// Answer here
<!--
.get & .post are HTTP methods

the GET method is used to REQUEST data from a specidied resource, in this case, from handleHomePage

the POST method is used to SEND date to a server to CREATE/UPDATE a resource -->
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
// Answer here
<!--
this line imports handlHomepage, handleFormData, handle404 from ./handlers.js file

it is to clean up to server file and make it more readable
 -->
```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
// Answer here
<!--

items is an empty array that is used to store objects push from handleFormData, line 9
 -->

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
// Answer here
<!--
it is there to reload the page and display the objects stored in items, if not reloaded, nothing will be displayed in the todo list
 -->

```

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
// Answer here
<!--
the page only accepts html pages and not json, or plain-text pages
 -->
```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
// Answer here
<!--
in homepage.ejs
line 1: imports header from patials
line 2: opens a div with class='input-container'
line 3: imports todoInput from partials
 todoInput is a form

line 7 - 9: prints each item from the imported items prop from handlers.js line 8
 -->
```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
// Answer here
<!--
global variable. we can refere to these variable when needing to style and then change these variable only and it changes the style for the whole file that refers to the styles.scss
 -->

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
// Answer here
<!--
in styles.scss line 10, we can see that the file imports the _homepage.scss.
this makes _homepage.scss able to see the global variable set in its parent file (styles.scss)
 -->
```
