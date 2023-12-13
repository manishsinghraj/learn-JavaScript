// prototype object

// Creating an object with a method
const person = {
    sayHello: function () {
        console.log('Hello, I am ' + this.name);
    }
};

// Creating a new object that inherits from the 'person' object
const john = Object.create(person);
john.name = 'John';

// Now 'john' has access to the 'sayHello' method through prototypal inheritance
john.sayHello(); // Output: Hello, I am John

// *************************************************************


//Vaiable in JS

console.log("Using var Keyword");
var x = 1;
if (x === 1) {
    var x = 2;
    console.log(x); // Output: 2 
}
console.log(x); // Output: 2 


// Using let keyword 
console.log("Using let Keyword");
let x1 = 1;
if (x1 === 1) {
    let x1 = 2;
    console.log(x1); // Output: 2 
}
console.log(x1); // Output: 1 


// Using const keyword 
console.log("Using const Keyword");
const number = 48;

// Changing const value will display TypeError 
try {
    const number = 42;
} catch (err) {
    console.log(err);
}
console.log(number); // Output: 48 


// *******************************************************

let x = 5; 
let y = 3; 

// Addition 
console.log("x + y = ", x); // 8 

// Subtraction 
console.log("x - y = ", x - y); // 2 

// Multiplication 
console.log("x * y = ", x * y); // 15 

// Division 
console.log("x / y = ", x / y); 

// Remainder 
console.log("x % y = ", (x % y)); // 2 

// Increment 
console.log("++x = ", ++x); // x is now 6 
console.log("x++ = ", x++); 
console.log("x = ", x); // 7 

// Decrement 
console.log("--x = ", --x); // x is now 6 
console.log("x-- = ", x--); 
console.log("x = ", x); // 5 

// Exponentiation 
console.log("x ** y =", x ** y); 

// Comparison 
console.log(x > y); // true 

// Equal operator 
console.log((2 == 2)); // true 

// Not equal operator 
console.log((3 != 2)); // true 

// Strict equal operator 
console.log((2 === 2)); // true 

// Strict not equal operator 
console.log((2 !== 2)); // true 

// Logical Operator 

// Logical AND 
console.log((x < 6 && y < 5)); // true 

// Logical OR 
console.log((x < 6 || y > 6)); // true 

// Logical NOT 
console.log(!(x < 6)); // false 


// ***************************************************

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




