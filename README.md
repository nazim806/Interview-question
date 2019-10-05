# Interview-question

**Topic**


#1 **Object oriented programming (OOP)**
 
 Object oriented programming is a programming style or paradigm centered around objects rather than functions. OOP is not a programming language or a tool. There are many object oriented programming language such as C#, Java, Ruby, Python, Javascript. There are four core concepts of object oriented programming: i) Encapsulation ii) Abstraction iii) Inheritance and iv) Polymorphism.
 
 Encapsulation: OOP combined a gorup of related varables and functions into a unit which is called an object. The varibles are referred as properties and the functions as methods of the object. This is called encapsulation. For example, a 'car' is an object with properties like make,model, color and methods like start(),stop() and move().
 
 OOP solved the entangled sphagetti code with many functions which was traditionally used in procedural programming.  
 
 Procedural programming has variables and functions separated/decoupled, whereas in OOP properties(variables) and methods(functions) are together. Also OOP has minimum or no function parameters.
 
 
 "The best functions are those with no parameters." - Uncle Bob
 
Abstraction: In OOP details and complexity of properties and methods are hidden, and show only the essentials. Therefore we have simple interface, reduce the impact of change.
 
 Inheritance: Inheritance is a mechanism to eliminate redundant code.
 
 Polymorphism: Polymorphism means many forms. It provides a way to perform a single action in different forms. It provides an ability to call the same method on different JavaScript objects and helps us refactor ugly 'if and else' or 'switch and case' statements. 
 
 


#2 **Model view controller (MVC)**


Model–View–Controller (usually known as MVC) is a software architectural pattern, commonly used for developing user interfaces which divides the related program logic into three interconnected elements.


#3 **Constructor function**

"In JavaScript, any function can return a new object. When it’s not a constructor function or class, it’s called a factory function."


#4 **Prototype, prototypical inheritance**


There is a super object in JavaScript that all objects will inherit from it. ‘__proto__’ is an internal property of an object which points to the Prototype. A prototype contains a constructor which lets the object be capable of creating the instances from it. __proto__ will always exist in objects and hierarchically point to the prototype it belongs to until null, which is called the prototype chain.


"Favor composition over Inheritance".

#5 **Recursion**

Recursion is simply when a function calls itself. All recursive functions should have three key features: a termination condition, a base case and the recursion. 

Recursion is a group of nested function calls. With nested functions, the most inner nested function will return first.

```js
function factorial(x) {

  // TERMINATION
  if (x < 0) return;
  
  // BASE
  if (x === 0) return 1;
   
  // RECURSION
   return x * factorial(x - 1);  
}
factorial(3);
// 6 

```



#6 **Async/Await**
  The async function declaration defines an asynchronous function, which returns an AsyncFunction object. An asynchronous function is a function which operates asynchronously via the event loop, using an implicit Promise to return its result.
  
  An async function can contain an await expression that pauses the execution of the async function and waits for the passed Promise's resolution, and then resumes the async function's execution and evaluates as the resolved value.
The await keyword is only valid inside async functions. Outside of an async function's body, you will get a SyntaxError. For example,

```js

async function f() {
  let promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("done!"), 1000)    
  });

  let result = await promise; // wait till the promise resolves
  alert(result); // "done!"  
}
f(); 

```

#7 **Callback function**

A callback is a function that is to be executed after another function has finished executing. In JavaScript, functions are objects. Because of this, functions can take functions as arguments, and can be returned by other functions. Functions that do this are called higher-order functions. Any function that is passed as an argument is called a callback function.

 Callbacks are a way to make sure certain code doesn’t execute until other code has already finished execution.
 
 ```js
 
 function first(){
  // Simulate a code delay
  setTimeout( function(){
    console.log(1);
  }, 500 );
}
function second(){
  console.log(2);
}
first();
second();

// 2
// 1

```

In this example even though we invoked the first() function first, we logged out the result of that function after the second() function.


#8 **Single page application (SPA)**

A single-page application (SPA) is a web application or web site that interacts with the user by dynamically rewriting the current page rather than loading entire new pages from a server. This approach avoids interruption of the user experience between successive pages, making the application behave more like a desktop application. In a SPA, either all necessary code – HTML, JavaScript, and CSS – is retrieved with a single page load, or the appropriate resources are dynamically loaded and added to the page as necessary, usually in response to user actions. The page does not reload at any point in the process, nor does control transfer to another page, although the location hash or the HTML5 History API can be used to provide the perception and navigability of separate logical pages in the application. Interaction with the single page application often involves dynamic communication with the web server behind the scenes.

An SPA is fully loaded in the initial page load and then page regions are replaced or updated with new page fragments loaded from the server on demand. To avoid excessive downloading of unused features, an SPA will often progressively download more features as they become required, either small fragments of the page, or complete screen modules. 

#9 **Dot notation and Bracket notation**

When working with dot notation, property identifies can only be alphanumeric (and _ and $). Properties can’t start with a number.
Here is 

dot notation syntax: objectName.propertyName; and 
bracket notation syntax: objectName["propertyName"];.

```js
let data = {
    name: "Name",
    age: 10
}

// Bracket notation
console.log(data["name"]);
console.log(data["age"]);

// Dot notation
console.log(data.name);
console.log(data.age);
```


#10 **Local storage, session storage, cookies**

Web applications can store data locally within the user's browser.
HTML web storage provides two objects for storing data on the client:

window.localStorage - stores data with no expiration date
window.sessionStorage - stores data for one session (data is lost when the browser tab is closed)

The localStorage Object:

The localStorage object stores the data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.
```js
// Store
localStorage.setItem("lastname", "Smith");
// Retrieve
localStorage.getItem("lastname");
//Remove
localStorage.removeItem("lastname");
```

The sessionStorage Object:

The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session. The data is deleted when the user closes the specific browser tab.



Cookies:

The expiration time for each cookie can be set.
The 4K limit is for the entire cookie, including name, value, expiry date etc. To support most browsers, keep the name under 4000 bytes, and the overall cookie size under 4093 bytes.
The data is sent back to the server for every HTTP request (HTML, images, JavaScript, CSS, etc) - increasing the amount of traffic between client and server.

Cookies are used for authentication purposes and persistence of user data, all cookies valid for a page are sent from the browser to the server for every request to the same domain - this includes the original page request, any subsequent Ajax requests, all images, style-sheets, scripts and fonts.

In terms of capabilities, cookies only allow you to store strings. sessionStorage and localStorage allow you to store JavaScript primitives but not Objects or Arrays. Session storage will generally allow you to store any primitives or objects supported by your Server Side language/framework.

#11 **Getters and Setters**

Getter is a function that is used to read property. Use object.defineProperty method to define getters and/or setters.

```js
function object (){

    let defaultLocation = {x:0, y:0}; 
object.defineProperty(this, 'defaultLocation', {
    get:function(){   
        return defaultLocation;      
    },

    set: function(value) {
        if (!value.x) || !value.y)
            throw new Error ('Invalid location.');
          defaultLocation = value;            
    }        
});
}

```
object.defaultLocation value can be used for validation.



#12 **"This" keyword**


In javascript "this" should represent the object where ‘this’ keyword currently located. But ‘this’ keyword is determined by how the function will be called. ‘this’ refers to the caller. If the caller cannot be found, ‘this’ will point to windows object.

#13 **Closure**

The closure in JS is about creating a closed lexical scope inside another scope, so the inner scope can access the outer scope. The closure is created as the function is created. The closure is to make variables and methods private in the scope.

#14 **Hoisting**

Hoisting is the JS default behavior which means moving all declarations to the top of the current scope and let variables can be used before the declaration. Initialization won’t be hoisted. Hoisting is only for declaration not for function expression.

The example below will hoist x, y at the top
```js
var x = 1
console.log(x + “ — -”+y) // 1 — -undefined
var y = 2
```

#15 **Function expression and function declaration**



The declaration will be defined during the parsing time, and expression will be defined at run time.

Function Expression is better than function declaration which is just a floating function 
and can be referred anywhere in the code. So, it’s wise to use function expression with a variable

e.g.,
```js
let a=1;
let b=2;
let add = function(a,b){
 return a+b;
}
 
```
#16 **Higher order function**


A function that accepts and /or returns another function is called higher-order function.

#17 **Strict Mode**


JavaScript's strict mode, introduced in ECMAScript 5, is a way to opt in to a restricted variant of JavaScript, thereby implicitly opting-out of "sloppy mode". Strict mode isn't just a subset: it intentionally has different semantics from normal code. Browsers not supporting strict mode will run strict mode code with different behavior from browsers that do, so don't rely on strict mode without feature-testing for support for the relevant aspects of strict mode. Strict mode code and non-strict mode code can coexist, so scripts can opt into strict mode incrementally.

Strict mode makes several changes to normal JavaScript semantics:

Eliminates some JavaScript silent errors by changing them to throw errors.
Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.
Prohibits some syntax likely to be defined in future versions of ECMAScript.

#18 **Asynchronous function**


Although JS is a single thread programming language with one call stack, it can also deal with some asynchronous functions using a mechanism called **event loop**. Knowing how JavaScript works from the fundamental level is the essential section to understand how the JS handles async.

In JS setTimout is an async method, which takes in a callback function as a parameter. The second parameter is the time, after which the callback is triggered.

#19 **Event delegation**


Event delegation is  a technique to let the event listeners on parents element also affect children element. Usually, event propagation( capturing and bubbling) allows us to implement event delegation. 

#20 **Function and Block scope (Const Var Let)**

var is function scope.
let and const are block scope.
Function scope is within the function.
Block scope is within curly brackets.

Var can be reassigned and updated. var variables are ‘function scope.’  It means they are only available inside the function they’re created in, or if not created inside a function, they are ‘globally scoped.’
If var is defined inside a function and you try to call it outside the function, it won’t work.

Benefits of using let and const: Rather than being scoped to the function they are scoped to the block.



#21 **Local vs Global scope**

In JavaScript there are two types of scope:
Local scope
Global scope
JavaScript has function scope: Each function creates a new scope. 
Scope determines the accessibility (visibility) of these variables.
Variables defined inside a function are not accessible (visible) from outside the function.

Local JavaScript Variables
Variables declared within a JavaScript function, become LOCAL to the function.
Local variables have Function scope: They can only be accessed from within the function.

Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.
Local variables are created when a function starts, and deleted when the function is completed.

Global JavaScript Variables
A variable declared outside a function, becomes GLOBAL.
A global variable has global scope: All scripts and functions on a web page can access it. 

#22 **Truthy and Falsy**

Each value in Javascript has an inherent boolean value, generally known as either truthy or falsy. Some of the rules are a little bizarre so understanding the concepts and effect on comparison helps when debugging JavaScript applications.


The following values are always falsy:
```js
false

0 (zero)

'' or "" (empty string)

null

undefined

NaN
```

Everything else is truthy. That includes:

```js
'0' (a string containing a single zero)

'false' (a string containing the text “false”)

[] (an empty array)

{} (an empty object)

function(){} (an “empty” function)

```


#23 **Event loop**


The event loop is basically an endless loop, which keeps on checking whether there is something to be executed in the call stack. If the call stack is empty it checks the Event Queue, whether there is something to move to the call stack. If there is a method present, it moves it to the call stack and the method gets executed. 

In short,  the event loop is a process that runs endlessly and whose only job is to monitor and transfer methods to the call stack from the event queue.

#24 **Document Object Model (DOM)**



DOM is an acronym for the document object model. DOM creates a visual representation of our HTML code. Meaning, what we see projected on our web pages is not our hard-coded HTML but a representation of it.

#25 **Data Structure**



At a high level there are three types of data structures:


   i) Arrays/lists : Stacks, Queues are like array that differ only in how items are inserted and removed. Stacks and queues are the simplest and can be constructed from linked lists.
   
   
   ii) Structures with nodes: Linked lists, Trees and Graphs are structures with nodes that keep references to other nodes. Trees and graphs are the most complex data structures because they extend the concept of a linked list.
   
   iii) Hash Tables: Hash tables depend on hash functions to save and locate data.


>"Bad programmers worry about the code. Good programmers worry about data structures and their relationships." - Linus Torvalds
   
#26 **Stacks and Queues**

Stack is just an array with two principled operations: push and pop. Push add elements to the top of the array, while pop removes them from the same location. Stack follows the *"Last In, First Out"* protocol (**LIFO**). Most important stack in JS is the call stack where we push in the scope of a function whenever we execute it.

Queues are arrays with two primary operations: unshift and pop. Unshift enqueues items to the end of the array, while Pop dequeues them from the beginning of the array. In other words, Queues follow the *"First In, First Out"* protocol (**FIFO**).If the direction is reversed, we can replace unshift and pop with push and shift, respectively.



#27 **Linked lists**

Like arrays, linked lists store data elements in sequential order. Instead of keeping indexes, linked lists hold pointers to other elements. The first node is called the head while the last node is called the tail. In a singly-linked list, a pointer to the previous node is also kept. 

Like arrays, linked lists can operate as stacks. Head is the only place for insertion and removal. In a doubly-linked list linked lists can also operate as queues, where insertion occurs at the tail and removal occurs at the head, or vice-versa.

Linked lists are useful on both the client and server. On the client, state management libraries like Redux structure its middleware logic in a linked-list fashoin. On the server, web frameworks like Express also structure its middleware logic in a similar fashion.

#28 **Tree data structure**

A Tree is like a linked list, except it keeps references to many child nodes in a hierarchical structure. Each node can have no more than one parent. The Document Object Model (DOM) is such a structure, with a root html node that branches into the head and body nodes, which further subdivide into all the familiar html tags. React's virtual DOM is also a tree structure.

In the Binary Search Tree each node can have no more than two children. The left child must have a value that is smaller than or equal to its parent, while the right child must have a greater value. Structured and balanced this way, we can search for any value in logarithmic time because we can ignore one-half of the branching with each iteration.

Traversal through the tree can happen in a vertical or horizontal procedure. In **Depth-First Traversal** (DFT) in the vertical direction a recursive algorithm is more elegant than an iterative one. Nodes can be traversed in pre-order, in-order, or post-order. If we need to explore the roots before inspecting the leaves, we should choose pre-order. But, if we need to explore the leaves before the roots, we should choose post-order. As its names implies, in-order enables us to traverse the nodes in sequential order. The property makes Binary Search Trees optimal for sorting.

In **Breadth-First Traversal** (BFT) in the horizontal direction, an iterative approach is more elegant than a recursive one. This requires the use of a queue to track all the children nodes with each iteration. However, the memory needed for such a queue might not be trivial. If the shape of a tree is wider than deep, BFT is a better choice than DFT. Also, the path that BFT takes between any two nodes is the shortest one possible.


#29 **Graph data structure**

If  a tree is free to have more than one parent, it becomes a Graph. Edges that connect nodes together in a graph can be directed or undirected, weighted or unweighted. Edges that have both direction and weight are analogous to vectors.

Multiplr inheritances in the form of Mixins and data objects that have many-to-many relationships produce graph structures. A social network and the internet itself are also graphs. The most complicated graph in nature is our human brain,which neural networks attempt to replicate to give machines superintelligence.


#30 **Hash Table**

A Hash table is a dictionary-like structure that pairs keys to values. The location in memory of each pair is determined by a hash function, which accepts a key and returns the address where the pair should be inserted and retrieved.
   

#31 **Algorithm**

An algorithm is like a function that transforms  certain input data structure into a certain output data structure. The logic inside decides the transformation.The inputs and outputs should clearly be defined as unit tests.

>“Algorithms: a common language for nature, human, and computer. ”  —  Avi Wigderson

>“Algorithms + Data Structures = Programs. ”    — Niklaus Wirth

>“An algorithm must be seen to be believed. ”    —  Donald Knuth

>“ For me, great algorithms are the poetry of computation. Just like     verse, they can be terse, allusive, dense, and even mysterious.   But once unlocked, they cast a brilliant new light on some   aspect of computing.  ”    — Francis Sullivan




#32 **Big-O notation**

Big O notation is used to classify algorithms according to how their running time or space requirements grow as the input size grows. Big O notation is useful when analyzing algorithms for efficiency. For example, the time (or the number of steps) it takes to complete a problem of size n might be found to be T(n) = 4n2 − 2n + 2. As n grows large, the n2 term will come to dominate, so that all other terms can be neglected—for instance when n = 500, the term 4n2 is 1000 times as large as the 2n term. Ignoring the latter would have negligible effect on the expression's value for most purposes. 


#33 **Coercion** 

Type coercion is the process of converting value from one type to another (such as string to number, object to boolean, and so on).
Type coercion can be explicit and implicit.

When a developer expresses the intention to convert between types by writing the appropriate code, like Number(value), it’s called explicit type coercion (or type casting).  Values can also be converted between different types automatically, and it is called implicit type coercion. It usually happens when you apply operators to values of different types, like
1 == null

#34 **Javascript Classes**

Javascript Classes are very similar to functions. Much like functions which have both function expressions and function declarations, classes have two components: class expressions and class declarations. Classes do not introduce a new inheritance model to JavaScript.
They’re often described as syntactical sugar over JavaScript’s existing structure of prototypical inheritance. One important difference between function declarations and class declarations is that function declarations are hoisted and class declarations are not. 

Class declaration:

```js
class Image {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

A class expression is the other way to define a class. Class expressions can be named or unnamed. 
```js
// An unnamed class expression
let Image = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Image.name);
// output: "Image"
// A named class expression
let MyImage = class Image {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(MyImage.name);
// output: "Image"
```

#35 **The Super keyword**

The super keyword is used to call corresponding methods of super class. This is one advantage over prototype-based inheritance.For example,

```js
class Volkswagen { 
  constructor(name) {
    this.name = name;
  }
  
  sound() {
    console.log(`${this.name} makes a sound.`);
  }
}
class Beetle extends Volkswagen {
  sound() {
    super.sound();
    console.log(`${this.name} toots it's horn.`);
  }
}
let b = new Beetle('Herbie');
b.sound(); 
// Herbie makes a sound.
// Herbie toots it's horn.
```


#36 **Mixins**

Mix-ins are templates for classes. A mixin is a class containing methods that can be used by other classes without a need to inherit from it.

>Mixin is a way properties are added to objects without using inheritance — Darren Jones

>Mixins are a form of object composition, where component features get mixed into a composite object so that properties of each mixin become properties of the composite object. — Eric Elliot

Mixin example:
```js
// mixin
function mixin (target, ...sources{
  object.assign (target, ...sources);
  }
const mydetails = {}
const  firstname = { firstname: "Nazim" }
const surname = { surname: "Uddin" }
const occupation = { occupation: "Software Developer" }
const nationality = { nationality: "American" }
console.log(mydetails)
mixin(mydetails,surname, firstname, occupation, nationality);
console.log(mydetails)
```

Object.assign(mixin) provides the basis in JavaScript for mixin properties between objects(objects without classes).

It takes as first argument the target object and then accepts all the objects to mixed with the target object as a rest ... argument.

#37 **Static methods**

Static methods, like many other features introduced in ES6, are meant to provide class-specific methods for object-oriented programming in Javascript.To declare a static method, simply prefix a method declaration with the word static inside the class declaration.

>“Static methods are called without instantiating their class and are also not callable when the class is instantiated. Static methods are often used to create utility functions for an application.” 

In other words, static methods have no access to data stored in specific objects.

```js
class Foo(){
   static methodName(){
      console.log("bar")
   }
}
```

Since these methods operate on the class instead of instances of the class, they are called on the class. There are two ways to call static methods:
```js
Foo.methodName() 
// calling it explicitly on the Class name
// this would give you the actual static value. 
this.constructor.methodName() 
// calling it on the constructor property of the class
// this might change since it refers to the class of the current instance, where the static property could be overridden

```


#38 **Polymorphism**

Polymorphism is one of the tenets of Object Oriented Programming (OOP). It is the practice of designing objects to share behaviors and to be able to override shared behaviors with specific ones. Polymorphism takes advantage of inheritance in order to make this happen.

#39 **Transpiler (Babel)**

Transpiler is the combination of two words translator and compiler. It converts modern Javascript code to ES5 that all browsers can understand. Babel is an example of a very popular transpiler.

#40 **Bundler (Webpack)**

Bundler combines all javascript files in a browser into a single file. Bundler minify javascript codes and get rid of all the white spaces, comments and uglify the codes. It also shorten the name of identifiers such as functions, objects thereby reduces the size of the file and deliver to client. There are many bundler, Webapck is one of the popular bundler. 




