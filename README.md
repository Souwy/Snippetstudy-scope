# Snippetstudy_scope

## Description
This is about knowing the differences between visible, declared, defined. these concepts are closely related to the concept of hoisting.

<!---
personal note: use ctrl+f and lookup "continued" to find where you haven't finish.
-->
   
## Learning objectives (keywords)
* Visible
* Declared and defined
* Intro to the concept of hoisting
   
## Code snippet #1
```js
var x = 5; // Initialize x

console.log(y)

let y = 7; // Initialize y
```
[PythonTutor #1](https://goo.gl/VB7nJr)   
   
Here, I receive an error that y is NOT DEFINED (>< undefined!) because I ask JS to print (console.log). but y is located AFTER I apply ```.log``` method to my variable ```console```. That is because let is not a variable that is hoisted by JS console.   
   
Hoisting is "JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function)." (W3 Schools)
   
Variable ``let`` and ``const`` are not hoisted. ``var``and ``function``are hoisted. Now, we add the concepts of visible, declared and defined to this.
   
## Code snippet #2 (var)
```js
innerer_var = 'defined';

{
   innerer_var = 2;
  {
    var innerer_var;
  }
}
```
[PythonTutor #2](https://goo.gl/LVz4Nd)   
   
For the concept of scope (defined, declared, and visible), we need to look somewhere in particular: the "memory" of the JS console. On PythonTutor, this is the board that is on the right (Frames and Object). after each lines, it updates the variables and values (if there's any updates to do) that is kept in the Console memory (it does not keep track of the modifications! only takes and memorize the last update).
   
1. JS declares "innerer_var" and hoists it to the global scope. It is now visible in all other scopes.   
2. JS defines "innerer_var" as (String, defined).   
>Inside Block 1, JS defines "innerer_var" as (Number, 2)   
>Inside Block 2, JS reaches the statement where "innerer_var" was declared. But it was already declared in the creation phase, so there's nothing to do.   
3. Final state. "innerer_var" is still visible at the global scope, with final value {Number, 2}   
   
## Code snippet #3 (let)
```js
let outer_let = 'defined';

{
   let inner_let = 2;
  {
    let innerer_let;
  }
}
```
[PythonTutor #3](https://goo.gl/dNXg2k)   
   
1. Nothing happens in the creation phase, there are no "var" variables or functions to hoist.   
2. JS declares & defines "outer_let" in a single statement.   
3. The new block scope is created, with "inner_let" declared but in the temporal dead zone.   
>"inner_let" is defined as "block 1". Both "outer_let" and "inner_let" are visible in the block scope.   
4. The second block scope is created, with "innerer_let" declared but in the temporal dead zone.   
>"innerer_let" is defined as "block 2". Both "inner_let" and "innerer_let" are visible in the block scope.   
5. Both block scopes are destroyed, "inner_let" and "innerer_let" no longer exist.   
6. Final state. "outer_let" is still there, it was declared in the global scope. "inner_let" is no longer there, it was declared in the block scope and was not hoisted, same with "innerer_let".   
   
## Code snippet #4 (Temporal Dead Zone)
```js
console.log(aVar); // undefined
console.log(aLet); // causes ReferenceError: aLet is not defined
var aVar = 1;
let aLet = 2;
```
- let and const have two broad differences from var:
  - They are block scoped.
  - Accessing a var before it is declared has the result undefined; accessing a let or const before it is declared throws ReferenceError:
- It appears from these examples that let declarations (and const, which works the same way) may not be hoisted, since aLet does not appear to exist before it is assigned a value.
- That is not the case, however—let and const are hoisted (like var, class and function), but there is a period between entering scope and being declared where they cannot be accessed.
   
## Helpful links
[repl.it](https://repl.it/@colevandersWands/primitive-types)  
[PythonTutor](https://goo.gl/QahvNv)  
[debugger](https://www.w3schools.com/code/tryit.asp?filename=FU1BIF6VJMS4)  
sketches : insert img here l8ter _to be continued_
[W3 Schools hoisting](https://www.w3schools.com/js/js_hoisting.asp)
   
## Vocabulary
- Visible:   
- Declared:   
- Defined:   
- Hoisted:   
- Creation phase: What happens before the first line is executed. Mostly just hoisting. You can see what happened in the creation phase, it's what PythonTutor displays before you click the forward button for the first time.   
- Execution phase: Everything that happens after the creation phase.   
 
Initialize: to declare and define a variable.   
Declare: to tell the console that the variable is there, but the value is not defined yet (therefore it is set to undefined).   
Assign: to add a value to a variable.   

## Review
* Struggles: 

* Learning objectives that need extra work?   

* next steps: 

  


