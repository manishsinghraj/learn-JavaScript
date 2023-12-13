```js
//var let const

// let,cont was introduced in es6 2015

//var -> function
//let -> block
//const -> block

//Objects
const person = {
  name: 'Manish',
  walk: function () { }
};

//if we have function inside of an object we called it as method.

//in ES6the new way of adding method.

const person1 = {
  name: 'Manish',
  walk() { },
  talk() { }
};

//two ways to access this fn,
person1.talk();
person1['name'] = "john";


//This keyword
const person2 = {
  name: 'Manish',
  walk() { console.log(this) },
  talk() { }
};
//This returns the reference to the current object

person2.walk(); // this will return the person2 Object

//Window

const walk = person2.walk;
walk(); //Standalone fn, outside of an object

// will return undefined if strict-mode is enabled,this is refering in global context that is window object.
//What is window?



//How to fix this problem - if i call walk(); it should give reference to the person object.

//In Js fn are Objects

//To ensure that walk() refers to the person2 object even when called as a standalone function, you can bind the method to the person2 object explicitly. You can use the bind() method to achieve this. Here's how you can fix the problem:
const person3 = {
  name: 'Manish',
  walk2() { console.log(this) },
  talk() { }
};

const walk2 = person3.walk2.bind(person3); // Bind the method to the person2 object
walk2(); // Now this will correctly reference the person2 object
//When you assign an object, function, or array to a variable or pass it as an argument, you're actually working with a reference to the underlying object in memory. Changes made through one reference will affect the underlying object and are visible through other references to the same object. This behavior is often referred to as "pass by reference" or "pass by sharing."

// The this keyword in JavaScript is a special keyword that refers to the current execution context.Its value depends on how and where it's used within your code. The behavior of this can be a source of confusion for many JavaScript developers because it can change its value depending on various factors. Here are some common scenarios where the this keyword is used and examples for each:

// Global Context:

// In the global context(outside of any function or object), this refers to the global object, which is window in a web browser and global in Node.js.

//   javascript
// Copy code
// console.log(this === window); // true (in a web browser)


// Function Context:

// Inside a function, the value of this depends on how the function is called.

// Regular Function Calls: In a regular function call, this typically refers to the global object.

//   javascript
// Copy code
// function myFunction() {
//   console.log(this === window); // true (in a web browser)
// }

// myFunction();
// Methods: When a function is called as a method of an object, this refers to the object that the method is called on.

//   javascript
// Copy code
// const person = {
//   name: "John",
//   sayHello: function () {
//     console.log("Hello, " + this.name);
//   },
// };

// person.sayHello(); // "Hello, John"
// Constructor Functions: When a function is used as a constructor with the new keyword, this refers to the newly created instance.

//   javascript
// Copy code
// function Dog(name) {
//   this.name = name;
// }

// const myDog = new Dog("Buddy");
// console.log(myDog.name); // "Buddy"
// Event Handlers:

// Inside event handlers, this often refers to the DOM element that triggered the event.

//   javascript
// Copy code
// const button = document.querySelector("button");
// button.addEventListener("click", function () {
//   console.log(this === button); // true
// });
// Arrow Functions:

// Arrow functions have a different behavior with this.They inherit the value of this from their enclosing(parent) function.

// javascript
// Copy code
// const person = {
//   name: "Alice",
//   sayHello: () => {
//     console.log("Hello, " + this.name); // "Hello, undefined"
//   },
// };

// person.sayHello();
// In this example, the arrow function sayHello inherits this from its enclosing context, which is the global context.Therefore, this.name is undefined.


// To understand the behavior of references, variables, and memory in JavaScript, you should be familiar with several key topics and concepts:

// Data Types: Understand the distinction between primitive data types(e.g., numbers, strings, booleans) and reference data types(e.g., objects, arrays, functions).

// Variables and Declarations: Learn how to declare variables using var, let, and const, and understand their scope and behavior.

//   Objects: Gain a solid understanding of objects in JavaScript, including how to create, modify, and access properties.

// References vs.Values: Learn the difference between passing by reference(reference types) and passing by value(primitive types) when working with variables and function arguments.

// Memory and Reference: Understand how memory is allocated and how variables, especially reference types, store references to objects in memory.

//   Mutability: Learn about mutable and immutable data types, particularly how objects can be modified in place.

// Passing by Reference and Copy: Understand how references work when objects are assigned to variables, passed as function arguments, or compared.

// Object Mutability: Learn how to avoid unintentional modification of objects and handle object immutability.

// Equality and Comparison: Understand how == (loose equality) and === (strict equality) operators work, especially when comparing objects and references.

// Garbage Collection: Get an overview of how JavaScript's garbage collection process works and how it manages memory.

// Scope and Closure: Familiarize yourself with the concepts of lexical scope and closure, as they play a role in variable references.

//   Debugging: Learn how to use debugging tools like the browser's developer console and debugger to inspect and trace variable values and references.

// Practice: Apply these concepts in practical coding exercises to reinforce your understanding.

// By mastering these topics, you'll have a solid foundation for understanding how references, variables, and memory management work in JavaScript, which will be invaluable when working with more complex code and applications.


//Difference between parameter and argument


//Arrow function use

const jobs = [
  { id: 1, isActive: true },
  { id: 1, isActive: true },
  { id: 1, isActive: false },
];

// const activeJobs = jobs.filter(function (job) { return job.isActive});
const activeJobs = jobs.filter((job) => job.isActive);

console.log(activeJobs); //[ { id: 1, isActive: true }, { id: 1, isActive: true } ]

//Learn filter map reduce etc


//Arrow fn and this
//Arrow fn dont rebind this keyword

const dog = {
  talk() {
    console.log('this', this);
  }
}

dog.talk(); //Returns reference to the dog object

const dog2 = {
  talk() {
    setTimeout(function () {
      console.log('this', this);
    }, 1000)
  }
}

dog2.talk(); //Returns reference window object, because the callback fun in setTimeInterval is not part of any object 
// it is standalone fn 

// How to solve this?

const dog3 = {
  talk() {
    const self = this; // Store a reference to 'this' in a variable
    setTimeout(function () {
      console.log('this', self); // 'self' refers to the dog2 object
    }, 1000);
  }
}

dog3.talk(); // 'this' refers to the dog3 object


//OR

const dog4 = {
  talk() {
    setTimeout(function () {
      console.log('this', this);
    }.bind(this), 1000);
  }
}

dog4.talk(); // 'this' refers to the dog4 object



//We dont need to do the above sol if using arrow fn
//Arrow fn dont Rebind this
// if you change to arrow fn it will inherit this keyword
const dog5 = {
  talk() {
    setTimeout(() => {
      console.log('this', this);
    }, 1000);
  }
}

dog5.talk(); // 'this' refers to the dog5 object


//Array.Map()
// changes the item of array,and creates a new array

// const color = ['red', 'green', 'blue'];
// const newColor = color.map(function (item) {
//   return '<li>' + item + '</li>';
// });

const color = ['red', 'green', 'blue'];
const newColor = color.map((item) => `<li>${item}</li>`);

console.log(color);
console.log(newColor);


//Object Destructuring
const address = {
  street: '123 Main St',
  city: 'New York',
  country: 'USA'
};

const { street, city, country } = address;
console.log(street);  // '123 Main St'
console.log(city);    // 'New York'
console.log(country); // 'USA'

const { street } = address;
console.log(street);  // '123 Main St'

const { street: st } = address;
console.log(st);      // '123 Main St'



// OR  
// using rest operators 
const person0 = {
  firstName: 'John',
  lastName: 'Doe',
  age: 30,
  city: 'New York',
  country: 'USA',
};

const { firstName, lastName, ...rest } = person0;

console.log(firstName); // 'John'
console.log(lastName);  // 'Doe'
console.log(rest);      // { age: 30, city: 'New York', country: 'USA' }
// The third const { street: st } = address; statement renames the extracted street property to st, and the value of st is logged to the console.

// const numbers = [1, 2, 3, 4, 5];
// const [first, second, ...rest] = numbers;

// const third = rest[0];
// console.log(third); // Outputs: 3


//Class

class Person {
  constructor(name) {
    this.name = name;
  }
  walk() {
    console.log("walk");
  }
}

const person9 = new Person('Manish');


//Inheritence

class Person {
  constructor(name) {
    this.name = name;
  }
  walk() {
    console.log("walk");
  }
}

class Teacher extends Person {
  constructor(name, degree) {
    super(name);
    this.degree = degree;
  }
  teach() {
    console.log("teach");
  }
}

const teacher = new Teacher('Mosh', "MSc");


//Modules
// instead of writing code in one File,we addit in different file. 

```
