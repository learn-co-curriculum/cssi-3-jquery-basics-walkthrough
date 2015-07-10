---
tags: cssi, javascript, jquery
level: 2
languages: javascript
---
#jQuery Basics

Okay, so we know how to include the jQuery library, and we’ve seen that it can help us change the text on elements we select. jQuery is a whole lot more than that, though! It makes tons of things we’d want to do a breeze, like:
+ finding particular elements on the page
+ adding and removing elements
+ changing content on the fly
+ triggering an action when a user clicks a particular element
+ triggering an action when a user types on the keyboard
+ hiding and showing elements
+ changing the style of elements on the fly
+ getting data from a server
+ sending data to a server

If you are looking for something in particular, check out the [jQuery Cheatsheet](http://oscarotero.com/jquery/) and look for what you want to do. We'll go over the main things you can do now, but don't worry about memorizing - you'll always be able to look up the syntax when you need to.

## JQuery - Selection and the DOM
In order to do anything with jQuery, we first need to be able to navigate the DOM. In previous example, we saw that we could select elements with the $() method. When we want to select, we pass a CSS selector string into the $() method - every element that you would get with the selector in CSS, you get with $().

Check out **traversal** in the jQuery docs for the complete list of methods.

Some examples:


|CSS          |jQuery           |Selected        |
|---          |---              |---             |
|p            |$('p')           |All the paragraph elements|
|div          |$('div')         |All the div elements|
|.button      |$('.button')     |All elements with class=”button”|
|#headline    |$('#headline')   |The element with id=”headline”|
|.code strong |$('.code strong')|all of the strong elements with parent elements with the class="code"|
|header nav li.home|$('header nav.home')|All the li elements inside navs inside headers with the class home'|

You can make them pretty specific!

##DOM Traversal
Sometimes, you have an element selected already, and you want to select an element or multiple elements that are related to it - maybe its parent or children, or all of its descendants, or the next child of its parent element (a sibling!).

JQuery gives us the power to move up and down the 'tree' of the DOM. There are a ton of methods for moving around, and you can browse through them on the cheatsheet under 'Tree Traversal'.

##Filtering
Sometimes, after you select lots of elements, you want to do something to a selection of them. jQuery has some great methods for choosing the particular elements you want from a set of them. Check them out under 'Filtering'.

##More Selection
There’s lots of ways to select elements, and pretty much any kind of element selection problem is easy with jQuery - if you can find the right method! If you have the time, check out the other methods on the cheatsheet. See if you can figure out what they do, and when you might need them.

##Adding and removing elements
Now that we know how to select elements and get around the DOM, let’s check out some of the cool things we can do!

Say you want a user to be able to add and remove items on a list - you don’t want to send a whole new HTML document from the server every time they do! Instead, you can use jQuery to add an element dynamically.

```
$('#my_list').append("<li>New element</li>")
```
And to remove an element:
```
$('#elementToRemove').remove()
```
The cheatsheet has lots more ways to add and remove elements. How would you add an element around a group of elements? How about removing an element without removing the elements inside it?

## JQuery and CSS
JQuery doesn’t just work to modify HTML - it also works to change the style of a page! Any kind of css that you might want to add, you can add!

Here are some methods you can use to edit your CSS with JQuery:
+ addClass() - Adds one or more classes to the selected elements
+ removeClass() - Removes one or more classes from the selected elements
+ toggleClass() - Toggles between adding/removing classes from the selected elements
+ css() - Sets or returns the style attribute
