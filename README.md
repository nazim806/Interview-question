# Interview-question

**Topic**


#1 **Object oriented programming (OOP)**


#2 **Model view control (MVC)**


#3 Constructor function


#4 Prototype, prototypical inheritance

#5 Recursion: calling a function without recalling an iteration.

#5 Async/Await

#6 Callback function

#7 Single page application (SPA)

#8 Dot notation and Bracket notation

#9 Local storage, session storage, cookies

#10 Getters and Setters

#11 **"This" keyword**

In javascript "this" should represent the object where ‘this’ keyword currently located. But ‘this’ keyword is determined by how the function will be called. ‘this’ refers to the caller. If the caller cannot be found, ‘this’ will point to windows object.

#12 **Closure**

The closure in JS is about creating a closed lexical scope inside another scope, so the inner scope can access the outer scope. The closure is created as the function is created. The closure is to make variables and methods private in the scope.

#13 **Hoisting**

Hoisting is the JS default behavior which means moving all declarations to the top of the current scope and let variables can be used before the declaration. Initialization won’t be hoisted. Hoisting is only for declaration.

The example below will hoist x, y at the top

var x = 1
console.log(x + “ — -”+y) // 1 — -undefined
var y = 2


#14 Function expression and function declaration

#15 Higher order function

#16 Strict Mode

#17 **Asynchronous function**

Although JS is a single thread programming language with one call stack, it can also deal with some asynchronous functions using a mechanism called **event loop**. Knowing how JavaScript works from the fundamental level is the essential section to understand how the JS handles async.

#18 **Event delegation**

Event delegation is  a technique to let the event listeners on parents element also affect children element. Usually, event propagation( capturing and bubbling) allows us to implement event delegation. 

#19 **Higher-order function**
A function that accepts and /or returns another function is called higher-order function.


#20 **Function expression and function declaration**

The declaration will be defined during the parsing time, and expression will be defined at run time.

Function Expression is better than function declaration which is just a floating function 
and can be referred anywhere in the code. So, it’s wise to use function expression with a variable

e.g.,

let a=1;
let b=2;
let add = function(a,b){
 return a+b;
}

