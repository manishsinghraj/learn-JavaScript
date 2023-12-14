# Contents
- what is Js
- Lexical Scoping

## What is JavaScript?

   - High-level, interpreted language.

   - Object-oriented, prototype-based.

   - Client-side scripting for DOM manipulation.

   - Asynchronous, non-blocking operations.

   - Cross-browser compatibility.

   - Versatile: web, server, mobile, game, desktop.

   - Adheres to ECMAScript standard.

   - Dynamically typed variables.

   - Interacts with HTML and CSS.

   - Event driven programming.

<hr>

## JavaScript is a high-level, interpreted programming language
The statement "JavaScript is a high-level, interpreted programming language" breaks down into two key concepts: "high-level" and "interpreted."

1. **High-Level:**
   - A "high-level" programming language is designed to be human-readable and developer-friendly. It abstracts away many low-level details, providing a more user-friendly syntax that is closer to human language. This abstraction simplifies the programming process and allows developers to focus on solving problems without having to manage intricate machine-level details.

   - High-level languages typically have features like built-in memory management, advanced data structures, and abstraction of hardware-related tasks. Examples of high-level languages include JavaScript, Python, Java, and Ruby.

2. **Interpreted:**
   - An "interpreted" language is executed line by line by an interpreter at runtime, as opposed to being compiled into machine code before execution. In the case of JavaScript, the interpreter is built into web browsers.

   - When a user opens a web page containing JavaScript code, the browser's JavaScript engine interprets and executes the code directly. This provides flexibility and ease of development, as developers can see the immediate results of their code changes without the need for a separate compilation step.

   - The interpreted nature of JavaScript also allows for dynamic typing, where variable types are determined at runtime, providing more flexibility but also requiring careful attention to type-related issues.

In summary, describing JavaScript as a "high-level, interpreted programming language" emphasizes its user-friendly syntax and the fact that it is executed by an interpreter at runtime, making it well-suited for web development and providing developers with rapid feedback during the development process.

![Alt text](image.png)



<hr>

## JavaScript is a prototype-based, object-oriented language

When describing JavaScript as a "prototype-based, object-oriented language," it refers to the language's approach to handling object-oriented programming (OOP) concepts. Here's a breakdown of the terms:

1. **Object-Oriented:**
   - JavaScript follows the principles of object-oriented programming, which is a programming paradigm that uses objects as the primary building blocks of software. Objects encapsulate data and behavior related to that data, promoting code organization, reusability, and maintainability.

   - Key OOP concepts in JavaScript include encapsulation, inheritance, and polymorphism.

2. **Prototype-Based:**
   - Unlike classical object-oriented languages (such as Java or C++), which use classes to create objects, JavaScript is prototype-based. In JavaScript, each object can serve as the prototype for another object. Objects inherit properties and behaviors directly from other objects, rather than through classes.

   - Every object in JavaScript has an associated prototype, and this forms a prototype chain. If a property or method is not found on an object, JavaScript looks up the prototype chain until it finds the property or until it reaches the end of the chain.

   - Prototypal inheritance in JavaScript is dynamic, allowing objects to be modified and extended during runtime.

Here's a simple example to illustrate prototypal inheritance in JavaScript:

```javascript
// Creating an object with a method
const person = {
    sayHello: function() {
        console.log('Hello, I am ' + this.name);
    }
};

// Creating a new object that inherits from the 'person' object
const john = Object.create(person);
john.name = 'John';

// Now 'john' has access to the 'sayHello' method through prototypal inheritance
john.sayHello(); // Output: Hello, I am John
```

In this example, the `person` object acts as a prototype for the `john` object. The `sayHello` method is shared through the prototype chain.

In summary, describing JavaScript as a "prototype-based, object-oriented language" highlights its unique approach to implementing object-oriented programming concepts using prototypal inheritance.


<hr>

## Variables in JavaScript

1. **Declaration:**
   - Variables are declared using the `var`, `let`, or `const` keywords.
   - `var` is function-scoped, while `let` and `const` are block-scoped.

2. **Initialization:**
   - Variables can be initialized (assigned a value) at the time of declaration or later in the code.

   ```javascript
   let age; // Declaration
   age = 25; // Initialization
   ```

3. **Hoisting:**
   - Variable declarations are hoisted to the top of their scope during the compilation phase.
   - However, only the declaration is hoisted, not the initialization.

4. **Scope:**
   - Variables have function scope (`var`) or block scope (`let`, `const`).
   - `let` and `const` introduced block-scoping in ES6, providing better control over variable visibility.

5. **Assignment:**
   - Values are assigned using the `=` operator.
   - Variables can be reassigned unless declared with `const`.

   ```javascript
   let name = "John";
   name = "Doe"; // Reassignment is possible with 'let'
   ```

6. **Data Types:**
   - JavaScript is dynamically typed, meaning variables can hold values of different types.

   ```javascript
   let count = 10;      // Number
   let message = "Hi";  // String
   let isTrue = true;   // Boolean
   ```

7. **Mutable vs. Immutable:**
   - Variables declared with `var` and `let` are mutable (can be changed).
   - Variables declared with `const` are immutable and cannot be reassigned.

   ```javascript
   const pi = 3.14;
   // pi = 3.14159; // Error: Cannot reassign a constant variable
   ```

8. **Naming Conventions:**
   - Follow best practices for variable naming:
     - Start with a letter.
     - Use camelCase for multi-word names.
     - Choose meaningful and descriptive names.

   ```javascript
   let totalAmount;
   ```
<hr>

## DataTypes

- **Primitive data types** are simple, immutable values directly stored in memory. They are passed by value, and changes to copies do not affect the original.

- **Non-primitive data types** are more complex data structures that store references to memory locations. They are mutable, passed by reference, and can dynamically change in size.

### Primitive Data Types:

1. **Directly Stored:**
   - Primitive data types are directly stored in memory, and they hold a simple, single value.

2. **Immutable:**
   - They are immutable, meaning their values cannot be changed once they are assigned.

3. **Pass by Value:**
   - When you pass a primitive data type to a function or assign it to another variable, a copy of the value is made. Changes to the copy don't affect the original.

4. **Limited in Size:**
   - Primitives have a fixed size in memory, which is determined by the type of the variable.

5. **Examples:**
   - Number, String, Boolean, Undefined, Null, Symbol.

### Non-Primitive (Reference) Data Types:

1. **Reference Stored:**
   - Non-primitive data types store references to the memory location where the data is held, rather than the actual data.

2. **Mutable:**
   - They are mutable, and changes to the data can affect other variables that reference the same data.

3. **Pass by Reference:**
   - When passed to a function or assigned to another variable, the reference to the data is passed, not a copy of the actual data.

4. **Dynamic Size:**
   - Non-primitive types can dynamically change in size during runtime.

5. **Examples:**
   - Object, Array, Function, Date.


### Example
JavaScript has several data types that are used to represent different kinds of values. Here are the primary data types in JavaScript:

1. **Primitive Data Types:**

   - **Number:** Represents numeric values.
     ```javascript
     let age = 25;
     let pi = 3.14;
     ```

   - **String:** Represents sequences of characters.
     ```javascript
     let name = "John";
     let message = 'Hello, World!';
     ```

   - **Boolean:** Represents true or false values.
     ```javascript
     let isTrue = true;
     let isFalse = false;
     ```

   - **Undefined:** Represents a variable that has been declared but not assigned a value.
     ```javascript
     let undefinedVar;
     ```

   - **Null:** Represents the absence of any object value.
     ```javascript
     let nullVar = null;
     ```

   - **Symbol (ES6 and later):** Represents a unique identifier.
     ```javascript
     let sym = Symbol('uniqueSymbol');
     ```

2. **Object Data Type:**

   - **Object:** Represents a collection of key-value pairs.
     ```javascript
     let person = {
         name: 'John',
         age: 30,
         isStudent: false
     };
     ```

3. **Derived Data Types:**

   - **Function:** Represents a reusable block of code.
     ```javascript
     function greet(name) {
         return 'Hello, ' + name + '!';
     }
     ```

   - **Array:** Represents an ordered list of values.
     ```javascript
     let numbers = [1, 2, 3, 4, 5];
     ```

   - **Date:** Represents a specific point in time.
     ```javascript
     let currentDate = new Date();
     ```

<hr>

 ## Operators

JavaScript provides a variety of operators for performing different operations on values. Here's an overview of some common types of operators in JavaScript:

### Arithmetic Operators:

1. **Addition (+):**
   ```javascript
   let sum = 5 + 3; // 8
   ```

2. **Subtraction (-):**
   ```javascript
   let difference = 8 - 3; // 5
   ```

3. **Multiplication (*):**
   ```javascript
   let product = 4 * 2; // 8
   ```

4. **Division (/):**
   ```javascript
   let quotient = 10 / 2; // 5
   ```

5. **Modulus (%):**
   ```javascript
   let remainder = 15 % 4; // 3
   ```

### Assignment Operators:

6. **Assignment (=):**
   ```javascript
   let x = 10;
   ```

7. **Addition Assignment (+=):**
   ```javascript
   let y = 5;
   y += 3; // y is now 8
   ```

8. **Subtraction Assignment (-=):**
   ```javascript
   let z = 10;
   z -= 4; // z is now 6
   ```

### Comparison Operators:

9. **Equal (==):**
   ```javascript
   let isEqual = 5 == '5'; // true (loose equality)
   ```

10. **Strict Equal (===):**
    ```javascript
    let isStrictEqual = 5 === '5'; // false (strict equality)
    ```

11. **Not Equal (!=):**
    ```javascript
    let isNotEqual = 10 != '10'; // false (loose inequality)
    ```

12. **Strict Not Equal (!==):**
    ```javascript
    let isStrictNotEqual = 10 !== '10'; // true (strict inequality)
    ```

### Logical Operators:

13. **Logical AND (&&):**
    ```javascript
    if (x > 0 && y < 10) {
        // Code executes if both conditions are true
    }
    ```

14. **Logical OR (||):**
    ```javascript
    if (a === 'hello' || b === 'world') {
        // Code executes if at least one condition is true
    }
    ```

15. **Logical NOT (!):**
    ```javascript
    if (!isLoggedin) {
        // Code executes if isLoggedin is false
    }
    ```

### Other Operators:

16. **Increment (++):**
    ```javascript
    let counter = 5;
    counter++; // counter is now 6
    ```

17. **Decrement (--):**
    ```javascript
    let counter = 5;
    counter--; // counter is now 4
    ```

18. **Conditional (Ternary) Operator (? :):**
    ```javascript
    let result = (age >= 18) ? 'Adult' : 'Minor';
    ```


<hr>

## JS Scope and Scope Chain

**Scope in JavaScript:**

Scope in JavaScript refers to the context in which variables are declared, defined, and accessed. It determines the visibility and accessibility of variables throughout the code. JavaScript has two main types of scope:

1. **Global Scope:**
   - Variables declared outside of any function or block have global scope.
   - They are accessible from any part of the code, including within functions.

   ```javascript
   let globalVar = 10;

   function exampleFunction() {
       console.log(globalVar); // Accessible within the function
   }
   ```

2. **Local (Function) Scope:**
   - Variables declared inside a function have local scope.
   - They are only accessible within that function.

   ```javascript
   function exampleFunction() {
       let localVar = 20;
       console.log(localVar); // Accessible within the function
   }

   // console.log(localVar); // Error: localVar is not defined outside the function
   ```

**Scope Chain:**

The scope chain in JavaScript refers to the hierarchy of scopes. When a variable is referenced, JavaScript looks for it in the current scope. If it's not found, it looks in the outer scope, continuing up the chain until the global scope is reached. This concept is essential for understanding variable resolution in nested functions.

Example of Scope Chain:

```javascript
let globalVar = 'I am global';

function outerFunction() {
    let outerVar = 'I am outer';

    function innerFunction() {
        let innerVar = 'I am inner';
        console.log(innerVar);   // Access innerVar
        console.log(outerVar);   // Access outerVar from the outer function
        console.log(globalVar);  // Access globalVar from the global scope
    }

    innerFunction();
}

outerFunction();
```

In this example, `innerFunction` has access to variables in its local scope (`innerVar`), the scope of the outer function (`outerVar`), and the global scope (`globalVar`). This nesting creates a scope chain that allows inner scopes to access variables in outer scopes.

### how it has acess to this console.log(globalVar)?

In JavaScript, functions have access to variables from their containing or outer scopes. This behavior is known as **lexical** scoping, where the scope of a variable is determined by its position in the source code.

In your provided example:

```javascript
let globalVar = 'I am global';

function outerFunction() {
    let outerVar = 'I am outer';

    function innerFunction() {
        let innerVar = 'I am inner';
        console.log(innerVar);   // Access innerVar
        console.log(outerVar);   // Access outerVar from the outer function
        console.log(globalVar);  // Access globalVar from the global scope
    }

    innerFunction();
}

outerFunction();
```

The `innerFunction` is nested inside `outerFunction`. When `innerFunction` is invoked, it looks for variables within its own scope first (`innerVar`), then looks in the scope of its containing function (`outerFunction`) for `outerVar`. If it doesn't find `outerVar` there, it continues up the scope chain to the global scope, where it finds and can access `globalVar`.

This is why `innerFunction` can successfully log the values of `innerVar`, `outerVar`, and `globalVar`. The lexical scoping rules allow functions to access variables from their enclosing scopes, creating a scope chain. In this case, `innerFunction` has access to the global scope through the chain of its containing functions (`outerFunction`).

<hr>

## What is Lexical Scoping?

Lexical scoping, also known as static scoping, is a way of defining variable scope in a programming language. Lexical scoping determines the scope of a variable based on its position in the source code, at the time the code is written. The term "lexical" refers to the lexicon or vocabulary of a language, and in this context, it emphasizes the relationship between the variable and its surrounding code structure.

In a lexically scoped language:

1. **Scope is Defined by Code Structure:**
   - The scope of a variable is determined by its location in the source code and the structure of the code.

2. **Nested Functions:**
   - Functions in a lexically scoped language have access to variables defined in their outer (containing) functions.

3. **Closure:**
   - A closure is formed when a function is defined inside another function, and it "closes over" the variables in its lexical scope, preserving access to those variables even after the outer function has completed execution.

Here's a simple example in JavaScript to illustrate lexical scoping:

```javascript
function outerFunction() {
    let outerVar = 'I am outer';

    function innerFunction() {
        let innerVar = 'I am inner';
        console.log(innerVar);   // Access innerVar
        console.log(outerVar);   // Access outerVar from the outer function
    }

    innerFunction();
}

outerFunction();
```

In this example, `innerFunction` is lexically scoped within `outerFunction`. As a result, it has access to `outerVar` even though it is called after `outerFunction` has finished execution.

Lexical scoping is a key concept in many programming languages, including JavaScript. It contributes to the predictability and clarity of variable access, as the scope is determined by the structure of the code rather than the runtime behavior.

<hr>

## What is Closure?

A closure is a feature in programming languages that allows a function to remember the variables from the scope in which it was created, even if the function is executed in a different scope. In other words, a closure gives a function access to its own scope, the scope of the outer function, and the global scope, forming a "closed-over" environment of variables.

Suppose we want to create a counter function that maintains its own count and allows us to increment the count. We can use a closure to encapsulate the count variable and expose methods to interact with it:

```javascript
function createCounter() {
    let count = 0;

    // The inner function, increment, is a closure
    function increment() {
        count++;
        console.log(count);
    }

    // Return the inner function, creating a closure
    return increment;
}

// Create two independent counters
const counter1 = createCounter();
const counter2 = createCounter();

// Each counter maintains its own count due to closures
counter1(); // Output: 1
counter1(); // Output: 2

counter2(); // Output: 1 (independent of counter1)
counter2(); // Output: 2
```

In this example:

- `createCounter` is a function that defines a local variable `count` and an inner function `increment`.
- The `increment` function is a closure because it references the `count` variable from its containing scope.
- When `createCounter` is invoked, it returns the `increment` function, creating a closure.
- We create two independent counters (`counter1` and `counter2`) by calling `createCounter` twice.
- Each counter maintains its own private count variable, and calling the `counter1` or `counter2` function increments its count independently.

Closures allow the inner function (`increment` in this case) to remember and access the variables from its outer scope (`createCounter`). This behavior enables us to create functions with private state and behavior, enhancing modularity and encapsulation in our code.

<hr>

## Functions in JS

Functions are a fundamental building block in JavaScript, allowing you to encapsulate and reuse blocks of code. Here's an overview of key concepts related to functions in JavaScript:

### 1. **Function Declaration:**
   - You can declare a function using the `function` keyword.
   ```javascript
   function greet(name) {
       console.log('Hello, ' + name + '!');
   }
   ```

### 2. **Function Expression:**
   - You can also assign a function to a variable.
   ```javascript
   const greet = function(name) {
       console.log('Hello, ' + name + '!');
   };
   ```

### 3. **Arrow Functions (ES6 and later):**
   - A concise way to write functions.
   ```javascript
   const greet = (name) => {
       console.log('Hello, ' + name + '!');
   };
   ```

### 4. **Function Invocation:**
   - Call a function to execute its code.
   ```javascript
   greet('John');
   ```

### 5. **Parameters and Arguments:**
   - Parameters are placeholders in the function declaration.
   - Arguments are actual values passed when calling the function.
   ```javascript
   function add(x, y) {
       return x + y;
   }
   console.log(add(3, 5)); // Output: 8
   ```

### 6. **Return Statement:**
   - Functions can return a value using the `return` keyword.
   ```javascript
   function multiply(x, y) {
       return x * y;
   }
   ```

### 7. **Default Parameters (ES6 and later):**
   - Provide default values for parameters.
   ```javascript
   function power(x, exponent = 2) {
       return Math.pow(x, exponent);
   }
   ```

### 8. **Rest Parameters (ES6 and later):**
   - Capture multiple arguments into an array.
   ```javascript
   function sum(...numbers) {
       return numbers.reduce((total, num) => total + num, 0);
   }
   ```

### 9. **Higher-Order Functions:**
   - Functions that take other functions as parameters or return functions.
   ```javascript
   function operate(x, y, operation) {
       return operation(x, y);
   }
   ```

### 10. **Callback Functions:**
   - Functions passed as arguments to other functions.
   ```javascript
   function processArray(array, callback) {
       return array.map(callback);
   }
   ```

### 11. **Closures:**
   - Functions that "close over" variables from their outer scope.
   ```javascript
   function createCounter() {
       let count = 0;
       return function() {
           count++;
           return count;
       };
   }
   ```

### 12. **Immediately Invoked Function Expressions (IIFE):**
   - Functions that are executed immediately after they are created.
   ```javascript
   (function() {
       console.log('I am an IIFE!');
   })();
   ```

### EXAMPLE

```JS 
// JS parseInt function 
const num1 = parseInt("3.14"); 
console.log('Using parseInt("3.14") = ' + num1); 
// Output: Using parseInt("3.14") = 3

// JS parseFloat function 
// It returns floating point Number until 
// it encounters Not a Number character 
const num2 = parseFloat("2018.12@geeksforgeeks"); 
console.log('parseFloat("2018@geeksforgeeks") = ' + num2); 
// Output: parseFloat("2018@geeksforgeeks") = 2018.12

// JS isNaN function 
console.log(isNaN(12)); 
// Output: false (because 12 is a number)

// JS Number() function 
const num3 = Number(true); 
console.log("Value of 'true': " + num3); 
// Output: Value of 'true': 1 (because Number(true) converts boolean true to 1)

// JS eval() function 
function evalfn() { 
	const a = 4; 
	const b = 4; 
	const value = eval(new String(a * b)); 
	console.log(value); 
} 
evalfn(); 
// Output: 16 (because eval evaluates the expression in the string)

// JS encode URI function 
const url = "https://www.google.com/search?q=geeks for geeks"; 
const encodedURL = encodeURI(url); 
console.log(encodedURL); 
// Output: https://www.google.com/search?q=geeks%20for%20geeks

```

<hr>

## Document Object Model

The DOM (Document Object Model) is a programming interface for web documents. It represents the structure of a document as a tree of objects, where each object corresponds to a part of the document, such as elements, attributes, and text. The DOM provides a way for programs to manipulate the structure, style, and content of web documents.

Here are key concepts related to the DOM:

### 1. **Document:**
   - The top-level object that represents the entire HTML or XML document.
   - Accessed using the `document` object.

   ```javascript
   const doc = document;
   ```

### 2. **Element:**
   - Represents an HTML or XML element in the document.
   - Accessed using methods like `getElementById` or `querySelector`.

   ```javascript
   const element = document.getElementById('myElement');
   ```

### 3. **Node:**
   - The basic building blocks of the DOM.
   - Elements, attributes, and text are types of nodes.

### 4. **Attribute:**
   - Represents an attribute of an HTML or XML element.
   - Accessed using methods like `getAttribute` and `setAttribute`.

   ```javascript
   const value = element.getAttribute('data-id');
   ```

### 5. **Event:**
   - Represents an occurrence that can be detected and handled.
   - Examples include clicks, keypresses, and form submissions.

   ```javascript
   element.addEventListener('click', handleClick);
   ```

### 6. **Traversal:**
   - Moving between nodes in the DOM tree.
   - Methods like `parentNode`, `childNodes`, `nextSibling`, and `previousSibling`.

   ```javascript
   const parent = element.parentNode;
   ```

### 7. **Manipulation:**
   - Changing the structure, content, or style of elements.
   - Methods like `appendChild`, `removeChild`, `innerHTML`, and `style`.

   ```javascript
   element.innerHTML = '<p>New content</p>';
   ```

### 8. **Forms:**
   - Accessing and manipulating form elements and their values.
   - Methods like `submit`, `reset`, and properties like `value`.

   ```javascript
   const input = document.getElementById('username');
   const inputValue = input.value;
   ```

### 9. **CSS:**
   - Accessing and manipulating styles applied to elements.
   - Methods like `getComputedStyle` and properties like `style`.

   ```javascript
   const bgColor = window.getComputedStyle(element).backgroundColor;
   ```

### 10. **Creating Elements:**
   - Dynamically creating new elements and adding them to the document.
   - Methods like `createElement` and `appendChild`.

   ```javascript
   const newElement = document.createElement('div');
   document.body.appendChild(newElement);
   ```


<hr>

## Events

In web development, events are occurrences or happenings that can be detected and responded to by your web page or application. JavaScript provides mechanisms to handle events and execute code in response to user interactions or other activities. Here are key concepts related to events in web development:

### 1. **Event Types:**
   - Events can be triggered by various actions, such as user interactions, changes in the document, or network activity.
   - Common event types include clicks, keypresses, mouse movements, form submissions, and more.

### 2. **Event Handling:**
   - Event handling involves defining functions (event handlers) to respond to specific events.
   - Event handlers are attached to HTML elements using attributes like `onclick` or by using JavaScript methods.

   ```html
   <button onclick="myFunction()">Click me</button>
   ```

   ```javascript
   const button = document.querySelector('button');
   button.addEventListener('click', myFunction);
   ```

### 3. **Event Listener:**
   - An event listener is a JavaScript function that listens for a specific event type on a target element.
   - It is added using the `addEventListener` method.

   ```javascript
   element.addEventListener('click', function(event) {
       // Handle the click event
   });
   ```

### 4. **Event Object:**
   - When an event occurs, an event object is created and passed to the event handler.
   - The event object contains information about the event, such as the target element, type, and any additional data.

   ```javascript
   element.addEventListener('click', function(event) {
       console.log(event.type); // 'click'
       console.log(event.target); // The element that triggered the event
   });
   ```

### 5. **Event Propagation:**
   - Events in the DOM can propagate through different phases: capturing, target, and bubbling.
   - The `addEventListener` method can capture events during the capturing phase or handle them during the bubbling phase.

   ```javascript
   element.addEventListener('click', function(event) {
       // Handle the click event during the bubbling phase
   });
   ```

### 6. **Event Delegation:**
   - Event delegation involves attaching a single event listener to a common ancestor of multiple elements.
   - It allows handling events for multiple elements with a single event handler.

   ```javascript
   document.addEventListener('click', function(event) {
       if (event.target.tagName === 'BUTTON') {
           // Handle click on a button
       }
   });
   ```

   - without event delegation

    
   ```javascript

        <ul id="myList">
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <!-- More list items dynamically added later -->
        </ul>
    
        const items = document.querySelectorAll('#myList li');
        
        items.forEach((item) => {
            item.addEventListener('click', function() {
                console.log(`Clicked on ${item.textContent}`);
            });
        });
    
   ```

   - without event delegation
    
   ```js 
    const list = document.getElementById('myList');

    list.addEventListener('click', function(event) {
        const target = event.target;
    
        if (target.tagName === 'LI') {
            console.log(`Clicked on ${target.textContent}`);
        }
    });

   ```

### 7. **Preventing Default Behavior:**
   - Some events have default behaviors (e.g., form submission, link navigation).
   - You can prevent the default behavior using the `event.preventDefault()` method.

   ```javascript
   form.addEventListener('submit', function(event) {
       event.preventDefault();
       // Handle form submission without navigating
   });
   ```

### 8. **Asynchronous Events:**
   - Events can be asynchronous, such as those triggered by network requests or timeouts.
   - Promises, callbacks, or `async/await` can be used to handle asynchronous events.

   ```javascript
   fetch('https://api.example.com/data')
       .then(response => response.json())
       .then(data => console.log(data))
       .catch(error => console.error(error));
   ```

<hr>

# Event Bubbling

Event bubbling is a phase in the event propagation model of the Document Object Model (DOM) in web browsers. When an event occurs on a specific element, such as a button click or a keypress, the event doesn't just stop there. Instead, it propagates or bubbles up through the ancestor elements of the target element.

The event starts from the target element, then moves up through its parent elements all the way to the root of the document (or to the first ancestor with a capturing event listener).

Here's a simple illustration of event bubbling:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event Bubbling Example</title>
    <style>
        div {
            padding: 10px;
            border: 1px solid #ccc;
            margin: 10px;
        }
    </style>
</head>
<body>

<div id="outer">
    <div id="middle">
        <div id="inner">Click me!</div>
    </div>
</div>

<script>
    document.getElementById('outer').addEventListener('click', function() {
        console.log('Outer div clicked!');
    });

    document.getElementById('middle').addEventListener('click', function() {
        console.log('Middle div clicked!');
    });

    document.getElementById('inner').addEventListener('click', function() {
        console.log('Inner div clicked!');
    });
</script>

</body>
</html>
```

In this example, if you click on the "Click me!" text inside the innermost `div` element, you will see all three log statements in the console: "Inner div clicked!", "Middle div clicked!", and "Outer div clicked!".

This is because the click event bubbles up through the ancestor elements, and each ancestor with a click event listener is notified and can respond to the event.

Event bubbling allows for a more flexible and efficient way to handle events. You can attach a single event listener to a common ancestor and handle events for multiple elements within that ancestor. It simplifies event delegation and reduces the need for attaching listeners to every individual element.

### what is the real example advantage? is this the feature?

Yes, event bubbling is a feature of the DOM that offers advantages, especially when it comes to handling events efficiently and managing code in a more organized way. Here are some real-world examples and advantages:

1. **Event Delegation:**
   - Event bubbling enables a technique known as event delegation. Instead of attaching event listeners to individual elements, you can attach a single event listener to a common ancestor. This is particularly useful when dealing with dynamic content or a large number of elements. For example, if you have a list of items, you can attach a click event listener to the entire list container rather than to each list item.

    ```html
    <ul id="myList">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>

    <script>
        document.getElementById('myList').addEventListener('click', function(event) {
            if (event.target.tagName === 'LI') {
                console.log('List item clicked:', event.target.textContent);
            }
        });
    </script>
    ```

2. **Performance:**
   - With event delegation, you reduce the number of event listeners in your application, which can lead to better performance, especially when dealing with a large number of elements. Instead of attaching individual listeners to each element, you handle events at a higher level.

3. **Dynamic Content:**
   - Event bubbling works well with dynamically generated content. If you add new elements to the DOM, they automatically inherit the event handlers from their ancestors. You don't need to manually attach listeners to newly added elements.

    ```javascript
    const newElement = document.createElement('li');
    newElement.textContent = 'New Item';
    document.getElementById('myList').appendChild(newElement);
    ```

4. **Code Organization:**
   - Handling events at a higher level promotes cleaner and more organized code. You can centralize your event handling logic in one place rather than scattering it across various elements.

In summary, event bubbling is a useful feature for creating more maintainable and efficient code, especially in scenarios where you want to handle events for multiple elements or dynamically generated content. It promotes a more streamlined approach to event handling and helps improve the overall performance of your web applications.

<hr>

## Event Propagation

Event propagation refers to the process by which events in the DOM (Document Object Model) traverse or propagate through the hierarchy of elements. There are two phases in event propagation: capturing phase and bubbling phase.

### 1. Capturing Phase:
- In the capturing phase, the browser starts from the root of the DOM tree and goes down to the target element. It checks for any elements that have registered a capturing event listener for the specific type of event.
- Event capturing is less commonly used but can be useful in certain scenarios.
- You can add a capturing event listener by setting the third parameter of `addEventListener` to `true`.

```javascript
element.addEventListener('click', handleEvent, true);
```

### 2. Target Phase:
- Once the event reaches the target element, the target phase begins. This is where the actual event target (the element that triggered the event) is processed, and any event listeners attached to it are executed.

### 3. Bubbling Phase:
- After the target phase, the event starts to bubble up from the target element back to the root of the DOM tree.
- During the bubbling phase, any ancestor elements that have registered a bubbling event listener for the specific type of event will be notified and can respond to the event.

Here's an example to illustrate event propagation:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event Propagation Example</title>
    <style>
        div {
            padding: 10px;
            border: 1px solid #ccc;
            margin: 10px;
        }
    </style>
</head>
<body>

<div id="outer">
    <div id="middle">
        <div id="inner">Click me!</div>
    </div>
</div>

<script>
    document.getElementById('outer').addEventListener('click', function() {
        console.log('Outer div clicked!');
    }, true);

    document.getElementById('middle').addEventListener('click', function() {
        console.log('Middle div clicked!');
    }, true);

    document.getElementById('inner').addEventListener('click', function() {
        console.log('Inner div clicked!');
    });
</script>

</body>
</html>
```

In this example, if you click on the "Click me!" text inside the innermost `div` element, you will see the following log statements in the console:

```
Outer div clicked!
Middle div clicked!
Inner div clicked!
```

This log order reflects the capturing phase followed by the target phase and then the bubbling phase.


<hr>

## window

In JavaScript, the `window` object represents the global window or the browser window in a web environment. It provides a set of properties and methods that allow interaction with the browser window and its content. Here are some important properties of the `window` object:

### 1. **Document:**
   - The `document` property represents the Document object associated with the window, providing access to the HTML document's structure and content.

   ```javascript
   const documentObject = window.document;
   ```

### 2. **Location:**
   - The `location` property represents the current URL of the window. It can be used to navigate to a different URL.

   ```javascript
   const currentURL = window.location.href;
   ```

### 3. **Navigator:**
   - The `navigator` property provides information about the browser's name, version, platform, etc.

   ```javascript
   const browserName = window.navigator.userAgent;
   ```

### 4. **History:**
   - The `history` property represents the browsing history and allows navigation through the session history.

   ```javascript
   window.history.back(); // Move back one page in the browser history
   ```

### 5. **Screen:**
   - The `screen` property provides information about the user's screen, such as width, height, and color depth.

   ```javascript
   const screenWidth = window.screen.width;
   ```

### 6. **Frames:**
   - The `frames` property represents an array-like object containing all the frames (iframes) in the current window.

   ```javascript
   const frameCount = window.frames.length;
   ```

### 7. **Inner and Outer Width/Height:**
   - The `innerWidth` and `innerHeight` properties represent the viewport's width and height excluding browser chrome.

   ```javascript
   const viewportWidth = window.innerWidth;
   ```

   - The `outerWidth` and `outerHeight` properties represent the width and height of the entire browser window.

   ```javascript
   const windowWidth = window.outerWidth;
   ```

### 8. **Scrolling:**
   - The `scrollX` and `scrollY` properties represent the number of pixels that the document is currently scrolled horizontally and vertically.

   ```javascript
   const scrollPositionX = window.scrollX;
   ```

### 9. **Alert, Confirm, Prompt:**
   - The `alert()`, `confirm()`, and `prompt()` methods are available on the `window` object for displaying dialogs.

   ```javascript
   window.alert('Hello, world!');
   ```

### 10. **Timers:**
   - The `setTimeout()` and `setInterval()` methods are used for scheduling code execution after a specified delay.

   ```javascript
   const timeoutID = window.setTimeout(function() {
       console.log('Delayed code execution');
   }, 1000);
   ```

<hr>

## == and ===

In JavaScript, `==` (equality operator) and `===` (strict equality operator) are used for comparing values. However, they have different behaviors regarding type coercion.

### `==` (Equality Operator):

- The `==` operator compares values for equality after performing type coercion if the operand types are different.
- If the types are different, JavaScript attempts to convert one or both operands to a common type before making the comparison.
- This can lead to unexpected results, especially when comparing values of different types.

#### Example:

```javascript
console.log(5 == '5');  // true (type coercion: '5' is coerced to number 5)
console.log(true == 1);  // true (type coercion: true is coerced to number 1)
console.log(null == undefined);  // true (type coercion: null is coerced to undefined)
```

### `===` (Strict Equality Operator):

- The `===` operator checks for equality without performing type coercion.
- It requires both the value and the type to be the same for the comparison to be true.

#### Example:

```javascript
console.log(5 === '5');  // false (strict equality: different types)
console.log(true === 1);  // false (strict equality: different types)
console.log(null === undefined);  // false (strict equality: different types)
```

### When to Use Which:

- Use `===` for most equality comparisons because it avoids unexpected type coercion.
- Use `==` only when you specifically want to perform type coercion and consider the potential side effects.

#### Note:

- It's generally recommended to use strict equality (`===`) to avoid unexpected behavior caused by type coercion.
- The equality operators are commonly used in conditional statements, comparisons, and other scenarios where you need to check if two values are equal.


### console.log(null === undefined); what are their types?

In JavaScript, `null` and `undefined` are distinct values with different types, and using the strict equality operator (`===`) to compare them will yield `false`. 

```javascript
console.log(null === undefined); // Output: false
```

Here's a brief explanation of their types:

- **`null`**:
  - `null` is a primitive value in JavaScript.
  - It represents the intentional absence of any object value.
  - The type of `null` is, unsurprisingly, `object`.

- **`undefined`**:
  - `undefined` is a primitive value as well.
  - It represents an uninitialized or undefined value.
  - The type of `undefined` is `undefined`.

So, even though both `null` and `undefined` are often used interchangeably to represent the absence of a meaningful value, they are distinct values with different types in JavaScript.


<hr>


## hoisting

Hoisting is a JavaScript behavior where function and variable declarations are moved to the top of their containing scope during the compilation phase. This means you can use a function or variable before it's declared in the code. However, it's important to note that only the declarations are hoisted, not the initializations.

Here's an example of function hoisting:

```javascript
// Function declaration
hoistedFunction(); // This works even though the function is called before its declaration

function hoistedFunction() {
    console.log('Hello, I am hoisted!');
}

// Function expression
// This would result in an error because function expressions are not hoisted
// notHoistedFunction(); // TypeError: notHoistedFunction is not a function

var notHoistedFunction = function() {
    console.log('I am not hoisted!');
};
```

In this example:

1. The `hoistedFunction` is declared using a function declaration. You can call this function even before its declaration in the code, thanks to hoisting.

2. The `notHoistedFunction` is declared using a function expression. Unlike function declarations, function expressions are not hoisted in the same way, and trying to call the function before its declaration would result in a `TypeError`.

It's a good practice to declare functions before they are used, even though hoisting allows calling them before the declaration. This helps improve code readability and avoids potential issues with variable hoisting.

### function expression means?

A function expression in JavaScript is a way to define a function as part of an expression. In other words, a function expression produces a value, and you can assign this value to a variable or use it as an argument in a function call. Function expressions are often used for creating anonymous functions or functions that are only needed for a short duration.

Here's the basic syntax of a function expression:

```javascript
const myFunction = function() {
    // Function body
    console.log('This is a function expression.');
};

// You can now call the function using the variable name
myFunction();
```

In the example above:

- `myFunction` is a variable that holds the function value.
- The function itself is defined using the `function` keyword followed by a set of parentheses for parameters (which are empty in this case) and a block of code for the function body.

Function expressions can also be used for creating anonymous functions, which are functions without a name:

```javascript
const addNumbers = function(x, y) {
    return x + y;
};

// Anonymous function used in an array method
const numbers = [1, 2, 3];
const squared = numbers.map(function(num) {
    return num * num;
});
```

In this example, `addNumbers` is a named function expression, while the function used in the `map` method is an anonymous function expression.

It's worth noting that function expressions have some advantages, such as the ability to create functions dynamically and pass them as arguments to other functions. They are also subject to variable scope rules and can be used in places where a function declaration might not be syntactically valid.

<hr>


## This Keyword

The `this` keyword in JavaScript is a special keyword that refers to the object it belongs to. The behavior of `this` can vary depending on how a function is called. Here are different scenarios where the behavior of `this` changes:

### 1. **Global Context:**
   - In the global context (outside any function or object), `this` refers to the global object (in a browser environment, it's typically the `window` object).

   ```javascript
   console.log(this === window); // Output: true
   ```

### 2. **Function Context:**
   - In a regular function (not an arrow function), `this` refers to the global object when the function is called in the global scope or in strict mode.

   ```javascript
   function logThis() {
       console.log(this);
   }

   logThis(); // Output: window (or global object in Node.js)
   ```

### 3. **Method Context:**
   - When a function is a method of an object, `this` refers to the object the method is called on.

   ```javascript
   const myObject = {
       myMethod: function() {
           console.log(this);
       }
   };

   myObject.myMethod(); // Output: myObject
   ```

### 4. **Constructor Context:**
   - When a function is used as a constructor with the `new` keyword, `this` refers to the newly created object.

   ```javascript
   function MyConstructor() {
       this.property = 'Hello';
   }

   const myInstance = new MyConstructor();
   console.log(myInstance.property); // Output: Hello
   ```

### 5. **Event Handler:**
   - In an event handler, `this` often refers to the element that triggered the event.

   ```javascript
   const myButton = document.getElementById('myButton');
   myButton.addEventListener('click', function() {
       console.log(this); // Output: myButton
   });
   ```

### 6. **Arrow Functions:**
   - Arrow functions do not have their own `this` context. They inherit `this` from the enclosing lexical scope.

   ```javascript
   const myObject = {
       myMethod: function() {
           setTimeout(() => {
               console.log(this);
           }, 1000);
       }
   };

   myObject.myMethod(); // Output: myObject
   ```

Understanding the different behaviors of `this` is crucial for writing effective and bug-free JavaScript code, especially in scenarios like event handling, method invocation, or object construction. Arrow functions are often used in situations where you want to preserve the lexical scope of `this`.

<hr>

##  Promises

Promises in JavaScript are a way to handle asynchronous operations. They provide a clean and more structured approach for managing asynchronous code compared to callbacks. A Promise represents a value that might be available now, or in the future, or never.

Here is a basic overview of Promises:

### Creating a Promise:

A Promise is created using the `Promise` constructor, which takes a function called the executor. The executor function has two parameters: `resolve` and `reject`.

```javascript
const myPromise = new Promise((resolve, reject) => {
    // Asynchronous operation
    setTimeout(() => {
        const success = true; // Simulating a successful operation
        if (success) {
            resolve('Operation completed successfully!');
        } else {
            reject('Operation failed!');
        }
    }, 2000);
});
```

### Handling Promise Results:

Once a Promise is created, you can use the `.then()` method to handle the resolved value and the `.catch()` method to handle any errors (rejected value).

```javascript
myPromise
    .then((result) => {
        console.log(result); // Output: Operation completed successfully!
    })
    .catch((error) => {
        console.error(error); // Output: Operation failed!
    });
```

### Chaining Promises:

Promises can be chained together using `.then()` to perform a sequence of asynchronous operations.

```javascript
const firstPromise = new Promise((resolve) => {
    resolve(1);
});

firstPromise
    .then((value) => {
        console.log(value); // Output: 1
        return value + 1;
    })
    .then((value) => {
        console.log(value); // Output: 2
        return value * 2;
    })
    .then((value) => {
        console.log(value); // Output: 4
    });
```

### Handling Multiple Promises:

You can use `Promise.all()` to wait for multiple promises to resolve. It returns a new promise that resolves with an array of results when all the provided promises have resolved.

```javascript
const promise1 = Promise.resolve('One');
const promise2 = new Promise((resolve) => setTimeout(() => resolve('Two'), 1000));
const promise3 = Promise.reject('Three'); // Simulating a rejected promise

Promise.all([promise1, promise2, promise3])
    .then((results) => {
        console.log(results); // Output: ['One', 'Two', 'Three']
    })
    .catch((error) => {
        console.error(error); // Output: 'Three'
    });
```

Promises are a fundamental part of modern JavaScript and are widely used for handling asynchronous operations, such as fetching data from an API, reading files, or performing other non-blocking tasks. They provide a more structured and readable way to work with asynchronous code compared to traditional callback patterns.

<hr>

## map, filter, reduce

`map`, `filter`, and `reduce` are higher-order functions in JavaScript that operate on arrays. They provide a concise and functional programming approach to perform common operations on arrays.

### 1. `map`:

The `map` function transforms each element of an array using a provided callback function and returns a new array containing the results.

```javascript
const numbers = [1, 2, 3, 4, 5];

const squaredNumbers = numbers.map((num) => num * num);

console.log(squaredNumbers); // Output: [1, 4, 9, 16, 25]
```

### 2. `filter`:

The `filter` function creates a new array containing only the elements that satisfy a given condition specified by a callback function.

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((num) => num % 2 === 0);

console.log(evenNumbers); // Output: [2, 4]
```

### 3. `reduce`:

The `reduce` function iterates over the elements of an array and accumulates a single result by applying a callback function.

```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, current) => accumulator + current, 0);

console.log(sum); // Output: 15
```

In the `reduce` example:
- `accumulator` is the accumulated result.
- `current` is the current element being processed.
- `0` is the initial value of the accumulator.

These functions are often used together to perform complex operations on arrays in a concise and expressive manner. For example, you might use `map` to transform data, `filter` to select specific elements, and `reduce` to compute a single result. This functional programming paradigm is often referred to as "chaining" these array methods.

```javascript
const numbers = [1, 2, 3, 4, 5];

const result = numbers
  .filter((num) => num % 2 === 0) // Filter even numbers
  .map((num) => num * num)         // Square each number
  .reduce((acc, cur) => acc + cur, 0); // Sum the squared numbers

console.log(result); // Output: 20
```

This chain of operations filters even numbers, squares them, and then calculates their sum. It's a powerful and readable way to express array transformations and computations in JavaScript.

### Example 2:

Sure, let's go through real-world examples for `map`, `filter`, and `reduce`.

### 1. `map` Example:

Suppose you have an array of user objects, and you want to create a new array containing only their names:

```javascript
const users = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' },
  { id: 3, name: 'Charlie' }
];

const userNames = users.map(user => user.name);

console.log(userNames);
// Output: ['Alice', 'Bob', 'Charlie']
```

### 2. `filter` Example:

Let's say you have an array of numbers, and you want to filter out only the even numbers:

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];

const evenNumbers = numbers.filter(num => num % 2 === 0);

console.log(evenNumbers);
// Output: [2, 4, 6, 8]
```

### 3. `reduce` Example:

Assume you have an array of expenses, and you want to calculate the total expense:

```javascript
const expenses = [100, 50, 75, 120, 45];

const totalExpense = expenses.reduce((acc, expense) => acc + expense, 0);

console.log(totalExpense);
// Output: 390
```



<hr>

# Callback function

A callback function in JavaScript is a function that is passed as an argument to another function and is executed after the completion of some asynchronous operation or at a later time. Callbacks are a way to handle tasks asynchronously, such as handling events, making HTTP requests, or reading files.

Here's a simple example of a callback function:

```javascript
function fetchData(callback) {
    // Simulating an asynchronous operation (e.g., fetching data from a server)
    setTimeout(() => {
        const data = 'Fetched data';
        // Call the callback function with the fetched data
        callback(data);
    }, 2000);
}

// Define a callback function
function handleData(data) {
    console.log('Handling data:', data);
}

// Call the fetchData function and pass the handleData function as a callback
fetchData(handleData);
```

In this example:

1. The `fetchData` function takes a callback function (`handleData`) as an argument.
2. Inside `fetchData`, there is a simulated asynchronous operation (a `setTimeout` in this case).
3. After the asynchronous operation is completed, the callback function (`handleData`) is invoked with the fetched data.

Callback functions are commonly used in scenarios such as:

- Event handling: Callbacks are often used to respond to events like button clicks or keyboard inputs.
- Asynchronous operations: Callbacks are used to handle the results of asynchronous operations like reading files, making HTTP requests, or querying databases.
- Callback-based APIs: Many libraries and frameworks use callback patterns to handle asynchronous code execution.

While callbacks are a fundamental part of JavaScript, they can lead to callback hell (also known as the pyramid of doom) when dealing with nested callbacks. To address this, modern JavaScript has introduced Promises and async/await, providing more structured and readable ways to handle asynchronous code.

<hr>

## Inheritance in JS

In JavaScript, inheritance is implemented using prototypes. Objects in JavaScript are linked to other objects through a prototype chain. Each object has a prototype object from which it inherits properties and methods. The prototype-based inheritance in JavaScript is different from classical inheritance in languages like Java or C++, as JavaScript is a prototype-based language.

Here's a basic example of how inheritance works in JavaScript:

```javascript
// Parent constructor function
function Animal(name) {
    this.name = name;
}

// Adding a method to the prototype of Animal
Animal.prototype.sayHello = function() {
    console.log(`Hello, I'm ${this.name}`);
};

// Child constructor function inheriting from Animal
function Dog(name, breed) {
    // Call the parent constructor using call or apply
    Animal.call(this, name);
    this.breed = breed;
}

// Set up the prototype chain: Dog.prototype inherits from Animal.prototype
Dog.prototype = Object.create(Animal.prototype);

// Adding a method to the prototype of Dog
Dog.prototype.bark = function() {
    console.log('Woof! Woof!');
};

// Creating instances of Animal and Dog
const animal = new Animal('Generic Animal');
const dog = new Dog('Buddy', 'Golden Retriever');

// Calling methods on instances
animal.sayHello();  // Output: Hello, I'm Generic Animal
dog.sayHello();     // Output: Hello, I'm Buddy
dog.bark();         // Output: Woof! Woof!
```

In this example:

1. We have a `Animal` constructor function with a `sayHello` method added to its prototype.

2. We create a `Dog` constructor function that inherits from `Animal` by setting its prototype to a new object created with `Object.create(Animal.prototype)`.

3. The `Dog` constructor calls the `Animal` constructor using `Animal.call(this, name)` to set the `name` property.

4. We add a `bark` method to the prototype of `Dog`.

5. Instances of `Animal` and `Dog` are created, and they can access methods defined in their prototypes.

It's important to note that JavaScript has introduced the `class` syntax in ECMAScript 2015 (ES6), which provides a more convenient syntax for creating and inheriting from classes. However, under the hood, it still uses prototype-based inheritance. The example above demonstrates the classic prototype-based approach for better understanding.

### ModernWay

The modern way to handle inheritance in JavaScript is to use the `class` syntax introduced in ECMAScript 2015 (ES6). While it's important to note that JavaScript's underlying model is still prototype-based, the `class` syntax provides a more familiar and syntactically convenient way to work with constructor functions, prototypes, and inheritance.

Here's the same example as before, but using the `class` syntax:

```javascript
// Parent class
class Animal {
    constructor(name) {
        this.name = name;
    }

    sayHello() {
        console.log(`Hello, I'm ${this.name}`);
    }
}

// Child class inheriting from Animal
class Dog extends Animal {
    constructor(name, breed) {
        super(name); // Call the parent constructor using super
        this.breed = breed;
    }

    bark() {
        console.log('Woof! Woof!');
    }
}

// Creating instances of Animal and Dog
const animal = new Animal('Generic Animal');
const dog = new Dog('Buddy', 'Golden Retriever');

// Calling methods on instances
animal.sayHello();  // Output: Hello, I'm Generic Animal
dog.sayHello();     // Output: Hello, I'm Buddy
dog.bark();         // Output: Woof! Woof!
```

Key points:

- `class` allows a more structured and readable way to define constructor functions and methods.
- `extends` is used for inheritance, and `super` is used to call the constructor of the parent class.
- The `class` syntax doesn't change the underlying prototype-based nature of JavaScript; it's just a syntactic sugar for working with prototypes and constructor functions.

Using `class` syntax is considered more idiomatic and is widely adopted in modern JavaScript development. It provides a clearer and more concise syntax for handling object-oriented programming concepts.

<hr>

## Getter and Setter

In JavaScript, getter and setter methods allow you to define and control access to an object's properties. They are special methods that allow you to get and set the values of properties in a more controlled manner, enabling you to perform actions or validations when a property is accessed or modified.

### Getter:

A getter is a method that gets the value of a specific property. It is defined using the `get` keyword followed by the property name.

```javascript
class Circle {
    constructor(radius) {
        this._radius = radius; // Convention: prefix with an underscore to indicate it's a private property
    }

    get radius() {
        return this._radius;
    }

    get area() {
        return Math.PI * this._radius ** 2;
    }
}

const myCircle = new Circle(5);
console.log(myCircle.radius); // Output: 5
console.log(myCircle.area);   // Output: 78.53981633974483
```

In this example, `radius` and `area` are getter methods. You access them like regular properties, but they are computed on the fly.

### Setter:

A setter is a method that sets the value of a specific property. It is defined using the `set` keyword followed by the property name.

```javascript
class Circle {
    constructor(radius) {
        this._radius = radius;
    }

    get radius() {
        return this._radius;
    }

    set radius(newRadius) {
        if (newRadius > 0) {
            this._radius = newRadius;
        } else {
            console.log('Invalid radius value');
        }
    }

    get area() {
        return Math.PI * this._radius ** 2;
    }
}

const myCircle = new Circle(5);
console.log(myCircle.radius); // Output: 5

myCircle.radius = 8;
console.log(myCircle.radius); // Output: 8

myCircle.radius = -3; // Output: Invalid radius value
console.log(myCircle.radius); // Output: 8 (unchanged)
```

In this example, `radius` is a setter method. It allows you to set the value of `radius` while also performing a validation check (ensuring that the new radius is greater than 0).

Using getter and setter methods provides better encapsulation and control over the behavior of object properties. They are commonly used in classes, especially when you want to perform some logic when getting or setting values.

### so what is the actual benefit of using getter when compared to normal method?

Using getters in JavaScript provides several benefits when compared to normal methods:

1. **Property Syntax:**
   - Getters allow you to access a property using a syntax that looks like accessing a regular property rather than calling a method with parentheses.

2. **Code Readability:**
   - Getters improve code readability by providing a more natural and intuitive way to access properties. This can make your code cleaner and easier to understand.

3. **Encapsulation:**
   - Getters allow you to encapsulate the logic for computing or deriving a property's value within the object. This promotes encapsulation and information hiding, making the internal implementation details less visible.

4. **Consistent Interface:**
   - Getters help in maintaining a consistent interface with other properties of the object. When other developers or yourself interact with the object, they can treat computed properties the same way as regular properties.

5. **Lazy Evaluation:**
   - Getters enable lazy evaluation, meaning that the computation is performed only when the property is accessed. This can be beneficial for performance, especially when dealing with expensive or resource-intensive computations.

Here's a comparison between a normal method and a getter for illustration:

Using a normal method:

```javascript
class Circle {
    constructor(radius) {
        this._radius = radius;
    }

    getRadius() {
        return this._radius;
    }
}

const myCircle = new Circle(5);
console.log(myCircle.getRadius()); // Method syntax
```

Using a getter:

```javascript
class Circle {
    constructor(radius) {
        this._radius = radius;
    }

    get radius() {
        return this._radius;
    }
}

const myCircle = new Circle(5);
console.log(myCircle.radius); // Property syntax
```

In this comparison, the getter syntax (`myCircle.radius`) provides a more natural and concise way to access the property compared to the method syntax (`myCircle.getRadius()`). The benefit becomes more apparent when interacting with objects in a more property-oriented manner.

### tell me what Encapsulation here means?

Certainly! Encapsulation refers to bundling the data (properties) and the methods (functions) that operate on the data within a single unit, such as a class. This helps hide the internal implementation details of the object from the outside world, exposing only what is necessary for the object's interface.

Let's consider an example without encapsulation:

```javascript
class CircleWithoutEncapsulation {
    constructor(radius) {
        this.radius = radius;
    }

    getArea() {
        return Math.PI * this.radius ** 2;
    }
}

const myCircle = new CircleWithoutEncapsulation(5);
console.log(myCircle.getArea()); // Output: 78.53981633974483
console.log(myCircle.radius);    // Direct access to the radius property
```

In this example, the `radius` property is exposed, and external code can directly access and modify it, bypassing any logic or validation that might be necessary.

Now, let's consider an example with encapsulation using a getter:

```javascript
class CircleWithEncapsulation {
    constructor(radius) {
        this._radius = radius; // Private property
    }

    get radius() {
        return this._radius;
    }

    get area() {
        return Math.PI * this._radius ** 2;
    }
}

const myCircle = new CircleWithEncapsulation(5);
console.log(myCircle.area);    // Output: 78.53981633974483
console.log(myCircle.radius);  // Accessing the radius property through the getter
```

In this example:

- The `radius` property is accessed through a getter, providing a controlled way to expose the value.
- The actual data is stored in a private property `_radius`, and external code cannot directly access or modify it.
- The `area` property is computed based on the `_radius`, and external code interacts with it without needing to know the internal details.

By encapsulating the logic within the object and using getters, you control how the properties are accessed, modified, and computed, hiding the internal implementation details and providing a more robust and maintainable design. This is a fundamental principle in object-oriented programming that helps manage complexity and promotes a clear and consistent interface for interacting with objects.

<hr>

## Fetch 

`fetch` is a modern JavaScript API for making network requests. It provides a cleaner and more powerful interface compared to older alternatives like XMLHttpRequest. The `fetch` function returns a Promise that resolves to the `Response` to that request, whether it is successful or not.

Here's a basic example of how to use `fetch`:

```javascript
fetch('https://api.example.com/data')
  .then(response => {
    // Check if the request was successful
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
    // Parse the response as JSON
    return response.json();
  })
  .then(data => {
    // Handle the parsed data
    console.log(data);
  })
  .catch(error => {
    // Handle errors
    console.error('Fetch error:', error);
  });
```

Key points:

- `fetch` takes a URL as its first argument. You can also provide an optional configuration object as the second argument.
- The `then` method is used to handle the asynchronous response from the server.
- The first `then` block checks if the response was successful (`response.ok`). If not, it throws an error to jump to the `catch` block.
- The second `then` block parses the response as JSON. You might need to use other methods like `text()`, `blob()`, etc., depending on the response type.
- The `catch` block handles any errors that occurred during the fetch.

### Fetch with Configuration:

You can provide additional configuration options like method, headers, and body:

```javascript
fetch('https://api.example.com/data', {
  method: 'POST', // or 'GET', 'PUT', etc.
  headers: {
    'Content-Type': 'application/json',
    // Other headers as needed
  },
  body: JSON.stringify({
    key1: 'value1',
    key2: 'value2',
  }),
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Fetch error:', error));
```

In this example, we're making a POST request with a JSON payload. Adjust the method, headers, and body according to your API requirements.

### Asynchronous/Await:

You can also use the `async/await` syntax for cleaner and more readable code:

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Fetch error:', error);
  }
}

fetchData();
```

Using `async/await` makes the code look synchronous while preserving the benefits of asynchronous behavior.

<hr>

## bind call  apply

`bind`, `call`, and `apply` are methods in JavaScript that are used to manipulate how functions are invoked and set the context (the value of `this`). Here's a brief overview of each:

### 1. `bind`:

- **Purpose:** Creates a new function that, when called, has its `this` keyword set to a specified value.
- **Syntax:**
  ```javascript
  const newFunction = originalFunction.bind(thisValue);
  ```
- **Example:**
  ```javascript
  const person = {
    name: 'John',
    greet: function() {
      console.log(`Hello, ${this.name}!`);
    },
  };

  const greetFunction = person.greet;
  greetFunction(); // This would normally throw an error because `this` is undefined.

  const boundGreetFunction = person.greet.bind(person);
  boundGreetFunction(); // Outputs: Hello, John!
  ```

### 2. `call`:

- **Purpose:** Invokes a function with a specified `this` value and passes arguments individually.
- **Syntax:**
  ```javascript
  originalFunction.call(thisValue, arg1, arg2, ...);
  ```
- **Example:**
  ```javascript
  const person = {
    name: 'John',
    greet: function(greeting) {
      console.log(`${greeting}, ${this.name}!`);
    },
  };

  person.greet.call(person, 'Hi'); // Outputs: Hi, John!
  ```

### 3. `apply`:

- **Purpose:** Invokes a function with a specified `this` value and passes an array or array-like object of arguments.
- **Syntax:**
  ```javascript
  originalFunction.apply(thisValue, [arg1, arg2, ...]);
  ```
- **Example:**
  ```javascript
  const person = {
    name: 'John',
    greet: function(greeting) {
      console.log(`${greeting}, ${this.name}!`);
    },
  };

  person.greet.apply(person, ['Hi']); // Outputs: Hi, John!
  ```

### Key Differences:

- `bind` creates a new function with a bound `this` value, but it doesn't invoke the function immediately. It returns a new function that can be invoked later.
- `call` and `apply` both invoke the function immediately. The only difference is how arguments are passed: individually for `call` and as an array for `apply`.
- All three methods are used for setting the context (`this`) for a function.
- These methods are particularly useful when dealing with callback functions, method borrowing, or situations where you want to explicitly set the `this` value.

It's important to choose the appropriate method based on the specific requirements of your code.

<hr>


<hr>


<hr>


<hr>

<hr>


<hr>
<hr>


<hr>

<hr>


<hr>

<hr>


<hr>

<hr>


<hr>