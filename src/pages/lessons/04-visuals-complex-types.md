---
type: lessons
title:  "Visual Direction and Complex Data Types"
number: 4
cover: "https://source.unsplash.com/HGNtPpNQBcI"
---
import Subpage from "../../components/subpage.js"

<Subpage slug="intro-to-visuals">

### Introduction to Visuals in IxD

Having spent time thinking distinctly about the words we use in interaction design, we now turn to think critically about the visual design we implement.

***Read IxD1, Chapter 4: Visual Direction in Interaction Design.***

#### Study Questions

1. In what ways is the sense of vision dominant in IxD?
2. What are three requirements for orienting users?
3. What are the seven tips for orienting users to navigation?
4. What are some ways we can ensure visual consistency?

</Subpage>
<Subpage slug="creating-lists">

### Creating Lists of Data with Arrays

The data types we've discussed several primitive data types so far: numbers, strings, and booleans. These provide very basic kinds of data we can store, but we often run into cases where we'd benefit from being able to store sets of data, particularly, lists of similar data.

***Read Duckett, Chapter 2, pp.70--73*** to learn about the Array data type.

#### Study Questions

1. What are arrays?
2. **SKILL:** Create an array using both the array literal technique and the array constructor, and add items to
an existing array using each method as well.
3. **SKILL:** Access items from inside an array.

</Subpage>
<Subpage slug="objects-in-detail">

### Objects in Detail

Its time to get serious about objects. Having studied the other data types, and most recently, arrays, you have
more context to consider what makes objects different and useful. We'll start with a general reading on objects
and how to construct them.

***Read Duckett, Chapter 3, pp.100--119*** to learn about the object data type.

Now let's take a look at some of the objects already set up and available to you through JavaScript.

***Read Duckett, Chapter 3, pp.120--139*** to learn about built-in objects.

#### Study Questions

1. **SKILL:** Create on object using literal notation and constructor notation.
9. **SKILL:** Access properties and methods of an object using dot notation.
10. What is the difference between an object created with the literal notation and an object created with the
constructor notation.
11. What is the `this` keyword?
12. What are built-in objects?
13. What are some features of the `window` object?
14. What are some features of the `document` object?
15. What are some features of the String object?
16. What are some features of the Number object?
17. What are some features of the Math object?
18. What are some features of the Date object?

</Subpage>
<Subpage slug="presentation-and-demo">

### Presentation and Demo

Watch this presentation and play along in the demo provided in CULearn. Use [this handout](/docs/vcd-3650-lesson-4.pdf) to take notes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/1DzO-uP2XA4" frameborder="0" allowfullscreen></iframe>

</Subpage>
<Subpage slug="commit-to-memory">

### Commit to Memory

#### Snippets

Create an array using literal syntax:

```js
var __1__ = [ __2__ ];
```

1. The name of the variable being assigned this array.
2. A comma-separated list of values.

Call an array value:

```js
__1__[ __2__ ]
````

1. The variable storing the array
2. The numerical index of the desired item, counting up from 0

Create an object using literal syntax:

```js
var __1__ = {
    __name1__: __value1__,
    __name2__: __value2__,
    etc...
};
```

1. The variable being assigned this object.
    * Provide a set of name-value pairs with a colon between name and value, and a comma after each
name-value pair.

Call properties or methods of an object with dot notation:

```js
__1__.__2__
````

1. The variable holding the object.
2. The desired property or method. If a method is called, also provide `()` and any parameters required by the methods.

**Define an object/class prototype with constructor syntax:**

```js
function __1__(__2__) {
    // Properties
    this.__3a__...
    this.__3n__...
    // Methods
    this.__4a__ = function...
    this.__4n__ = function...
}
```

1. The name of the object/class, usually capitalized
2. Parameters for setting up the object
3. Any predefined properties using the keyword `this` and assigning the desired value
4. Any predefined methods using the keyword `this` and assigning an anonymous function

**Instantiate any predefined object/class:**

```js
__1__ = new __2__(__3__);
```

1. Typically a variable to store the object instance
2. The name of the object/class after the keyword new
3. Any parameters allowed by the object

#### Built-in objects

Be familiar with what is possible with each of the following built-in objects:

* `window`
* `document`
* String
* Number
* Array
* Math
* Date

</Subpage>
