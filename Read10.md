#  JS Debugging
how to find the errors in your code. It will also teach you how to write scripts that deal with potential errors gracefully.

* THE CONSOLE & DEV TOOLS Tools  
   built into the browser that help you hunt for errors.

* COMMON PROBLEMS
Common sources of errors, and how to solve them

 * HANDLING ERRORS How code can deal with potential errors gra cefully

 ### ORDER OF EXECUTION 

 To find the source of an error, it helps to know how scripts are processed. 
 The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run:

  ### EXECUTION CONTEXTS 

  The JavaScript interpreter uses the concept of execution contexts. 
  There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope.

  ## The stak
  EXECUTION CONTEXT & HOISTING
  every time script enters new execution its throw in to phases of activuty
  * prepare 
  * excute  
  how to under stand the scop 
  In the interpreter, each execution context has its own va ri ables object.
*It holds the variables, functions, and parameters available within it*

#### If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.

Eror obje
**Error objects can help you find where your mistakes are and browsers have tools to help you read them.**

* Syntax Error
* Ref erenceError
* EvalError
* URI Error
* Type Error
* RangeError
* NaN
* Error