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
 
 Polymorphism: Polymorphism means many forms. It helps us refactor ugly 'if and else' or 'switch and case' statements.
 
 


#2 **Model view controller (MVC)**


Model–View–Controller (usually known as MVC) is a software architectural pattern, commonly used for developing user interfaces which divides the related program logic into three interconnected elements.


#3 **Constructor function**

"In JavaScript, any function can return a new object. When it’s not a constructor function or class, it’s called a factory function."


#4 **Prototype, prototypical inheritance**


There is a super object in JavaScript that all objects will inherit from it. ‘__proto__’ is an internal property of an object which points to the Prototype. A prototype contains a constructor which lets the object be capable of creating the instances from it. __proto__ will always exist in objects and hierarchically point to the prototype it belongs to until null, which is called the prototype chain.


"Favor composition over Inheritance".

#5 **Recursion**



calling a function without recalling an iteration.

#5 **Async/Await**
  The async function declaration defines an asynchronous function, which returns an AsyncFunction object. An asynchronous function is a function which operates asynchronously via the event loop, using an implicit Promise to return its result.
  
  An async function can contain an await expression that pauses the execution of the async function and waits for the passed Promise's resolution, and then resumes the async function's execution and evaluates as the resolved value.
The await keyword is only valid inside async functions. Outside of an async function's body, you will get a SyntaxError. For example,

** async function f() {



  let promise = new Promise((resolve, reject) => {
  
  
    setTimeout(() => resolve("done!"), 1000)
    
    
  });


  let result = await promise; // wait till the promise resolves
  
  

  alert(result); // "done!"
  
  
}



f(); 

**

#6 **Callback function**



#7 **Single page application (SPA)**



#8 **Dot notation and Bracket notation**

When working with dot notation, property identifies can only be alphanumeric (and _ and $). Properties can’t start with a number.
Here is 

dot notation syntax: objectName.propertyName; and 
bracket notation syntax: objectName["propertyName"];.

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



#9 **Local storage, session storage, cookies**



#10 **Getters and Setters**

Getter is a function that is used to read property. Use object.defineProperty method to define getters and/or setters.

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
} );
}
object.defaultLocation;



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




#32 **Coercion** 

Type coercion is the process of converting value from one type to another (such as string to number, object to boolean, and so on).
Type coercion can be explicit and implicit.

When a developer expresses the intention to convert between types by writing the appropriate code, like Number(value), it’s called explicit type coercion (or type casting).  Values can also be converted between different types automatically, and it is called implicit type coercion. It usually happens when you apply operators to values of different types, like
1 == null

#33 **Javascript Classes**



#34 **The Super keyword**



#35 **Mixins**


#36 **Static methods**



#37 **Polymorphism**



#38 **Transpiler (Bablejs)**


#38 **Bundler (Webpack)**



