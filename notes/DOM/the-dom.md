>[home](../../home.md)
# The DOM

### What is the dom?

It is `The Document Object Model` and it provides a means to interact with an HTML document.

## **1. Accessing HTML elements**

Ways to access elements:

- `getElementsByTagName`
- `getElementsByClassName`
- `getElementById`
- `getElementByName`
- `getElementByTagNameNS`

Most common ways"

- `getElementByName`:
  - by `p` or `div` for instance.
  - return an `array`(nodelist) of elements, because more than one of each element can exist
- `getElementByName`:
  - by class name
  - return an `array` (nodelist) of elements.
- `getElementById`:
  - return a single element

Unlike with CSS `IDs`, accessing elements in scripts doesn't effect specificity and makes it easier to find specific elements.

Using a `Class` is useful for manipulating multiple elements on a page.

## **2. Selecting elements from HTML**

### **querySelector()**

The `querySelector()` method returns the _first_ match only.

> `document.querySelector()`

- `document.querySelector('h1')`
- `document.querySelector('p')`

The `querySelectorAll()` method returns all instances of matching elements

> `document.QuerySelectorAll()`

    document.querySelectorAll('p')
    NodeList(15) [p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph, p.paragraph]

**`querySelector` can also use class `.` and/or ID `#`:**

- `document.querySelector('#w3scools')`
- `document.querySelector('a#w3schools')`
- `document.querySelectorAll('.dom')`

## **3. Using HTML Elements**

**_Some methods to access and change HTML elements are:_**

- The `for` loop:

> the example below is searching for elements with `.dom` class

    var spans = document.querySelectorAll('.dom')
    for (var i = 0; i < spans.length; i++) {
      spans[i].innerHTML = 'HTML5 Document Object Model'
    }

- The `slice` method to convert the `nodelist` into an array

        var spans = Array.prototype.slice.call(document.querySelectorAll('.dom'))
        spans.forEach(function (span) { span.innerHTML = 'HTML5 Document Object Model' })

  - Having created an Array The `setAttribute` method can be used(same example as above)

        spans.forEach(function(span) { span.setAttribute('style', 'color: red; font-weight:bold')})

## **4. The DOM and Events**

## Events:

When a user interacts with a webpage, we want it to react.
As users we want and interactive experience.

When "events" ('click', 'mouseenter', 'keyup' [More examples here...](https://developer.mozilla.org/en-US/docs/Web/Events)) occur they need to be captured.

### **_Event Handler and Callback Functions_**

"Event handlers" are attached to interactive objects.
"event handlers" are linked with a "callback" function, which is called when an event occurs.

> In this example the `event handler` is `id= "way-cool-button"` is added to a button:

      <!DOCTYPE html>
      <html lang="en">
        <head>
          <title>Test</title>
        </head>
        <body>
          <div id="app">
            <header>
              <h1>My event test page</h1>
            </header>
            <main>
              <button id="way-cool-button">Click me!</button>
            </main>
        </body>
      </html>

> One `Callback` function is:

    document.querySelector('#way-cool-button').onclick = function (event) {
      console.log(event)
    }

This method only allows one `event` to be added and only one `callback` for each object.

> Another `callback` function is:

    document.querySelector('#way-cool-button').addEventListener(
      'click',
      function (event) { console.log(event) },
      false
    )

[**_Link to list of HTML DOM Events_**](https://www.w3schools.com/jsref/dom_obj_event.asp)

## Example 1: Way Cool Button

> This example shows an `Event` being captured

    <!DOCTYPE html>
    <html lang="en">
      <head>
        <title>Test</title>
      </head>
      <body>
        <div id="app">
          <header>
            <h1>My event test page</h1>
          </header>
          <main>
            <button id="way-cool-button">Click me!</button>
          </main>
      </body>
    </html>

Callback:

    document.querySelector('#way-cool-button').onclick = function (event) {
      console.log(event)
    }

![results](https://handbook.eda.nz/images/js-dom-click-me.png)

## Example 2: Event Handler to capture keystrokes

> This example captures keystrokes and prints them in a paragraph below the input box:

    <!DOCTYPE html>
    <html lang="en">
      <head>
        <title>Test</title>
      </head>
      <body>
        <div id="app">
          <header>
            <h1>My keystroke test page</h1>
          </header>
          <main>
            <p>
              <input id="keystroker">
            </p>
            <p id="outputter"></p>
          </main>
      </body>
    </html>


    var input = document.querySelector('#keystroker')
    var output = document.querySelector('#outputter')
    var updater = function (e) { output.innerHTML = input.value }
    input.addEventListener('keyup', updater, false)

![output](https://handbook.eda.nz/images/js-dom-keyup.png)

## Example 3: Form Submission to test Page

    <!DOCTYPE html>
    <html lang="en">
      <head>
        <title>Test</title>
      </head>
      <body>
        <div id="app">
          <header>
            <h1>My form submission test page</h1>
          </header>
          <main>
            <form id="catch-it">
              <input id="some-text">
              <input type="submit">
            </form>
            <p id="outputter"></p>
          </main>
      </body>
    </html>

    var form = document.querySelector('#catch-it')
    var input = document.querySelector('#some-text')
    var output = document.querySelector('#outputter')
    var updater = function (e) {
      e.preventDefault()
      output.innerHTML = 'Submitting form with "' + input.value + '"'
    }
    form.addEventListener('submit', updater, false)

![output](https://handbook.eda.nz/images/js-dom-catching-form-submit.png)

## **Research: The DOM - How it Relates to CSS and HTML:**

### **What is the DOM?**

The role of the `The Document Object Model(DOM)` is to both represent, and provide a means to manipulate, the `Document`.

This representation takes the form of a logical tree, with branches, `nodes` (and associated event handlers) as well as Javascript `objects`:

> **_"Each branch of the tree ends in a node, and each node contains objects. DOM methods allow programmatic access to the tree. With them, you can change the document's structure, style, or content."_** - [mdn - Document Object Model(DOM)](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)

**Another way to think of it is in terms of parent/child elements:**

At the top of the ancestry tree is the Document:

- The `Document` is parent of the `HTML`, which is the parent of the `head`, `body` and their subsequent children elements (`header`, `main`, `footer`) and so on.

**What about CSS?**  
While the `HTML` parses information to the `DOM`, the browser fetches `CSS` (and other resources). The `CSS` searches for `selectors` and maps them onto relevant `nodes` in the `DOM`.

**How can we manipulate the DOM?**
On a functional level, the `DOM` takes `HTML` and `CSS` and transforms them into `Javascript`, which can then be manipulated. Effectively, we are able to manipulate _everything_ in the `document` (`HTML`, `CSS`) with `Javascript` through functions such as `querySelector`.

# Cheat Sheet

## Accessing Keys/Values In an Array

    function updateCounts() {
      var totals = {
        blue: 0,
        green: 0,
        invisible: 0,
      }

      // WRITE CODE HERE TO COUNT BLUE, GREEN, AND INVISIBLE DOTS
      totals.blue = document.getElementsByClassName('blue').length

      totals.green = document.getElementsByClassName('green').length

      totals.invisible = document.getElementsByClassName('invisible').length
      // Once you've done the counting, this function will update the display
      displayTotals(totals)
      }

> Keys and Values can be accessed with dot notation. `totals` for the variable and `blue` for the value inside of the variable.
