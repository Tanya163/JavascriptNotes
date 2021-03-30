# JavascriptNotes

JavaScript is a high level, interpreted, programming language used to make web pages more interactive. It is a very powerful client-side scripting language which makes your webpage more lively and interactive.

## Variables
A memory location that acts as a container for storing data is named as a Variable. They are reserved memory locations.

You have to use the ‘let’ keyword to declare a variable. The syntax is as follows:

 let age;
 age = 23;
 
## Constants
The values that are fixed and cannot be changed during execution time are called constants. To declare a  constant you have to use the ‘const’ keyword.

The syntax is as follows:

Const value;
value = 7;

## Data Types
You can assign different types of values to a variable such as a number or a string. There are different data types such as: 
Numbers
Strings
Boolean
Undefined
Null

## Objects
Objects are variables too, but they contain many values, so instead of declaring different variables for each property, you can declare an object which stores all these properties

To declare an object in JavaScript use the ‘let’ keyword and make sure to use curly brackets in such a way that all property-value pairs are defined within the curly brackets. The syntax is as follows:


let user= {
 
name: 'Aron',id: '1234'
 
};

In this example, the user is the object with two different properties, i.e, name, and id.

## Arrays
An array is a data structure that contains a list of elements which store multiple values in a single variable.

To declare an array in JavaScript use the ‘let’ keyword with square brackets and all the array elements must be enclosed within them. The syntax is as follows:

let shopping=[];
shopping=['paintBrush','sprayPaint','waterColours','canvas'];

## Functions
A function is a block of organized, reusable code that is used to perform single, related action.

To declare a function in JavaScript, use the ‘function’ keyword. The Syntax is as follows:


function sum(a, b) {
return a+b;
}

When JavaScript reaches a return statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.

Functions often compute a return value. The return value is "returned" back to the "caller":


var x = myFunction(4, 3);   

function myFunction(a, b) {
  return a * b;             
}

## Closures
JavaScript variables can belong to the local or global scope.
Global variables can be made local (private) with closures.



## DOM Manipulation
When a web page is loaded, the browser creates a Document Object Model of the page.

The HTML DOM model is constructed as a tree of Objects.The HTML DOM is a standard object model and programming interface for HTML. It defines:

The HTML elements as objects
The properties of all HTML elements
The methods to access all HTML elements
The events for all HTML elements

A property is a value that you can get or set (like changing the content of an HTML element).
A method is an action you can do (like add or deleting an HTML element).

<html>
<body>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "Hello World!";
</script>

</body>
</html>

In the example above, ### getElementById is a method, while innerHTML is a property.

The innerHTML property can be used to get or change any HTML element, including <html> and <body>.

## Methods:

document.getElementById(id):	Find an element by element id
document.getElementsByTagName(name): Find elements by tag name
document.getElementsByClassName(name):	Find elements by class name


