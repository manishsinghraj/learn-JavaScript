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



# JavaScript var let const Interview Questions and Answers

## Example 1
```javascript
{
    var a = 5;
    let b = 5;
    const c = 5;
}

console.log(a); // Output: 5
console.log(c); // Output: ReferenceError: c is not defined
console.log(b); // Output: ReferenceError: b is not defined
```
**Explanation:** In this example, `a` is declared using `var`, making it accessible outside the block, while `b` and `c` are declared using `let` and `const` respectively, making them block-scoped variables. Therefore, `a` is accessible outside the block, `c` results in a ReferenceError because `const` variables are block-scoped and not accessible outside the block, and `b` results in a ReferenceError because `let` variables are block-scoped and not accessible outside the block.

## Example 2
```javascript
function test() {
    let a = "Hello";

    if (true) {
        let a = "Hi";
        console.log(a); // Output: Hi
    }

    console.log(a); // Output: Hello
}

test();
// Output:
// Hi
// Hello
```
**Explanation:** In this example, `a` is declared twice using `let` within different scopes. Inside the `if` block, a new variable `a` is declared, shadowing the outer variable `a` within that block. Therefore, the inner `a` holds the value `"Hi"` within the `if` block, while the outer `a` retains its value `"Hello"` outside the `if` block.

## Example 3
```javascript
function test() {
    let a = "Hello";

    if (true) {
        let a = "Hi";
        console.log(a); // Output: Hi
    }

    console.log(a); // Output: Hello
}

test(); // Output: Hi, Hello
```
**Explanation:** This example is similar to the previous one, but it emphasizes variable shadowing. The inner `a` shadows the outer `a` within the `if` block, meaning it has a separate scope and does not affect the outer `a`. Therefore, within the `if` block, `a` refers to the inner variable `"Hi"`, while outside the `if` block, `a` refers to the outer variable `"Hello"`.

## Example 4
```javascript
function test() {
    var a = "Hello";
    let b = "Bye";

    if (true) {
        let a = "Hi";
        var b = "Goodbye"; // Error: Illegal shadowing (let to var)
        console.log(a); // Output: Hi
        console.log(b); // Output: b has already been declared
    }
}

test(); // Output: b has already been declared
```
**Explanation:** In this example, `a` is declared using `var`, making it function-scoped, while `b` is declared using `let`, making it block-scoped. Inside the `if` block, a new variable `a` is declared using `let`, which shadows the outer `a` only within that block. However, when attempting to declare `b` using `var` within the same block, it results in an error because `b` has already been declared using `let` within the same block.


Certainly! Here's the continuation of the markdown file with examples demonstrating variable redeclaration:


## Example 5
```javascript
var x = 10;
var x = 20;
console.log(x); // Output: 20
```
**Explanation:** In this example, `x` is declared using `var` twice in the same scope. With `var`, variable redeclaration is allowed, and the second declaration overrides the first one. Therefore, `x` holds the value `20` after the redeclaration.

## Example 6
```javascript
let y = 10;
let y = 20; // SyntaxError: Identifier 'y' has already been declared
console.log(y);
```
**Explanation:** Unlike `var`, with `let` and `const`, variable redeclaration in the same scope is not allowed. Therefore, attempting to declare `y` again using `let` results in a SyntaxError because `y` has already been declared.

## Example 7
```javascript
const z = 10;
const z = 20; // SyntaxError: Identifier 'z' has already been declared
console.log(z);
```
**Explanation:** Similar to `let`, `const` also disallows variable redeclaration in the same scope. Therefore, attempting to redeclare `z` using `const` results in a SyntaxError because `z` has already been declared.



## Example 8
```javascript
var x;
console.log(x); // Output: undefined
```
**Explanation:** In this example, `x` is declared using `var` but not initialized. Variables declared with `var` are initialized with the value `undefined` by default until they are assigned a value. Therefore, `console.log(x)` outputs `undefined`.

## Example 9
```javascript
let y;
console.log(y); // Output: undefined
```
**Explanation:** Similar to `var`, variables declared with `let` are also initialized with the value `undefined` by default until they are assigned a value. Therefore, `console.log(y)` outputs `undefined`.

## Example 10
```javascript
const z;
console.log(z); // SyntaxError: Missing initializer in const declaration
```
**Explanation:** Unlike `var` and `let`, variables declared with `const` must be initialized at the time of declaration. Therefore, attempting to declare `z` with `const` without providing an initial value results in a SyntaxError.


Sure, here's an updated version of the example including `let` and `const` declarations:



## Example 11

```javascript
console.log(a); // Output: undefined
var a = 10;
```

**Explanation:** In this example, `a` is declared using `var` after it's been referenced in the `console.log` statement. Despite the declaration appearing after the usage, JavaScript hoists variable declarations to the top of their scope during the compilation phase. So, the code is interpreted by JavaScript as:

```javascript
var a;
console.log(a); // Output: undefined
a = 10;
```

Therefore, `a` is hoisted and initialized with the value `undefined` before the `console.log` statement is executed, resulting in the output of `undefined`. Later, `a` is assigned the value `10`.

## Example 12

```javascript
console.log(b); // ReferenceError: Cannot access 'b' before initialization
let b = 20;
```

**Explanation:** Unlike `var`, variables declared with `let` and `const` are not initialized until their declaration statement is reached during execution. Therefore, attempting to access `b` before it's declared results in a ReferenceError.

## Example 13

```javascript
console.log(c); // ReferenceError: Cannot access 'c' before initialization
const c = 30;
```

**Explanation:** Similar to `let`, variables declared with `const` are also not initialized until their declaration statement is reached during execution. Therefore, attempting to access `c` before it's declared results in a ReferenceError.

You're right. I apologize for the oversight. Let me correct that.

In the provided function `abc()`, when trying to access variable `b` before its initialization, a `ReferenceError` will occur because `let` and `const` variables are not initialized until their declaration statement is reached.
Sure, let's update the markdown with the corrected example and label it as Example 14:


## Example 14

```javascript
function abc() {
    console.log(a, b, c); // ReferenceError: Cannot access 'b' before initialization
    const c = 30;
    let b = 20;
    var a = 10;
}

abc();
```

**Explanation:**

1. The `console.log(a, b, c)` statement tries to access `a`, `b`, and `c`.
2. Both `let` and `const` declarations (`b` and `c`) are hoisted to the top of their block scope but are not initialized.
3. Since `b` is accessed before its initialization, a `ReferenceError` occurs.
4. `var` declaration (`a`) is also hoisted to the top of the function scope but is initialized with `undefined`.
5. `const c = 30;` initializes `c` with the value `30`.

Therefore, attempting to access `b` before its declaration results in a `ReferenceError`.


Certainly! Here's the updated markdown with the provided JavaScript code added as Example 15:


# JavaScript Scope and Nested Functions

## Example 15

```javascript
// The following variables are defined in the global scope
const num1 = 20;
const num2 = 3;
const name = "Chamakh";

// This function is defined in the global scope
function multiply() {
  return num1 * num2;
}

console.log(multiply()); // 60

// A nested function example
function getScore() {
  const num1 = 2;
  const num2 = 3;

  function add() {
    return `${name} scored ${num1 + num2}`;
  }

  return add();
}

console.log(getScore()); // "Chamakh scored 5"
```

**Explanation:**

1. Variables `num1`, `num2`, and `name` are declared in the global scope and have the values `20`, `3`, and `"Chamakh"`, respectively.

2. The function `multiply()` is defined in the global scope. It calculates and returns the product of `num1` and `num2`.

3. `console.log(multiply());` invokes the `multiply()` function, which calculates `num1 * num2`, resulting in `60`, and logs the result to the console.

4. The function `getScore()` is defined in the global scope. It declares its own `num1` and `num2` variables with values `2` and `3`, respectively.

5. Within `getScore()`, a nested function `add()` is defined. This function accesses variables `name`, `num1`, and `num2` from its lexical environment (the `getScore()` function scope). It returns a string with the concatenation of `name` and the sum of `num1` and `num2`.

6. `console.log(getScore());` invokes the `getScore()` function, which calls the `add()` function internally. The `add()` function returns `"Chamakh scored 5"`, which is then logged to the console.

This example demonstrates variable and function scoping in JavaScript, as well as the concept of lexical scope, where nested functions can access variables from their containing functions.


## Example 16: Function Hoisting

```javascript
// Calling the function before its declaration
console.log(add(5, 3)); // Output: 8

function add(a, b) {
  return a + b;
}
```

**Explanation:**

In JavaScript, function declarations are hoisted to the top of their containing scope during the compilation phase. This means that you can call a function before its actual declaration in the code, and it will still work as expected.

1. The `add` function is declared and defined below the `console.log` statement. Despite this, when the code is executed, the `add` function is hoisted to the top of its containing scope (in this case, the global scope).

2. When `console.log(add(5, 3));` is executed, the `add` function is already available due to hoisting. Therefore, the function is invoked with arguments `5` and `3`, which results in the sum `8` being logged to the console.

This example demonstrates how function declarations are hoisted in JavaScript, allowing you to use functions before their actual declarations in the code. However, it's important to note that this behavior applies specifically to function declarations (`function functionName() {}`), not to function expressions (`const functionName = function() {}`) or arrow functions (`const functionName = () => {}`), which behave differently with respect to hoisting.


## Example 17: Rest and Spread Operators

```javascript
// Rest parameter example
function sum(...args) { //rest
  return args.reduce((acc, val) => acc + val, 0);
}

console.log(sum(1, 2, 3, 4, 5)); // Output: 15

// Spread operator example
const numbers = [1, 2, 3, 4, 5];
const max = Math.max(...numbers); //spread

console.log(max); // Output: 5
```

**Explanation:**

1. **Rest Parameter (`...args`):** In the `sum` function, the rest parameter `...args` is used to collect any number of arguments passed to the function into an array. Inside the function body, the `reduce` method is applied to sum up all elements of the `args` array, starting from an initial value of `0`.

2. When `sum(1, 2, 3, 4, 5)` is called, all arguments passed to the function are collected into the `args` array. The `reduce` method then iterates over this array and computes the sum of its elements, resulting in `15`, which is logged to the console.

3. **Spread Operator (`...numbers`):** In the second part of the example, the spread operator `...numbers` is used to spread the elements of the `numbers` array as individual arguments to the `Math.max` function. This allows `Math.max` to determine the maximum value among the numbers in the array.

4. The `Math.max` function returns the largest of the provided numbers, which is `5` in this case, as it's the largest number in the `numbers` array.




```javascript
const fn = (a, ...num, x, y) => {
    console.log(x, y)
};
fn(5,6,3,7) // Error : Rest operator should be last

// corrected
const fn = (a,x,y, ...nums) => {
    console.log(x, y, nums)
};
fn(5,6,3,7, 8, 9) // 6 3 (3) [7, 8, 9] 
```


## Example 18: Regular Function vs. Arrow Function

```javascript
// Regular function
function regularFunction() {
  console.log("Regular Function");
  console.log("Arguments:", arguments);
  console.log("this:", this);
}

// Arrow function
const arrowFunction = () => {
  console.log("Arrow Function");
  console.log("Arguments:", arguments); // Error: arguments is not defined
  console.log("this:", this); // Output: the global object (e.g., window in the browser, or global in Node.js)
}

// Call regular function
regularFunction(1, 2, 3);

// Call arrow function
arrowFunction(1, 2, 3);
```

**Explanation:**

1. **Regular Function:**
   - The `regularFunction` is a traditional function declaration. When called, it logs "Regular Function" to the console.
   - The `arguments` object inside the function contains all arguments passed to it. It can be used to access all arguments, even those not explicitly declared in the function's parameter list.
   - The `this` keyword inside the function refers to the context in which the function is called. In this case, it will refer to the global object (`window` in a browser environment, or `global` in Node.js).

2. **Arrow Function:**
   - The `arrowFunction` is an arrow function declaration. When called, it logs "Arrow Function" to the console.
   - Arrow functions do not have their own `arguments` object. Attempting to access `arguments` inside an arrow function will result in a reference error (`arguments is not defined`).
   - The `this` keyword inside an arrow function retains the value of `this` from the enclosing lexical context. In most cases, this will be the value of `this` from the outer scope where the arrow function is defined. In this example, it refers to the global object.

When you run the code, you'll see the difference in behavior between regular functions and arrow functions, particularly with regards to the `arguments` object and the `this` keyword. Regular functions have their own `arguments` object, while arrow functions do not. Additionally, the value of `this` inside an arrow function is determined by the enclosing lexical scope, while for regular functions it depends on how the function is called.

## Example 19: `this` in Arrow Functions vs. Regular Functions

```javascript
let user = {
    username: "Roadside Coder",
    rc1: () => {
        console.log("Subscribe to " + this.username); // undefined
    },
    rc2() {
        console.log("Subscribe to " + this.username); // "Subscribe to Roadside Coder"
    }
};

user.rc1(); // Output: "Subscribe to undefined"
user.rc2(); // Output: "Subscribe to Roadside Coder"
```

**Explanation:**

1. **Arrow Function (`rc1`):**
   - `rc1` is defined as an arrow function. Arrow functions do not bind their own `this` value but inherit it from the enclosing lexical context (in this case, the global scope). Therefore, `this.username` inside `rc1` refers to `undefined`, as `this` in the global scope does not have a `username` property.

2. **Regular Function (`rc2`):**
   - `rc2` is defined as a regular function using the shorthand method syntax. Regular functions within objects are bound to the object itself when they are called as methods. Therefore, `this.username` inside `rc2` correctly refers to the `username` property of the `user` object.

When you call `user.rc1()`, it logs "Subscribe to undefined" because `this.username` in the arrow function `rc1` is `undefined`. On the other hand, calling `user.rc2()` logs "Subscribe to Roadside Coder" because `this.username` in the regular function `rc2` correctly refers to the `username` property of the `user` object.

This example illustrates the difference in behavior between arrow functions and regular functions with respect to the `this` keyword when used within object methods. Arrow functions do not bind their own `this` value, while regular functions do. Therefore, it's important to choose the appropriate function syntax based on the desired behavior regarding the `this` keyword.


# JavaScript Scope and Nested Functions

## Example 20: Lexical Scope

```javascript
function outerFunction() {
  let counter = 0;

  function innerFunction() {
    counter++;
    return counter;
  }

  return innerFunction;
}

const closureFunc1 = outerFunction();
const closureFunc2 = outerFunction();

console.log(closureFunc1()); // Output: ?
console.log(closureFunc1()); // Output: ?
console.log(closureFunc2()); // Output: ?
console.log(closureFunc2()); // Output: ?
```

**Explanation:**

1. **Outer Function (`outerFunction`):**
   - `outerFunction` defines a variable `counter` and declares an inner function `innerFunction`.
   - `innerFunction` increments `counter` by one each time it's called and returns the updated value.

2. **Lexical Scope:**
   - Each time `outerFunction` is called, it creates a new lexical scope for the returned `innerFunction`. Therefore, multiple instances of `innerFunction` maintain their own separate `counter` variables.

3. **Closure:**
   - When `closureFunc1` and `closureFunc2` are called, they capture and retain references to their respective `counter` variables from their enclosing lexical scopes.

**Interview Output-Based Question:**

**Question:** What will be the output of the following code snippet?

```javascript
console.log(closureFunc1()); // Output: ?
console.log(closureFunc1()); // Output: ?
console.log(closureFunc2()); // Output: ?
console.log(closureFunc2()); // Output: ?
```

**Answer Choices:**
a) `1`, `2`, `1`, `2`  
b) `1`, `1`, `2`, `2`  
c) `1`, `2`, `2`, `3`  
d) `1`, `1`, `1`, `1`

**Correct Answer:** c) `1`, `2`, `2`, `3`

**Explanation:** 
- The first call to `closureFunc1()` increments its own `counter` variable from `0` to `1`, and returns `1`. 
- The second call to `closureFunc1()` increments the same `counter` variable from `1` to `2`, and returns `2`.
- The first call to `closureFunc2()` operates on a separate `counter` variable (initialized to `0`), increments it from `0` to `1`, and returns `1`.
- The second call to `closureFunc2()` operates on the same `counter` variable as the previous call (which was incremented to `1`), increments it from `1` to `2`, and returns `2`.


## Example 21: Closure

```javascript
function createCounter() {
  let count = 0;

  return function() {
    count++;
    return count;
  };
}

const counter1 = createCounter();
const counter2 = createCounter();

console.log(counter1()); // Output: ?
console.log(counter1()); // Output: ?
console.log(counter2()); // Output: ?
console.log(counter2()); // Output: ?
```

**Explanation:**

1. **`createCounter` Function:**
   - `createCounter` is a higher-order function that returns an inner function.
   - The inner function maintains a private `count` variable using closure and increments it by one each time it's called.

2. **Closure:**
   - Each time `createCounter` is called, it creates a new lexical scope for the returned inner function. Consequently, each instance of the inner function maintains its own separate `count` variable, isolated from other instances.

**Interview Output-Based Question:**

**Question:** What will be the output of the following code snippet?

```javascript
console.log(counter1()); // Output: ?
console.log(counter1()); // Output: ?
console.log(counter2()); // Output: ?
console.log(counter2()); // Output: ?
```

**Answer Choices:**
a) `1`, `2`, `1`, `2`  
b) `1`, `1`, `1`, `1`  
c) `1`, `2`, `2`, `3`  
d) `2`, `3`, `1`, `2`

**Correct Answer:** c) `1`, `2`, `2`, `3`

**Explanation:** 
- The first call to `counter1()` increments its own `count` variable from `0` to `1`, and returns `1`. 
- The second call to `counter1()` increments the same `count` variable from `1` to `2`, and returns `2`.
- The first call to `counter2()` operates on a separate `count` variable (initialized to `0`), increments it from `0` to `1`, and returns `1`.
- The second call to `counter2()` operates on the same `count` variable as the previous call (which was incremented to `1`), increments it from `1` to `2`, and returns `2`.


## Example 22: Closure Scope Chaining

```javascript
var username = "Piyush";

function makeFunc() {
  var name = "Mozilla";

  function displayName(num) {
    console.log(name, num, username);
  }

  return displayName;
}

makeFunc()(5);
```

**Explanation:**

1. **Variable Declarations:**
   - `username` is declared in the global scope with the value `"Piyush"`.
   - `makeFunc` function is defined, which contains another function `displayName`.
   - Inside `makeFunc`, `name` is declared with the value `"Mozilla"`.

2. **Closure Scope Chaining:**
   - `displayName` function has access to its enclosing scope, including the variables `name` and `username`, due to closure.
   - When `makeFunc()` is called, it returns the `displayName` function.

**Interview Output-Based Question:**

**Question:** What will be logged to the console when `makeFunc()(5)` is executed?

**Answer Choices:**
a) `"Mozilla" 5 "Piyush"`  
b) `"Mozilla" undefined "Piyush"`  
c) `"Mozilla" 5 undefined`  
d) `"Piyush" 5 "Piyush"`

**Correct Answer:** a) `"Mozilla" 5 "Piyush"`

**Explanation:** 
- `makeFunc()` is called, returning the `displayName` function.
- When `displayName` is invoked with `5`, it logs `"Mozilla"` (captured from the lexical scope of `makeFunc`), `5`, and the global variable `username` with the value `"Piyush"`.



## Example 23: Nested Function with Closure

```javascript
// global scope
var e = 10;

function sum(a) {
  return function(b) {
    return function(c) {
      // outer functions scope
      return function(d) {
        // local scope
        return a + b + c + d + e;
      };
    };
  };
}

console.log(sum(1)(2)(3)(4)); // log 20
```

**Explanation:**

1. **Variable Declarations:**
   - `e` is declared in the global scope with the value `10`.

2. **Function Definitions:**
   - `sum` function takes `a` as its parameter and returns a function.
   - The returned function also takes `b` as its parameter and returns another function.
   - This nesting continues until the fourth returned function takes `d` as its parameter and returns the sum of all parameters plus the global variable `e`.

**Interview Output-Based Question:**

**Question:** What will be logged to the console when `sum(1)(2)(3)(4)` is executed?

**Answer Choices:**
a) `20`  
b) `40`  
c) `30`  
d) `10`

**Correct Answer:** a) `20`

**Explanation:** 
- The `sum` function is called sequentially with arguments `1`, `2`, `3`, and `4`.
- Each nested function adds its argument to the previous accumulated value (`a + b + c + d`), resulting in `1 + 2 + 3 + 4 = 10`.
- Additionally, the global variable `e` with the value `10` is also added to the sum, resulting in `10 + 10 = 20`.

<br>

- `learn more:` https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures



## Example 24: Shadowing in IIFE

```javascript
let count = 0;

(function printCount() {
  if (count == 0) {
    let count = 1; // Shadowing
    console.log(count); // 1
  }
  // count is 0 from global
  console.log(count);
})();
```

**Explanation:**

1. **Variable Declarations:**
   - `count` is declared in the global scope with the initial value `0`.

2. **IIFE (Immediately Invoked Function Expression):**
   - An IIFE is used to encapsulate the code.
   - Inside the IIFE, another variable `count` is declared using `let` keyword, which shadows the global variable `count`.

**Interview Output-Based Question:**

**Question:** What will be logged to the console when the code is executed?

**Answer Choices:**
a) `1`, `1`  
b) `1`, `0`  
c) `0`, `0`  
d) `0`, `1`

**Correct Answer:** b) `1`, `0`

**Explanation:** 
- Inside the IIFE, a local variable `count` is declared and initialized to `1`.
- This local `count` variable is used within the if statement, so `1` is logged to the console.
- Outside the if statement, the global `count` variable with the value `0` is logged to the console.





## Example 25: form closure

```javascript
//create a fnc

// Usage example:
var addSix = createBase(6);
console.log(addSix(10)); // returns 16
console.log(addSix(21)); // returns 27
```


**Answer**
```javascript
function createBase(base) {
  // Return a function that adds the given argument to the base value
  return function(additionalValue) {
    return base + additionalValue;
  };
}

// Usage example:
var addSix = createBase(6);
console.log(addSix(10)); // returns 16
console.log(addSix(21)); // returns 27
```

Explanation:

1. The `createBase` function takes a `base` value as a parameter and returns another function.
2. The returned function captures the `base` value in its closure and adds the `additionalValue` parameter to it.
3. When `addSix` is invoked with different arguments, it adds those arguments to the base value of `6`, returning the sum.

Sure, here's the full code example with optimization explained in Markdown format:


## Example 26: Closure Time Optimization

```javascript
function find(index) {
    let a = [];
    for (let i = 0; i < 1000000; i++) {
        a[i] = i * 1;
    }
    console.log(a[index]);
}

console.time("6");
find(6);
console.timeEnd("6");

console.time("12");
find(50);
console.timeEnd("12");
```

**Output:**
```
6
6: 17.741943359375 ms
50
12: 16.117919921875 ms
```

**Optimized Version:**

```javascript
function find() {
    let a = [];
    for (let i = 0; i < 1000000; i++) {
        a[i] = i * 1;
    }
    // Return a function that accesses the precomputed value directly
    return function(index) {
        console.log(a[index]);
    };
}

// Usage example:
const findValue = find();

console.time("6");
findValue(6);
console.timeEnd("6");

console.time("12");
findValue(50);
console.timeEnd("12");

//output
// 6
// 6 : 0.139892578125 ms
// 50
// 2: 0.02099609375 ms
```

**Explanation:**

**Issue:**
- In the original code, the `find` function recalculates the array values every time it is called with a different index.
- This approach leads to unnecessary computation overhead, especially for large arrays.

**Solution:**
- To optimize the code, we precompute the array values outside the `find` function.
- We create a closure by returning a function from the `find` function, which encapsulates the precomputed array.
- This closure allows us to directly access the precomputed array values without the need for recalculation.
- By using closures and precomputing the array values, we eliminate the need for redundant computations and improve the efficiency of the code.


## Example 27: Logging with setTimeout

```javascript
for (var i = 0; i < 3; i++) {
    setTimeout(function log() {
        console.log(i); // What is logged?
    }, 1000);
}
```

**Output:**
After 1 second (due to the timeout), the value of `i` is logged three times consecutively, each time printing `3`.

**Explanation:**
- In the loop, `setTimeout` is called three times, but it doesn't execute immediately.
- After the loop finishes, `i` has the final value of `3`.
- When the timeout expires (after 1 second in this case), the callback function inside `setTimeout` is executed.
- However, by the time the callback function is executed, the loop has already finished executing, and `i` has the final value of `3`.
- So, when `console.log(i)` is called inside the callback function, it prints the value of `i` at that moment, which is `3`.

**Optimized Solution:**
To log the correct value of `i` for each iteration, we can use block-scoped variables with `let`:

```javascript
for (let i = 0; i < 3; i++) {
    setTimeout(function log() {
        console.log(i); // Logs 0, 1, 2 respectively
    }, 1000);
}
```

**Explanation:**
- By using `let` instead of `var`, `i` is block-scoped, which means each iteration of the loop will have its own separate `i`.
- Therefore, when the callback function inside `setTimeout` is executed, it will capture the value of `i` for the corresponding iteration, resulting in the expected behavior of logging `0`, `1`, and `2` respectively after 1 second for each iteration.

```javascript
function a() {
    for (var i = 0; i < 3; i++) {
        setTimeout(function log() {
           console.log(i); // What is logged?
        }, i * 1000);
    }
}

a();
``` 
- not allowed to change var to let, achieve 0, 1, 2

```javascript
function a() {
    for (var i=0; i < 3; i++) {
        function inner(i) {
            setTimeout(function log() {
            console.log(i); // What is logged?
            }, i* 1000);
        }
        inner(i);
    }
}
a();

//OR

function a() {
    for (var i = 0; i < 3; i++) {
        setTimeout((function (index) {
            return function () {
                console.log(index); // Each log has its own scope for 'index'
            };
        })(i), i * 1000);
    }
}

a();


```

## Example 28: Closure Private Counter

```javascript
function counter() {
    var _counter = 0;
    function add(increment) {
        _counter += increment;
    }
    function retrieve() {
        return "Counter = " + _counter;
    }
    return {
        add,
        retrieve,
    };
}

const count = counter();
count.add(5);
count.add(10);
console.log(count.retrieve()); // Output: Counter = 15
```

**Explanation:**
- The `counter` function defines a private variable `_counter` initialized to `0` and two inner functions `add` and `retrieve`.
- The `add` function takes an `increment` parameter and increments the `_counter` variable by the given `increment`.
- The `retrieve` function returns a string representation of the current counter value.
- Inside the `counter` function, an object with references to the `add` and `retrieve` functions is returned, creating a closure that retains access to the `_counter` variable even after the `counter` function has finished executing.
- When `count.add(5)` is called, the `_counter` variable is incremented by `5`.
- Similarly, when `count.add(10)` is called, the `_counter` variable is further incremented by `10`.
- Finally, `count.retrieve()` retrieves the current value of `_counter`, which is `15`, and logs it to the console.

This example demonstrates how closures can be used to create private variables in JavaScript, allowing for encapsulation and information hiding within functions. The returned object provides a controlled interface to manipulate and retrieve the private variable's value.




## Example 29: Module Pattern
In the module pattern, JavaScript developers use closures to create private variables and functions, encapsulating them within a single object. This approach allows for better organization of code and prevents polluting the global namespace. Let's create an example demonstrating the module pattern:

```javascript
const Calculator = (function() {
    // Private variables
    let result = 0;

    // Private functions
    function add(a, b) {
        return a + b;
    }

    function subtract(a, b) {
        return a - b;
    }

    // Public interface
    return {
        // Public methods
        add: function(a, b) {
            result = add(a, b);
            return result;
        },
        subtract: function(a, b) {
            result = subtract(a, b);
            return result;
        },
        getResult: function() {
            return result;
        }
    };
})();

// Usage example:
Calculator.add(5, 3); // Returns 8
Calculator.subtract(10, 2); // Returns 8
console.log(Calculator.getResult()); // Output: 8
```

**Explanation:**
- In this example, we create a module named `Calculator` using an IIFE (Immediately Invoked Function Expression).
- Inside the IIFE, we define private variables (`result`) and functions (`add` and `subtract`).
- The private variables and functions are accessible only within the scope of the IIFE due to closures.
- We return an object containing public methods (`add`, `subtract`, and `getResult`), which have access to the private variables and functions.
- Users can interact with the `Calculator` module using its public methods, but they cannot directly access or modify its private members.

This example demonstrates how to create a module with private members using the module pattern in JavaScript. It helps organize code and prevents unintended modifications to internal state by encapsulating functionality within a self-contained unit.

## Example 30: Run Once

```javascript
let name;
function greet() {
    name = "Manish";
    console.log("Hello", name);
}
    greet(); //Hello Manish 
    greet(); //Hello Manish
    greet(); //Hello Manish
    greet(); //Hello Manish
    greet(); //Hello Manish
    greet(); //Hello Manish
```

### Method 1: Using Closure

```javascript
let name;

function greet() {
    let called = 0;
    return function() {
        if (called > 0) {
            console.log("Already Called");
        } else {
            name = "Manish";
            console.log("Hello", name);
            called++;
        }
    };
}

let g = greet();
g(); // Hello Manish
g(); // Already Called
g(); // Already Called
g(); // Already Called
g(); // Already Called
```

**Explanation:**
- In this method, we define a `greet` function that returns another function using a closure.
- The inner function keeps track of the number of times it has been called using the `called` variable.
- If `called` is greater than 0, it means the function has already been called, so it logs "Already Called". Otherwise, it sets the `name` variable and logs "Hello" followed by the name.
- This approach ensures that the function runs only once by using a closure to maintain the state.

### Method 2: Using a Custom Once Function

```javascript
function once(func, context) {
    let ran;
    return function() {
        if (func) {
            ran = func.apply(context || this, arguments);
            func = null;
        }
        return ran;
    };
}

const hello = once(() => console.log("hello"));
hello(); // hello
hello(); // (no output)
hello(); // (no output)
```

**Explanation:**
- Here, we define a `once` function that takes another function `func` as input and returns a new function.
- The returned function can only be called once. After the first call, subsequent calls to the function have no effect.
- Inside the returned function, we use a closure to capture the `ran` variable, which keeps track of whether the function has been called before.
- If `func` exists (meaning it has not been called yet), we call it and store the result in `ran`. We then set `func` to `null` to ensure it cannot be called again.
- This approach provides a reusable way to create functions that run only once.

### Method 3: Using lodash's `once` Function

```javascript
const _ = require('lodash');

let name;
const greet = _.once(function() {
    name = "Manish";
    console.log("Hello", name);
});

greet(); // Hello Manish
greet(); // (no output)
```

**Explanation:**
- Lodash provides a utility function called `once`, which creates a version of a function that can only be called once.
- In this method, we use `_.once` to create a `greet` function that runs only once.
- The first call to `greet` sets the `name` variable and logs "Hello" followed by the name.
- Subsequent calls to `greet` have no effect and produce no output.
- Lodash's `once` function provides a convenient way to ensure that a function runs only once, without having to manually manage state or write custom logic.



## Example 31: Implement memoized fn

```javascript  
const clumsysquare = (num1, num2) => {
    for (let i = 1; i <= 100000000; i++) { }
    return num1 * num2;
};
console.time("First call");
console.log(clumsysquare(9467, 7649));
console.timeEnd("First call");
console.time("Second call");
console.log(clumsysquare(9467, 7649));
console.timeEnd("Second call");


// output
// 72413083
// First call: 67.257080078125 ms
// 72413083
// Second call: 60.3701171875 ms

```


```javascript
const memoizedSquare = (function() {
    const cache = {};
    return function(num1, num2) {
        const key = `${num1}_${num2}`;
        if (cache[key] === undefined) {
            for (let i = 1; i <= 100000000; i++) { } // Simulating heavy computation
            cache[key] = num1 * num2;
        }
        return cache[key];
    };
})();

console.time("First call");
console.log(memoizedSquare(9467, 7649));
console.timeEnd("First call");
console.time("Second call");
console.log(memoizedSquare(9467, 7649));
console.timeEnd("Second call");

// 72413083
// First call: 61.737060546875 ms
// 72413083
// Second call: 0.02685546875 ms
```

**Explanation:**
- In this method, we implement memoization using a closure. 
- We define a function `memoizedSquare` that returns another function using a closure.
- Inside the closure, we maintain a `cache` object to store previously computed results.
- When `memoizedSquare` is called with arguments `num1` and `num2`, we generate a unique key based on the arguments.
- If the result for the given key is not present in the cache, we compute it and store it in the cache.
- Subsequent calls to `memoizedSquare` with the same arguments will return the result from the cache without re-computation.
- This approach significantly reduces the execution time for repeated calls with the same arguments, as the heavy computation is performed only once and the result is cached for reuse.



```javascript
// Example 28: Currying -  Higher-Order Function for Arithmetic Operations
// evaluate("sum") (4) (2) => 6
// evaluate("multiply")(4)(2) => 8
// evaluate("divide") (4) (2) => 2
// evaluate("substract") (4) (2) => 2

// Define the evaluate function
function evaluate(operation) {
    // Define the inner function based on the provided operation
    let func;
    switch (operation) {
        case "sum":
            func = (a, b) => a + b;
            break;
        case "multiply":
            func = (a, b) => a * b;
            break;
        case "divide":
            func = (a, b) => a / b;
            break;
        case "subtract":
            func = (a, b) => a - b;
            break;
        default:
            throw new Error("Invalid operation");
    }
    
    // Return the function that performs the specified operation
    return function(a) {
        return function(b) {
            return func(a, b);
        };
    };
}

// Test cases
console.log(evaluate("sum")(4)(2));        // Output: 6
console.log(evaluate("multiply")(4)(2));   // Output: 8
console.log(evaluate("divide")(4)(2));     // Output: 2
console.log(evaluate("subtract")(4)(2));   // Output: 2
```

**Explanation:**
- The `evaluate` function takes a string `operation` as input and returns a function.
- Inside `evaluate`, a switch statement is used to determine the appropriate function (`func`) based on the provided `operation`.
- The returned function accepts two arguments `a` and `b`, representing the operands.
- Depending on the `operation`, the function `func` performs the specified operation on `a` and `b`.
- The returned function evaluates the operation on the provided operands and returns the result.



## Example 32: Infinite Currying

```javascript
// Original function to demonstrate infinite currying
function add(a) {
    return function(b) {
        if (b) return add(a + b);
        return a;
    };
}

// Test case: Sum of multiple numbers using infinite currying
console.log(add(5)(2)(4)(8)()); // Output: 19
```

**Explanation:**
- The `add` function takes a number `a` as input and returns a new function.
- This returned function also takes a number `b` as input.
- If `b` is provided, it adds `a` and `b`, then returns a new function that continues the process of adding more numbers.
- If `b` is not provided (or falsy), it returns the accumulated sum.
- This allows for infinite currying, where you can call the `add` function with any number of arguments, and it will keep currying until no more arguments are provided, at which point it returns the sum of all accumulated numbers.

---

## Example 33: Infinite Currying

```javascript
// Define a currying function
function curry(fn) {
    return function curried(...args) {
        if (args.length >= fn.length) {
            return fn(...args);
        } else {
            return function(...nextArgs) {
                return curried(...args.concat(nextArgs));
            };
        }
    };
}

// Test case: Sum of multiple numbers using infinite currying
const sum = curry((...args) => args.reduce((acc, curr) => acc + curr, 0));

console.log(sum(1)(2)(3)(4)(5)); // Output: 15
console.log(sum(1)(2, 3)(4, 5)); // Output: 15
console.log(sum(1, 2)(3, 4)(5)); // Output: 15
```

**Explanation:**
- The `curry` function takes a function `fn` as input and returns a new function `curried`.
- The `curried` function collects arguments until it has received the same number of arguments as the original function `fn`.
- Once the required number of arguments is collected, it applies the original function `fn` with those arguments.
- If the collected arguments are less than the required number, it returns a new function that continues to collect additional arguments until the required number is reached.
- This process allows for infinite currying, where you can call the curried function with any number of arguments, and it will keep currying until all arguments are collected before invoking the original function.



## Example 34: Partial Application

```javascript
// Original function to demonstrate partial application
function sum(a) {
    return function(b, c) {
        return a + b + c;
    };
}

// Test case: Partial application of the sum function
const x = sum(10);
console.log(x(5, 6)); // Output: 21
console.log(x(3, 2)); // Output: 15

// Alternatively
console.log(sum(20)(1, 4)); // Output: 25
```

**Explanation:**
- The `sum` function takes a single argument `a` and returns a new function.
- This returned function takes two arguments `b` and `c` and calculates the sum of `a`, `b`, and `c`.
- Partial application is demonstrated by calling the `sum` function with only the first argument (`a`), creating a new function `x` with `a` pre-filled.
- The new function `x` can then be called with the remaining arguments (`b` and `c`) to calculate the sum.
- Alternatively, partial application can be achieved directly by chaining function calls, as shown in the last example.


```javascript
// Example 31: Partial Application

// Original function to demonstrate partial application
function greet(greeting, name) {
    return `${greeting}, ${name}!`;
}

// Partial application function
function partial(fn, ...args) {
    return function(...remainingArgs) {
        return fn(...args, ...remainingArgs);
    };
}

// Test case: Partial application of the greet function
const sayHello = partial(greet, "Hello");
console.log(sayHello("John")); // Output: "Hello, John!"

const sayHi = partial(greet, "Hi");
console.log(sayHi("Alice")); // Output: "Hi, Alice!"
```

**Explanation:**
- The `greet` function takes two arguments: `greeting` and `name`, and returns a formatted greeting message.
- The `partial` function takes a function `fn` and a list of arguments `...args`.
- It returns a new function that, when called with additional arguments (`...remainingArgs`), applies both the original arguments and the additional arguments to the original function `fn`.
- This allows for partial application, where you can pre-fill some arguments of a function to create a new function with fewer parameters.
- In the example, `partial` is used to create new functions `sayHello` and `sayHi` that partially apply the `greet` function with the greeting `"Hello"` and `"Hi"`, respectively.
- When these new functions are called with a single argument (the `name`), they produce the desired greeting message with the predefined greeting.


## Example 35: Currying

<!-- Converts f(a, b, c) into f(a)(b)(c) -->

```javascript

// Original function to demonstrate currying
function sum(a, b, c) {
    return a + b + c;
}

// Currying function
function curry(fn) {
    return function curried(...args) {
        if (args.length >= fn.length) {
            return fn(...args);
        } else {
            return function(...nextArgs) {
                return curried(...args.concat(nextArgs));
            };
        }
    };
}

// Test case: Currying the sum function
const curriedSum = curry(sum);
console.log(curriedSum(1)(2)(3)); // Output: 6
```

**Explanation:**
- The `sum` function takes three arguments `a`, `b`, and `c`, and returns their sum.
- The `curry` function is used to convert the `sum` function into a curried function.
- When called with fewer arguments than expected, the curried function returns a new function that takes the remaining arguments.
- This allows for partial application and chaining of function calls, resulting in a more flexible and expressive way of invoking the original function.

<hr>
<hr>
<hr>
<hr>

---






# JavaScript IIFE Interview Questions and Answers

## Question 1
What will be the output of the following IIFE?
```javascript
(function() {
    var x = 10;
    console.log(x);
})();
```
**Answer:** The output will be `10`. Explanation: Inside the IIFE, `x` is declared and initialized with the value `10`. Then, `x` is logged to the console.

## Question 2
Explain the output of the following code snippet:
```javascript
var result = (function() {
    return 2 + 2;
})();
console.log(result);
```
**Answer:** The output will be `4`. Explanation: The IIFE returns the result of `2 + 2`, which is `4`. This value is assigned to `result`, which is then logged to the console.

## Question 3
Predict the output of the following IIFE:
```javascript
var a = 5;
(function() {
    console.log(a);
})();
```
**Answer:** The output will be `5`. Explanation: Inside the IIFE, `a` is accessed from the outer scope, and its value is `5`, so `5` is logged to the console.

## Question 4
What will be logged to the console in this code?
```javascript
(function() {
    var name = 'John';
    console.log('Hello, ' + name + '!');
})();
```
**Answer:** The output will be `Hello, John!`. Explanation: Inside the IIFE, the variable `name` is declared and initialized with the value `'John'`. Then, a greeting message is logged to the console using the value of `name`.

## Question 5
Explain the output of this code:
```javascript
var count = 0;
(function() {
    count++;
    console.log(count);
})();
```
**Answer:** The output will be `1`. Explanation: The variable `count` is initialized to `0`, then it's incremented inside the IIFE, resulting in `1`, which is then logged to the console.

## Question 6
What will be the output of this IIFE?
```javascript
(function(x) {
    console.log(x * x);
})(5);
```
**Answer:** The output will be `25`. Explanation: The IIFE takes an argument `x` and logs the square of `x`, which is `25`.

## Question 7
Predict the output of the following code snippet:
```javascript
var greeting = (function() {
    return 'Hello';
})();
console.log(greeting + ', World!');
```
**Answer:** The output will be `Hello, World!`. Explanation: The IIFE returns the string `'Hello'`, which is assigned to `greeting`. Then, the value of `greeting` is concatenated with `', World!'` and logged to the console.

## Question 8
Explain the output of this IIFE:
```javascript
(function() {
    var a = b = 5;
})();
console.log(b);
```
**Answer:** The output will be `5`. 
Explanation: Inside the IIFE, `b` is assigned the value `5`, 
making it a global variable. 
Therefore, `b` is accessible outside the IIFE and 
logs `5` to the console.

In JavaScript, when you write var a = b = 5;, b indeed becomes a global variable if it wasn't previously defined. However, the var keyword does not get prefixed to b.

Let's break down what happens:

b = 5;: If b hasn't been previously declared using var, let, or const, it becomes a global variable. The var keyword is not used here, so b is assigned the value 5 in the global scope.

var a = b;: This line declares a variable a using the var keyword and assigns it the value of b. Since b has been assigned the value 5 in the global scope, a will also have the value 5.

So, to clarify, the var keyword does not prefix b in this context. Instead, b becomes a global variable due to the absence of any variable declaration keyword (var, let, const). This behavior is often considered a side effect and can lead to unexpected behavior and bugs if not used carefully. It's generally recommended to avoid relying on such implicit global variable declarations for clarity and maintainability of code. Explicitly declaring variables using var, let, or const is a better practice. 

## Question 9
What will be logged to the console in this code?
```javascript
var num = 10;
(function() {
    console.log(num);
    var num = 20;
})();
```
**Answer:** The output will be `undefined`. Explanation: Inside the IIFE, `num` is declared with `var`, causing it to be hoisted to the top of the function and initialized with `undefined` before the `console.log` statement.

## Question 10
Predict the output of the following IIFE:
```javascript
(function() {
    var x = 'inside';
})();
console.log(x);
```
**Answer:** The output will be a ReferenceError: `x is not defined`. Explanation: `x` is declared inside the IIFE, making it inaccessible outside the IIFE. Therefore, a ReferenceError occurs when trying to log `x` outside its scope.


Your question and answer are close, but there's a small mistake in the explanation of the first answer. Let me correct and improve the formatting for clarity:

## Question 11

### Code Snippet 1
```javascript
for (var i = 1; i <= 5; i++) {
    setTimeout(function() {
        console.log(i);
    }, i * 1000);
}
```
**Answer:** 
```
6
6
6
6
6
```
**Explanation:** 
In this code snippet, the loop iterates from `1` to `5`, and for each iteration, a `setTimeout` function is called. However, since `var` is used to declare `i`, it is function-scoped rather than block-scoped. By the time the `setTimeout` callback functions are executed, the loop has already finished executing, and the value of `i` is `6` in all callback functions. Hence, `6` is logged to the console five times.

### Code Snippet 2
```javascript
for (let i = 1; i <= 5; i++) {
    (function(i) {
        setTimeout(function() {
            console.log(i);
        }, i * 1000);
    })(i);
}
```
**Answer:** 
```
1
2
3
4
5
```
**Explanation:** 
In this code snippet, `let` is used to declare `i`, making it block-scoped. Therefore, each iteration of the loop creates a new lexical environment for `i`. Inside the immediately invoked function expression (IIFE), `i` is passed as an argument, creating a new closure for each iteration. As a result, when the `setTimeout` callback functions are executed, they capture the correct value of `i` for each iteration, resulting in logging `1`, `2`, `3`, `4`, and `5` to the console at intervals of one second each.


