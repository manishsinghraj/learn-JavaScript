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