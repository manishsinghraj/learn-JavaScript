```js 
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



// ********************************************************************
//DOM

        function geeks() { 
            var node = document.createElement("P"); 
            var t = document.createTextNode("GeeksforGeeks"); 
            node.appendChild(t); 
            document.getElementById("sudo").appendChild(node); 
        } 
        function nClone() { 
            // Accessing div attribute using a variable geek 
            var geek = document.getElementsByTagName("DIV")[0]; 
  
            // Cloning geek variable into a variable named clone 
            var clone = geek.cloneNode(true); 
  
            // Adding our clone variable to end of the document 
            document.body.appendChild(clone); 
        } 
        function hasAttr() { 
            var s = document.body.hasAttributes(); 
            document.getElementById("gfg").innerHTML = s; 
        } 
  
        function Geeks() { 
            var doc = document.getElementById("listitem"); 
            doc.removeChild(doc.childNodes[0]); 
        } 
  
        /* Using getElementById */
        function getAttr() { 
            var rk = document.getElementById("button").getAttribute("onClick"); 
            document.getElementById("gfg1").innerHTML = rk; 
        } 
  
        /* Using getElementsByTagName */
        function getElement() { 
            var doc = document.getElementsByTagName("p"); 
            doc[0].style.background = "green"; 
            doc[0].style.color = "white"; 
        } 
  
        /* Cheacking the equality */
        function isequal() { 
            var out = document.getElementById("result"); 
            var divele = document.getElementsByTagName("div"); 
            out.innerHTML += 
                "element 1 equals element 1: " + 
                divele[0].isEqualNode(divele[0]) + 
                "<br/>"; 
            out.innerHTML += 
                "element 1 equals element 2: " + 
                divele[0].isEqualNode(divele[1]) + 
                "<br/>"; 
            out.innerHTML += 
                "element 1 equals element 3: " + 
                divele[0].isEqualNode(divele[2]) + 
                "<br/>"; 
        } 


// *************************************************************
// Events

        function hiThere() { 
            alert("Hi there!"); 
        } 
        function focused() { 
            var e = document.getElementById("inp"); 
            if (confirm("Got it?")) { 
                e.blur(); 
            } 
        } 
  
        /* Mouseover event */
        document.getElementById("hID").addEventListener("mouseover", over); 
  
        /* Mouseoout event */
        document.getElementById("hID").addEventListener("mouseout", out); 
  
        /* Over on green */
        function over() { 
            document.getElementById("hID").style.color = "green"; 
        } 
  
        /* Leaving Out Black */
        function out() { 
            document.getElementById("hID").style.color = "black"; 
        } 
  
        function Geeks() { 
            var x = document.getElementById("GFG").value; 
            document.getElementById("sudo").innerHTML = "Selected Subject: " + x; 
        } 
  
        /* Success alert */
        function Geek() { 
            alert("Form submitted successfully."); 
        } 
        function Function() { 
            document.getElementById("geeks").style.fontSize = "30px"; 
            document.getElementById("geeks").style.color = "green"; 
        } 


// *******************************************************************


// window

        // JS location property 
        let origin = window.location.origin; 
        document.getElementById("demo").innerHTML = origin; 
  
        // JS screen property 
        function getResolution() { 
            alert("Your screen is: " + screen.width + "x" + screen.height); 
        } 
  
        // JS toolbar property 
        var visible = window.toolbar.visible; 
  
        // JS navigator property 
        function checkConnectionStatus() { 
            if (navigator.onLine) { 
                alert("Application is online."); 
            } else { 
                alert("Application is offline."); 
            } 
        } 
        // JS history property 
        function getViews() { 
            alert( 
                "You've accessed " + history.length + " web pages in this session."
            ); 
        } 
        // JS close property 
        let myWindow; 
        function closeWin() { 
            if (myWindow) { 
                myWindow.close(); 
            } 
        } 

// *******************************
        var gfgWindow; 
  
        // Function that open the new Window 
        function windowOpen() { 
            gfgWindow = window.open( 
                "https://www.geeksforgeeks.org/", 
                "_blank", 
                "width=200, height=200"
            ); 
        } 
  
        // Function that Resize the open Window 
        function resizeWin() { 
            gfgWindow.resizeTo(400, 400); 
            gfgWindow.focus(); 
        } 
  
        // Function that Closes the open Window 
        function windowClose() { 
            gfgWindow.close(); 
        } 
  
        // Function that blur the open Window 
        function windowBlur() { 
            gfgWindow.blur(); 
        } 
  
        // Function that focus on open Window 
        function windowFocus() { 
            gfgWindow.focus(); 
        } 
  
        // Alert function 
        function wlcm() { 
            alert("Welcome to GeeksforGeeks"); 
        } 
  
        // Prompt function 
        function geek() { 
            var doc = prompt("Please enter some text", "GeeksforGeeks"); 
            if (doc != null) { 
                document.getElementById("g").innerHTML = "Welcome to " + doc; 
            } 
        } 
  
        // Function setTimeout and clearTimeout 
        var t; 
        function color() { 
            if (document.getElementById("btn").style.color == "blue") { 
                document.getElementById("btn").style.color = "green"; 
            } else { 
                document.getElementById("btn").style.color = "blue"; 
            } 
        } 
        function fun() { 
            t = setTimeout(color, 3000); 
        } 
        function stop() { 
            clearTimeout(t); 
        } 


```


