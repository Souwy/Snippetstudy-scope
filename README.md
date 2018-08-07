# Snippetstudy-scope-hoisted

## Description
This is about knowing the differences between visible, declared, defined, hoisted 

<!---
personal note: use ctrl+f and lookup "continued" to find where you haven't finish.
-->

## Learning objectives (keywords)
* Visible
* Declared and defined
* Hoisting

## Code snippet #1
```js
var x = 5; // Initialize x

console.log(y)

let y = 7; // Initialize y
```
Here, I receive an error that y is NOT DEFINED (>< undefined!) because I ask JS to print (console.log). but y is located AFTER I apply ```.log``` method to my variable ```console```.


## Code snippet #2
var x = 5; // Initialize x

console.log(y)

let y = 7; // Initialize y
## Study Links
[repl.it](https://repl.it/@colevandersWands/primitive-types)  
[pytut](https://goo.gl/QahvNv)  
[debugger](https://www.w3schools.com/code/tryit.asp?filename=FU1BIF6VJMS4)  
sketches : insert img here l8ter _to be continued_

## Vocabulary

### JS Scopte and hoisting
Visible:   
Declared:   
Defined:   
Hoisted:   

### Misc
Initialize: to declare and define a variable.   
Declare: to tell the console that the variable is there, but the value is not defined yet (therefore it is set to undefined).   
Assign: to add a value to a variable.   

## Review
* Struggles: 
  * how the value "number", which is already a string, becomes "string" after the operator "typeof" is executed.
  * hoisting.
* Learning objectives that need extra work?   
  value, type
  difference between primitive type and operators
* next steps: 
  * hoisting
  * [block-scope-let-vs-var](https://github.com/elewa-academy/block-scope-let-vs-var#index)
  * 12345-345
  


