
# JavaScript DOM Table of Content

### Document Object Model (DOM)
The Document Object Model (DOM) is an API (Application Programming Interface) used to interact with HTML documents. It represents the structured hierarchy of an HTML document as a tree-like structure, allowing developers to access, manipulate, and modify the content and structure of web pages dynamically.

Example:
Suppose you have an HTML document with the following structure:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>DOM Example</title>
  </head>
  <body>
    <h1>Hello, DOM!</h1>
    <p>This is a paragraph.</p>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
    </ul>
  </body>
</html>
```
<hr>
## Nodes and Types of Nodes
Nodes in the DOM represent individual parts of an HTML document. There are several types of nodes, including:
```
Element Nodes: These represent HTML elements, such as <div>, <p>, or <ul>.
```

Text Nodes: These represent the text content within an element.

Attribute Nodes: These represent attributes of an element.

Comment Nodes: These represent comments within the HTML code.

<hr>

## Selecting Elements Using DOM
To manipulate elements in the DOM, you can select them using various methods. Here are some common ones:
>getElementById()
getElementsByName()
getElementsByTagName()
getElementsByClassName()
querySelector() and querySelectorAll()

### getElementById()
This method allows you to select an element by its unique id attribute. It returns the first element with the specified ID.


If you have multiple elements with the same id in an HTML document, the document.getElementById method is supposed to return the first element it encounters with that id. However, it's important to note that having multiple elements with the same id in HTML is invalid and can lead to unpredictable behavior in your code.

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
  <div id="myElement">Element 1</div>
  <div>Another Element</div>
  <div id="myElement">Element 2</div>
</body>
</html>

```

```js
var element = document.getElementById("myElement");
```

If you use document.getElementById("myElement") in this case, it may return the first element with the id "myElement" (which is "Element 1" in this example). However, this behavior is not guaranteed, and it's considered bad practice to have multiple elements with the same id in your HTML. HTML specifications require id attributes to be unique within a document.

To select multiple elements, you should use classes or other attributes and utilize methods like getElementsByClassName, querySelectorAll, or other means depending on your needs.


The best practice for naming elements with id attributes is to ensure that each id is unique within the entire HTML document. Having multiple elements with the same id is invalid HTML and can lead to unpredictable behavior when using JavaScript or CSS to target those elements.

If you want to identify multiple elements in a similar way, you can use classes instead of id attributes. Here's an example of how you can modify your HTML to use classes:

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body>
  <div class="myElement">Element 1</div>
  <div>Another Element</div>
  <div class="myElement">Element 2</div>
</body>
</html>


In this example, both <div> elements have the class "myElement," which is a more appropriate way to group and identify multiple elements that share similar characteristics.
```

To select elements with a specific class in JavaScript, you can use the getElementsByClassName method or the querySelectorAll method. Here's an example using getElementsByClassName:
```js
var elements = document.getElementsByClassName("myElement");

// Now, elements is a collection of elements with the "myElement" class.
// You can access and manipulate these elements as needed.
```
<br>

>**How do I access particular element which has same class name?**

When multiple elements share the same class name, and you want to access a specific element among them, you typically have several options:

Use an Index: You can access elements by their index within the collection returned by getElementsByClassName or querySelectorAll. For example, if you want to access the second element with the class "myElement," you can do this:
```js
var elements = document.getElementsByClassName("myElement");
var secondElement = elements[1]; // Indexing is zero-based, so [1] refers to the second element.
```

Use More Specific Selectors: If you want to target a specific element with a given class, but that class is used on multiple elements, you can make your selector more specific by combining it with other attributes or by nesting it within a parent element. For example, if you have the following HTML:

```
<div class="myElement">Element 1</div>
<div class="myElement">Element 2</div>
<div class="myElement">Element 3</div>

```

```js
var secondElement = document.querySelector("div.myElement:nth-child(2)");
//This query will select the second div element with the class "myElement."
```
Assign Unique Identifiers: If you need to work with specific elements frequently, consider assigning unique identifiers (IDs) to those elements, even if they share a common class. You can then use getElementById to access them directly by their IDs, which are guaranteed to be unique.

<hr>
### getElementsByName()
You can select elements by their name attribute. It returns a collection of elements with the specified name.

```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByName Example</title>
</head>
<body>
    <input type="text" name="myName" value="Value 1">
    <input type="text" name="myName" value="Value 2">
    <input type="text" name="myName" value="Value 3">
    <script src="script.js"></script>
</body>
</html>

```
```js
var elements = document.getElementsByName("myName");
console.log(elements); // NodeList(2) [input, input]
```
Example code:
```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByName Example</title>
</head>
<body>
    <input type="text" name="username" value="John">
    <input type="text" name="username" value="Doe">
    <input type="text" name="email" value="johndoe@example.com">
    <button id="btn">Get Username</button>

    <div id="output"></div>

    <script src="script.js"></script>
</body>
</html>

```

```js
document.addEventListener("DOMContentLoaded", function () {
    var button = document.getElementById("btn");
    var output = document.getElementById("output");

    button.addEventListener("click", function () {
        var elements = document.getElementsByName("username");

        // Loop through the elements and display their values
        var usernames = [];
        for (var i = 0; i < elements.length; i++) {
            usernames.push(elements[i].value);
        }

        output.textContent = "Usernames: " + usernames.join(", ");
    });
});

```
<hr>

### getElementsByTagName()

This method selects elements by their HTML tag name, returning a collection of matching elements.
```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByTagName Example</title>
</head>
<body>
    <p>This is the first paragraph.</p>
    <p>This is the second paragraph.</p>
    <p>This is the third paragraph.</p>
    <button id="btn">Get Paragraphs</button>

    <script src="script.js"></script>
</body>
</html>
```
```js
var paragraphs = document.getElementsByTagName("p");
console.log(paragraphs); //HTMLCollection(3) [p, p, p]
```
Example code:
```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByTagName Example</title>
</head>
<body>
    <p>This is the first paragraph.</p>
    <p>This is the second paragraph.</p>
    <p>This is the third paragraph.</p>
    <button id="btn">Get Paragraphs</button>

    <script src="script.js"></script>
</body>
</html>
```
```js
document.addEventListener("DOMContentLoaded", function () {
    var button = document.getElementById("btn");

    button.addEventListener("click", function () {
        var paragraphs = document.getElementsByTagName("p");

        // Loop through the paragraphs and log their content
        for (var i = 0; i < paragraphs.length; i++) {
            console.log("Paragraph " + (i + 1) + ": " + paragraphs[i].textContent);
        }
    });
});
```
<hr>
### getElementsByClassName()
You can select elements by their class name. It returns a collection of elements with the specified class.

```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByName Example</title>
</head>
<body>
    <p class="para">This is the first paragraph.</p>
    <p class="para">This is the second paragraph.</p>
    <p class="para">This is the third paragraph.</p>
    <button id="btn">Get Paragraphs</button>
</body>
</html>
```

```js
 var paragraphs = document.getElementsByClassName("para");
 console.log(paragraphs); //HTMLCollection(3) [p.para, p.para, p.para]
```

```html

<!DOCTYPE html>
<html>
<head>
    <title>getElementsByName Example</title>
</head>

<body>
    <h1 class="message">first heading</h1>
    <div id="container">
        <h1 class="message">second heading</h1>
        <h1 class="message">third heading</h1>
    </div>
</body>

</html>
```
```js
    let cont = document.getElementById("container");
    let msg = cont.getElementsByClassName("message");
    console.log(msg);
```





Example code:
```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByClassName Example</title>
</head>
<body>
    <h2 class="section-title">Section 1</h2>
    <p class="section-text">This is the content of section 1.</p>
    
    <h2 class="section-title">Section 2</h2>
    <p class="section-text">This is the content of section 2.</p>
    
    <h2 class="section-title">Section 3</h2>
    <p class="section-text">This is the content of section 3.</p>
    
    <button id="btn">Get Sections</button>

    <script src="script.js"></script>
</body>
</html>
```

```js
document.addEventListener("DOMContentLoaded", function () {
    var button = document.getElementById("btn");

    button.addEventListener("click", function () {
        var sectionTitles = document.getElementsByClassName("section-title");
        var sectionTexts = document.getElementsByClassName("section-text");

        // Loop through and log section titles and texts
        for (var i = 0; i < sectionTitles.length; i++) {
            console.log("Section Title " + (i + 1) + ": " + sectionTitles[i].textContent);
            console.log("Section Text " + (i + 1) + ": " + sectionTexts[i].textContent);
        }
    });
});
```
<hr>

>### querySelector() and querySelectorAll()
>These methods allow you to select elements using CSS selectors.

>### querySelector() 
>returns the first element that matches the selector.

```html
<!DOCTYPE html>
<html>
<head>
    <title>getElementsByName Example</title>
</head>
<body>
    <h1 class="message">first heading</h1>
    <div id="container">
        <h1 class="message">second heading</h1>
        <h1 class="message">third heading</h1>
    </div>
</body>
</html>
```

```js
    let msg = document.querySelector(".message");
    console.log(msg); //h1.message
```

Example code:

```html

<!DOCTYPE html>
<html>
<head>
    <title>querySelector Example</title>
</head>
<body>
    <h1>Title</h1>
    <p>This is a paragraph.</p>
    <div class="content">This is a div with class "content".</div>
    <button id="btn">Get Content</button>

    <script src="script.js"></script>
</body>
</html>
```
```js
document.addEventListener("DOMContentLoaded", function () {
    var button = document.getElementById("btn");

    button.addEventListener("click", function () {
        // Select the first <div> element with class "content"
        var contentDiv = document.querySelector("div.content");

        // Log the text content of the selected element
        console.log("Content:", contentDiv.textContent);
    });
});

```

<hr>

>### querySelectorAll() 
>returns a NodeList of all elements that match the selector.

Example code:
```html
<!DOCTYPE html>
<html>
<head>
    <title>querySelectorAll Example</title>
</head>
<body>
    <h1>Title</h1>
    <p class="content">This is a paragraph with class "content".</p>
    <ul>
        <li>Item 1</li>
        <li class="item">Item 2</li>
        <li>Item 3</li>
    </ul>
    <div class="content">This is another div with class "content".</div>
    <button id="btn">Get Content</button>

    <script src="script.js"></script>
</body>
</html>
```

```js
document.addEventListener("DOMContentLoaded", function () {
    var button = document.getElementById("btn");

    button.addEventListener("click", function () {
        // Select elements using document.querySelectorAll

        // Select all <p> elements with class "content"
        var contentParagraphs = document.querySelectorAll("p.content");
        console.log("Content paragraphs:");
        contentParagraphs.forEach(function (paragraph) {
            console.log(paragraph.textContent);
        });

        // Select all <li> elements with class "item"
        var itemElements = document.querySelectorAll("li.item");
        console.log("Item elements:");
        itemElements.forEach(function (item) {
            console.log(item.textContent);
        });

        // Select all <div> elements with class "content"
        var contentDivs = document.querySelectorAll("div.content");
        console.log("Content divs:");
        contentDivs.forEach(function (div) {
            console.log(div.textContent);
        });
    });
});

```


<hr>

> to dod

Traversing elements
Selecting parent element
Selecting child element
Selecting Sibling elements

Manipulating HTML elements
createElement()
appendChild()
textContent
innerHTML
after()
append()
prepend()
insertAdjacentHTML()
replaceChild()
cloneNode()
removeChild()
insertBefore()

Attribute methods
getAttribute()
setAttribute()
hasAttribute()
removeAttribute()

Manipulating Element's Styles
style property
cssText
getComputedStyle()
className property
classList property

JavaScript Events
What is event in JavaScript
Event Bubbling & Event Capturing
Event Handler in HTML Attributes
Event Objects
DOM Level 0 event handlers
addEventListener() and 
removeEventListener()
Different Types of Event