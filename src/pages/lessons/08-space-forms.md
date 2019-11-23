---
type: lessons
title: "Space and Forms"
number: 8
cover: "https://source.unsplash.com/4kEWGyAtz34"
---
import { Subpage, Callout } from "course-components";

<Subpage slug="embracing-space">

### Embracing Space

Let's step back into IxD1 to look at the role space plays in interactive interfaces.

<Callout lead={true} color="secondary">

Read IxD1, Chapter 7: Embracing Space in Interaction Design

</Callout>

Note that the item labeled #3 on p.110 is formatted incorrectly. It looks like a third implication of the law of proximity, but it is supposed to be the third function white space plays in interaction design.

#### Study Questions

1. What three functions does white space play in interaction design?
2. What are the four kinds of white space?
3. What is the law of proximity?
4. What two implications that the law of proximity has for interaction design?
5. Describe the role chunking can play in interaction design.
6. Explain the Law of Context.

</Subpage>
<Subpage slug="form-review">

### Form Review

You may recall studying the basic tags used for working with forms in Web 1 and Web 2. We finally have much more to go on now to talk more about how they all work.

Here's an example for us to consider:

```html
<form action="submit.php" method="post">
    <ul>
        <li>
            <label for="name">Name:</label>
            <input type="text" name="name" id="name" value="" />
        </li>
        <li>
            Requesting a reply:
            <ul>
                <li>
                    <input type="radio" name="reply" id="reply-yes" value="yes" />
                    <label for="age-yes">Yes</label>
                </li>
                <li>
                    <input type="radio" name="reply" id="reply-no" value="no" />
                    <label for="age-no">No</label>
                </li>
            </ul>
        </li>
        <li>
            <label for="age">Age range</label>
            <select name="age" id="age">
                <option value="under-18">Under 18</option>
                <option value="between-18-and-30">Between 18 and 30</option>
                <option value="30-up">30 and older</option>
            </select>
        </li>
        <li>
            <label for="msg">Message:</label>
            <textarea name="msg" id="msg"></textarea>
        </li>
    </ul>
    <p><button name="send" type="submit">Send</button></p>
</form>
```

And lets imagine that the user has entered the following data or selections:

Name:
: `Phil`  

Requesting a reply:
: Selected the `Yes` radio button

Age range:
: Selected the `30 and older` option

Message:
: `Hello world and how are you`

#### Configuring the Form

Let's start with the container, the `<form>` tag. This tag allows us to collect and configure a set of data:

* **WHICH data:** The `<form>` tag should be used to wrap around all the elements collect data for a given form. This is usually just one per page, but can be several in a single-page application. Here we wrap it around `name`, `reply`, `age`, `msg`, and `send`. More on the fields themselves later...
* **WHERE to send the data:** Use the `action` attribute to indicate the file or URL to which the data entered in this form should be sent when it is submitted. This is called the processing script. In this case, when the user enters data and presses submit, this data will be sent to `submit.php`.
* **HOW to package the data:** Use the `method` attribute to set the form to submit either as `get` or as `post` data.
    * `get` will send the data to the recipient script using the `GET` http method, which means the variables and data are encrypted as an URL string and sent with the page name like this:

        ```
        submit.php?name=Phil&reply=yes&age=30-up&msg=Hello+world+and+how+are+you
        ```

        Notice how what is sent is the `value` attributes for corresponding fields/selections except for the text input fields. The text input fields transforms he provided text into URL-encoded text.

    * `post` will send the data in a more secure fashion by packaging the data into the header of the HTTP request sent to `submit.php`. Prefer using this method with forms.

Note here that while we're learning more about the elements and settings, we're still going to rely on other technology to actually process the data. In this case we're referencing a PHP script that will handle the data. PHP is a programming language that runs on similar concepts as JavaScript but is better saved for another class.

#### Labeling the fields

In well-formed HTML forms we should always provide a `label` for each field. Then we also connect the label to the corresponding field by providing the `for` attribute and setting it tot he corresponding field's `id` attribute.

So take note of how we have a `label` for each field in the example above:

* The `name` field has its own label as do the `age` and `msg` fields.
* Each radio button in the `reply` field group has its own label, again, pointing to each respective `id` attribute. These fields therefore just have plain text "Reply requested:" before them.

#### Collecting Data

Finally we need an actual widget to collect the data we need from the user. Below is a table reminding you of all the different widget options. But first, note the following:

* Each widget should get its own unique `id` attribute so that you can pair it with a `label` as discussed above.
* Each widget group should have its own `name` attribute. These become the label for the data submitted to the processing script. In most cases, each widget would have a distinct value here, such as you can see with `name`, `age`, and `msg`. But note that the radio buttons both have the same `name`. This ensure that they act as a group, allowing only one of the two to be selected. The same goes for checkboxes.

Here is a reminder of the kinds of "widgets" we can create and which tag and setting to use.

| Widget | `input` tag with `type` set to... | `button` tag with `type` set to... | Other tag... |
|:=================|:===========|:==========|:=|
| Single-line text | `text`     |           |  |
| Multi-line text  |            |           | `<textarea>` |
| Password text    | `password` |           |  |
| Submit button    | `submit`   | `submit`  |  |
| Reset button     | `reset`    | `reset`   |  |
| Misc button      |            | (default) |  |
| Radio button     | `radio`    |           |  |
| Checkbox         | `checkbox` |           |  |
| Drop-down list   |            |           | `<select>` with a series of `<option>`s. |
| Selection list   |            |           | `<select>` with a series of `<option>`s. Set `size` to 1 or more to determine how many are visible. |

Many of these can be created with the `input` tag but with a different `type` setting. The `button` tag should be preferred for the three widgets shown despite the overlap.

So with this review of elements, take another look at the sample form provided above. This form contains the following widgets:

* A single line text input with the name `name`.
* Two radio buttons that are grouped as a series with the name `reply`.
* A drop-down list with the name `age`.
* A Multi-line text box with the name `msg`.  

</Subpage>
<Subpage slug="forms-and-events">

### Forms and Events in jQuery

One last set of selectors to understand when working with jQuery is those that pertain specifically to form elements.

First, be sure you're familiar with HTML form elements. If you did not learn these when you took earlier Web Design classes, please see the provided review documents.

<Callout lead={true} color="secondary">

Read Duckett, Chapter 7, pp.342-345.

</Callout>

#### Study Questions

1. List some examples of selectors you can use with form elements in jQuery.
2. List the methods and events you can use with form elements in jQuery.
3. **SKILL:** Read and write the value of a form field using `.val()`.

</Subpage>
<Subpage slug="presentation-and-demo">

### Presentation and Demo

Watch this presentation and play along in the demo provided in CULearn. Use [this handout](/docs/vcd-3650-lesson-8.pdf) to take notes.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EWvp-Rjpi5E" frameborder="0" allowfullscreen></iframe>

</Subpage>
