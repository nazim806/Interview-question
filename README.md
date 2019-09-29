# Interview-question

**Topic**


#1 **Object oriented programming (OOP)**


#2 **Model view control (MVC)**


#3 **Constructor function**


#4 **Prototype, prototypical inheritance**
There is a super object in JavaScript that all objects will inherit from it. ‘__proto__’ is an internal property of an object which points to the Prototype. A prototype contains a constructor which lets the object be capable of creating the instances from it. __proto__ will always exist in objects and hierarchically point to the prototype it belongs to until null, which is called the prototype chain.


"Favor composition over Inheritance".

#5 **Recursion**

calling a function without recalling an iteration.

#5 **Async/Await**

#6 **Callback function**

#7 **Single page application (SPA)**

#8 **Dot notation and Bracket notation**

#9 **Local storage, session storage, cookies**

#10 **Getters and Setters**

#11 **"This" keyword**

In javascript "this" should represent the object where ‘this’ keyword currently located. But ‘this’ keyword is determined by how the function will be called. ‘this’ refers to the caller. If the caller cannot be found, ‘this’ will point to windows object.

#12 **Closure**

The closure in JS is about creating a closed lexical scope inside another scope, so the inner scope can access the outer scope. The closure is created as the function is created. The closure is to make variables and methods private in the scope.

#13 **Hoisting**

Hoisting is the JS default behavior which means moving all declarations to the top of the current scope and let variables can be used before the declaration. Initialization won’t be hoisted. Hoisting is only for declaration not for function expression.

The example below will hoist x, y at the top

var x = 1
console.log(x + “ — -”+y) // 1 — -undefined
var y = 2


#14 **Function expression and function declaration**

The declaration will be defined during the parsing time, and expression will be defined at run time.

Function Expression is better than function declaration which is just a floating function 
and can be referred anywhere in the code. So, it’s wise to use function expression with a variable

e.g.,

let a=1;
let b=2;
let add = function(a,b){
 return a+b;
}
 

#15 **Higher order function**

A function that accepts and /or returns another function is called higher-order function.

#16 **Strict Mode**

JavaScript's strict mode, introduced in ECMAScript 5, is a way to opt in to a restricted variant of JavaScript, thereby implicitly opting-out of "sloppy mode". Strict mode isn't just a subset: it intentionally has different semantics from normal code. Browsers not supporting strict mode will run strict mode code with different behavior from browsers that do, so don't rely on strict mode without feature-testing for support for the relevant aspects of strict mode. Strict mode code and non-strict mode code can coexist, so scripts can opt into strict mode incrementally.

Strict mode makes several changes to normal JavaScript semantics:

Eliminates some JavaScript silent errors by changing them to throw errors.
Fixes mistakes that make it difficult for JavaScript engines to perform optimizations: strict mode code can sometimes be made to run faster than identical code that's not strict mode.
Prohibits some syntax likely to be defined in future versions of ECMAScript.

#17 **Asynchronous function**

Although JS is a single thread programming language with one call stack, it can also deal with some asynchronous functions using a mechanism called **event loop**. Knowing how JavaScript works from the fundamental level is the essential section to understand how the JS handles async.

In JS setTimout is an async method, which takes in a callback function as a parameter. The second parameter is the time, after which the callback is triggered.

#18 **Event delegation**

Event delegation is  a technique to let the event listeners on parents element also affect children element. Usually, event propagation( capturing and bubbling) allows us to implement event delegation. 

#19 **Const Var Let**



#20 **Local vs Global scope**



#21 **Truthy and Falsy**

#22 **Event loop**

The event loop is basically an endless loop, which keeps on checking whether there is something to be executed in the call stack. If the call stack is empty it checks the Event Queue, whether there is something to move to the call stack. If there is a method present, it moves it to the call stack and the method gets executed. 

In short,  the event loop is a process that runs endlessly and whose only job is to monitor and transfer methods to the call stack from the event queue.

#23 **Document Object Model (DOM)**

DOM is an acronym for the document object model. DOM creates a visual representation of our HTML code. Meaning, what we see projected on our web pages is not our hard-coded HTML but a representation of it.

#24 **Data Structure**

At a high level there are three types of data structures:


   i) Arrays/lists : Stacks, Queues are like array that differ only in how items are inserted and removed. Stacks and queues are the simplest and can be constructed from linked lists.
   
   
   ii) Structures with nodes: Linked lists, Trees and Graphs are structures with nodes that keep references to other nodes. Trees and graphs are the most complex data structures because they extend the concept of a linked list.
   
   iii) Hash Tables: Hash tables depend on hash functions to save and locate data.


"Bad programmers worry about the code. Good programmers worry about data structures and their relationships." - Linus Torvalds
   
#25 **Stacks and Queues**


#26 **Linked lists**


#27 **Tree data structure**


#28 **Graph data structure**


#29 **Hash Table**


   


#30 **Algorithm**



#31 **Big-O notation**





# **Coercion** 

Type coercion is the process of converting value from one type to another (such as string to number, object to boolean, and so on).
Type coercion can be explicit and implicit.

When a developer expresses the intention to convert between types by writing the appropriate code, like Number(value), it’s called explicit type coercion (or type casting).  Values can also be converted between different types automatically, and it is called implicit type coercion. It usually happens when you apply operators to values of different types, like
1 == null

