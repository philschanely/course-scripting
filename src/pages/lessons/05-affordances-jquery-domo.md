---
type: lessons
title:  "Affordances and Introduction to jQuery and DOM"
number: 5
cover: "https://source.unsplash.com/W_K6j6OQBDg"
---
import Subpage from "../../components/subpage.js"

<Subpage slug="affordances">

### Affordances

Visual design for interactive sites and applications moves quickly beyond the elements of the layout that the user sees, reads, and otherwise processes. Interactive design involves action and change. In order to give users a sense of what can or should be possible in the design we need to think about affordances and signifiers.

***Read IxD1, Chapter 5: Affordances***

#### Study Questions

1. What are affordances and signifiers? How are they similar and how are they distinct?
2. Describe each of the 5 different kinds of signifiers.

</Subpage>
<Subpage slug="digging-deep-with-dom">

### Digging Deep with the DOM

Last of all this week we look deeper at the DOM and some options we have for working with the DOM in JavaScript.

***Read Duckett, Chapter 5, pp.183--189*** for a formal overview of the DOM that expands on the other summaries you have read to date.

Pages 188--189 introduce some JavaScript DOM methods and properties that allow us to do stuff with the DOM tree. However, these are a little complicated to access using basic JavaScript. jQuery has a lot of shortcuts for these DOM features and expands on them with other helpful tools.

</Subpage>
<Subpage slug="intro-to-jquery">

### Formal Introduction to jQuery

So let's make another big shift and look formally at how jQuery can be used.

***Read Duckett, Chapter 7, pp.293-305*** for a formal introduction to jQuery.

Note that pp.302--303 expound on how to use selectors in jQuery. These are overall very similar to the selectors you use with CSS!

You also might want to bookmark pp.304--305 as these show a comprehensive list of jQuery methods you can use for all kinds of operations. The rest of this chapter explains these in more detail and we'll look at them closer over the next few lessons.

</Subpage>
<Subpage slug="dre-explained">

### The DRE Explained

We've already been working with this little structure in our exercises:

```js
$(document).ready(function() {
    // Do stuff...
});
```

***Read Duckett, Chapter 7, pp.312, 313*** for a formal explanation of this feature.

</Subpage>
<Subpage slug="jquery-and-dom-overview">

### Overview of jQuery Functionality with DOM

Now more about some aspects of jQuery.

***Read Duckett, Chapter 7, pp.306, 307, 310, 311*** for more information about how we can:

* Select individual DOM elements with jQuery (306).
* Select groups of DOM elements with jQuery (306).
* Retrieve content of a DOM element (307).
* Change content of a DOM element (307).
* Easily apply changes to groups of elements (310).
* Chain jQuery commands in sequence (311).

All these give us background for things we can do with jQuery selections.

Now let's look closer at a series of key features of jQuery selections.

***Read Duckett, Chapter 7, pp.314-321*** for more details about some jQuery methods we can use to work with elements in the DOM. Three categories of operations are covered here and explained more below.

#### 1. Retrieving and Changing Elements and Attributes

First of all, we have three methods that allow us to both *retrieve* and to *change* elements in various ways:

* We *retrieve* plain text content of an element with `.text()` and *change* the content of the element by calling the same method but passing new content into it (pp.314--317):

    ```js
    // Retrieve plain text content
    var boxText = $("div.box").text();

    // Change plain text content
    $("div.box").text("Let's each cake.");
    ```

* We *retrieve* HTML content of an element with `.html()` and *change* the content of the element by calling the same method but passing new content into it (pp.314--317):

    ```js
    // Retrieve HTML content
    var boxContent = $("div.box").html();

    // Change HTML content
    $("div.box").html("<p>Let's each cake.</p>");
    ```

* We *retrieve* the value of an attribute of an element with `.attr()` and *change* the content of an attribute by passing a second value into the same method (pp.320).

#### 2. Working Specifically with `class` Attributes

Building on this, we often work with `class` attributes in specific, so we can use the following for common operations:

* `.addClass()` -- add a new class onto an element. Pass just the class name in quotations *without the typical period before it*.
* `.removeClass()` -- remove a class from an element. Again pass just the class name in quotations *without the typical period before it*.
* `.toggleClass()` -- (BONUS) toggle a class on or off from an element. As before, pass just the class name in quotations *without the typical period before it* and it will either be added if its absent or be removed if its present.

#### 3. Replacing and Removing Elements and Attributes

Finally, we can replace or remove elements and their attributes:

* We replace an element with new content with `.replaceWith()` (316--317):

    ```js
    // Replace a div.box with a p
    $("div.box").replaceWith("<p>Let's eat cake</p>");
    ```    

* We remove an element altogether with `.remove()` (p.316--317)
* We remove an attribute from an element with `.removeAttr()` (p.316--317)
* We insert content in relationship to existing content as follows (318--319):
    * `.before()` -- before and outside the selected element (such as inserting a new paragraph above a `ul`)
    * `.prepend()` -- inside the element before any of its inner contents (such as adding a new item at the beginning of a `ul`)
    * `.append()` -- inside the element after any of its inner contents (such as adding a new item to the end of a `ul`)
    * `.after()` -- after and outside the selected element (such as inserting a new paragraph after a `ul`)

#### Study Questions

1. What is the DOM tree?
2. What are the 4 types of nodes that make up the DOM tree and what do they represent?
3. Briefly describe 3 main features of jQuery.
4. What are some of the differences between jQuery's basic DOM features and the default JavaScript DOM?
5. **SKILL:** Read, write, and otherwise modify HTML and text content using jQuery's `.html()`, `.text()`, `.replaceWith()`, and `.remove()` methods.
6. **SKILL:** Insert new content into an HTML document using jQuery's `.before()`, `.after()`, `.prepend()`, and `.append()` methods.
7. **SKILL:** Retrieve, change, and remove attributes using jQuery's `.attr()` and `removeAttr()` methods.
8. **SKILL:** Add and remove classes on HTML elements using `.addClass()`, `.removeClass()`, and `.toggleClass()`.   

</Subpage>
<Subpage slug="presentation-and-demo">

### Presentation and Demo

Watch this presentation and play along in the demo provided in Moodle. Use [this handout](/docs/vcd-3650-lesson-5.pdf) to take notes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/DNYpPFYV4_M" frameborder="0" allowfullscreen></iframe>         

</Subpage>
<Subpage slug="commit-to-memory">

### Commit to Memory

#### The DRE

Full Document Ready Event Handler:

```js
$(document).ready(function() {
    // Do stuff...
});
```

Abbreviated DRE:

```js
$(function() {
    // Do stuff...
});
```

#### jQuery DOM methods

Know what each of these does and any parameters they accept:

* `.html()`
* `.text()`
* `.attr()`
* `.addClass()`
* `.removeClass()`
* `.toggleClass()`
* `.replaceWith()`
* `.before()`
* `.prepend()`
* `.append()`
* `.after()`
* `.remove()`
* `.removeAttr()`

</Subpage>
