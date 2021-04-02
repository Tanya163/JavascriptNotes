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


## Module - 5

**Event Listeners**: 
Event listeners are among the most frequently used JavaScript structures in web design. They allow us to add interactive functionality to HTML elements by “listening” to different events that take place on the page, such as when the user clicks a button, presses a key, or when an element loads.


Event listener and event handler are two terms that cause confusion. ... A listener watches for an event to be fired. The handler is responsible for dealing with the event.

Const Butts=document.querySelector(‘.button’);            //get the first element of the class using
                                                                                             //querySelector
Butts.addEventListener(‘click’,call_back_function);

addEventListener(‘click’,function() {           //anonymous function
Console.log(‘It got clicked’}
);

Function handleClick()
{
Console.log(‘clicked’);
}

Butts.addEventListener(‘click’,handleClick);         //name function


Const hey=() => console.log(‘hey’)                  // fat arrow function


In order to listen to multiple buttons or elements we use querySelectorALL()

In order to attach event handler to all the elements or buttons we need to loop them using foreach()

eg.   buttons.forEach(function(button)   {         //button is just a parameter to traverse all the 
                                                                              //elements in buttons
Console.log(‘hey’);
buttons.addEventListener(‘click’, function {  console.log(‘hey again’)        //this anonymous 
                                                                                                                           //function is known as  
                                                                                                                           //event handler 
});



Target property tells that which element has triggered the event.
Target (the event which is being fired) and currentTarget(the main element) difference :
target is the element that triggered the event (e.g., the user clicked on) currentTarget is the element that the event listener is attached to
Why  event.target === event.currentTarget are same not always only when there are no other tags attached.

**Propagation**: Flow to events getting triggered

**Event bubbling** :  events get triggered from child to parents from bottom to up
There are two ways of event propagation in the HTML DOM, bubbling and capturing.
Event propagation is a way of defining the element order when an event occurs. If you have a <p> element inside a <div> element, and the user clicks on the <p> element, which element's "click" event should be handled first?
In bubbling the inner most element's event is handled first and then the outer: the <p> element's click event is handled first, then the <div> element's click event.

We can stop bubbling by using stopPropagation() function 


**Event capture**: goes from the root of the DOM tree to way down till the target node.
Eg: window.addEventListener
(
‘click’, function(event) 
{ console.log(‘you clicked the window’) 
},
{capture:true} 
);

Console.log(e.currentTarget) and console.log(this) to get the current  node but this keyword has a downside with the arrow function related to its scope.  Recommended to not use this in eventListener’s callback function ??

//confirm
//Prompt
//console.dir(event.target)
//includes
Events :
//keyup
//keydown
//focus
//blur
//event.key

**event.PreventDefault()**

## Module-7

* B brackets
* E exponents
* D ivision
* M ultiplication
* A ddition
* S ubration

//.replace(/\s/g,’-‘)    //regex-regular expression
//console.group()
//console.groupend()

Empty string is not true it is  not false its an empty string
**Truthy**: which are equated to true I.e. all numbers and any value , empty array and empt object also.
**Falsey**  : which equates to false eg : 0 for numbers and empty string for strings. , undefined , null , NaN 

**Coercion** converting something of a different datatype into another type
And ! Operator coerces any datatype into a true boolean(either true or false).

**Shortcircuiting** (with if condition and &&) and its solution:
Use a single &. That is a bitwise operator. It will execute all conditions and then return a bitwise sum of the results.

 function checkAll() {
    return checkSomething(1)
      & checkSomething(2)
      & checkSomething(3)
 }


The window object allows execution of code at specified time intervals.
These time intervals are called timing events.
The two key methods to use with JavaScript are:
**1. setTimeout(function, milliseconds)** :Executes a function, after waiting a specified number of milliseconds.
**2. setInterval(function, milliseconds)** :Same as setTimeout(), but repeats the execution of the function continuously. Will not run immediately so you have to make your own immediate function by calling the call_back function immediately inside your customised function.
**3. clearTimeout(reference to the setTimeout function i.e in a variable)**:for stoping setTimeout.

How to stop an interval after x seconds:
 setTimeout(function() {
clearInterval( reference var name)  } , 3000);



