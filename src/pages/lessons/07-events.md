---
type: lessons
title: "Events"
number: 7
cover: "https://source.unsplash.com/_Ch_onWf38o"
---
import Subpage from "../../components/subpage.js"

<Subpage slug="events">

### Events in JavaScript and jQuery

Returning to our survey of JavaScript and jQuery concepts, we now turn to the exciting topic of events.

***Read Duckett, Chapter 6, pp.243--250, 260--263, 266--267.***

These pages discuss the basic gyst of what events are and some introduction to how to work with them in straight up JavaScript. In a moment we'll look at how jQuery once again saves the day with some shortcuts. But first note that pp.246--247 list the different events that can be triggered in a webpage.

Also, we're going to expound more on the 3 steps discussed on pp.248--249 for how to set up event listeners and handlers in our class discussion. We'll also unpack the event flow, delegation, and behavior methods addressed in these readings.

Now let's look at the jQuery methods that make things a little simpler.

***Read Duckett, Chapter 7, pp.326--331.***

Finally, let's take one more look at what we've been calling the Document Ready Event (DRE) all-in-one now that we know more about events.

***Read Duckett, Chapter 7, pp.312-313.***

So what we've been doing all this time is putting our code inside an event handler that waits for our full document to load before it is processed. When the document is ready, it issues an event that we can respond to with the code we put in this declaration block. We do this to ensure that all the DOM elements we expect to work with are present before we dive in with JavaScript to manipulate them. Page 313 shows an even shorter version of the DRE all-in-one that you're welcome to start using if you like.

#### Study Questions

1. What are events in JavaScript?
2. List examples of some events that can be triggered on a webpage.
3. What is event binding?
4. What is event bubbling?
5. What is the value of event delegation?
6. Why do we use the DRE all-in-one?
7. List the properties and methods of the jQuery event object.
8. **SKILL:** Use the `.on()` method to listen for and respond to events.

</Subpage>
<Subpage slug="listening-and-responding">

### Listening and Responding

In JavaScript as in most other languages that deal with events we will find a common pattern:

1. We set up *event listeners* that wait for particular events to occur on particular objects. In jQuery this is established with the `.on()` method, particular its first parameter, which specifies the kind of event for which to listen on the selected elements.
2. We configure an *event handler* that will be called in response to a particular event. We configure this through the second parameter of the `.on()` method. We can:
    1. Provide an anonymous function
    2. Name a separate function

Regardless, the contained code will be processed.

Event handlers accept a single parameter, the event that occurred. We usually represent these with the variable `e`.

When we want to work with the element that caused the event in jQuery we often use this pattern:

```js
$(__1__).on(__2__, function(e) {
    var $target = $(e.target);
    // Stuff to do in response...
});
```

Here, `__1__` is the element on which we're listening for `__2__` event to occur. Inside we convert `e.target` to a jQuery object, which we store in `$target`.

</Subpage>
<Subpage slug="presentation-and-demo">

### Presentation and Demo

Watch this presentation and play along in the demo provided in CULearn. Use [this handout](/docs/vcd-3650-lesson-7.pdf) to take notes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/4RNrTndQZdw" frameborder="0" allowfullscreen></iframe>

</Subpage>
<Subpage slug="commit-to-memory">

### Commit to Memory

#### Event binding

Event listener structure (separate handler method):

```js
$(__1__).on(__2__, __3__);
```

1. Selector for an element in the desired event's bubble flow.
2. The event name as a string.
3. The name of a separate function that acts as the event handler.

Event handler function structure:

```js
function __1__(e) {
    __2__
}
```

1. Name of the function.
2. Code that responds to the event.

Event listener structure (all-in-one handler):

```js
$(__1__).on(__2__, function(e){
    __3__
});
```

1. Selector for an element in the desired event's bubble flow.
2. The event name as a string.
3. The code that responds to the event.

#### Common operations with event objects:

Stop the default action of the event:

```js
e.preventDefault();
```

Capture the event's target object and as a jQuery object (Use any variable name desired for `$target`):

```js
var $target = $(e.target);
```

</Subpage>
