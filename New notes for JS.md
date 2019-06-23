# javascript

# Variables
 Declare variable with 2 variatn:
 1. let str = 'string'; - variable that can be changet
 2. const str = 'string' - this variable cannot be changet.
 Types of variable:
 1. Global - variable outside of any loops/function
 2. Local - variable in loops/function, can't use outside loops/function where was created.
   
## Variable naming
1. First litter must be not a number(digit).
2. Not reserved name(reserved by programming language).
3. The name must contain only letters, digits, or the symbols $ and _.
4. The name should give a description of this variable
        
#  Data types
                                             
There is a 7 different data types name:
1."number" - for number
2."boolean" - true/false
3."string" - for strings
4."symbol" - unique identifiers
5. "object" - complex data structure
6."undefined" - variable without any date or data with undefined value
7."null" - unknown value

when we type let someVariable = null, we clear value of this variable. So null is value with nothing.

There is also 2 form of typeof without any difference "typeof x and typeof(x)"

## Type Conversions
                                   
We can convert value type. Also JS have functions that automatically convert.
If we use for example math methods then variables will be converted to the number if it's possible
```(javascript)
let a = '1';
let b = '3';
console.log(a+b) // result is 4;
```

## Operators
```(javascript)
let sum = a + b;
```
*a* and *b* is an operand(sometimes its called arguments).

An operator is unary if it has a single operand. For example, the unary negation - reverses the sign of a number.
An operator is binary if it has two operands.
 
   Remainder %
 The result of a % b is the remainder of the integer division of a by b.

   Exponentiation **
 For a natural number b, the result of a ** b is a multiplied by itself b times.
2**4 = 16
    Increment/decrement
 Increment ++ increases a variable by 1
 a++ = a+1;

 Decrement -- decreases a variable by 1
 a-- = a-1;

!!! Increment/decrement can only be applied to variables. Trying to use it on a value like 5++ will give an error. !!!

   Bitwise operators:
   1. AND - ( & )
   2. OR - ( | )
   3. XOR  - ( ^ )
   4. NOT = ( ~ )
   5. LEFT SHIFT - ( << )
   6. RIGHT SHIFT - ( >> )
   7. ZERO-FILL RIGHT SHIFT - ( >>> )

   Comma 
   (rare to use)
 The comma operator allows us to evaluate several expressions, dividing them with a comma ,. Each of them is evaluated but only the result of the last one is returned.
2+3,4,5,6, = 8;
## Comparisons
  Comparison type's:
   1. < 
   2. >
   3. =
   4. >=
   5. <=
   6. !=
   7. ===
   8. ==
  When we use 'if', condition was already boolean.
  for example:
  ```(javascript)
  if (condition) {
    ..
  }
  ```
  *condition* - boolean.

# Boolean
true - yes(1) /correct
false - no(0) / wrong

Strings are compared letter-by-letter in the “dictionary” order.

# Interaction: alert, prompt, confirm
all this scripts paused script execution

alert

```(javascript)
 alert(message);
```

*promt* - accepts two arguments, first will show message(before coma) and second will shows an input field.

Sshow a message and paused script until you press "OK"
 It returns the text or, if CANCEL or Esc is clicked, null.

```(javascript)
 result = prompt(title[, default]);
```

*confirm* - show message with two option "OK" and "CANCLE", just for boolean.

```(javascript)
result = confirm(question);
```

#   Conditional operators: if, '?'

## The “if” statement, Boolean conversion, The “else” clause

```(javascript)
if (condition) {
  return true
} else {
  return false;
}
}
```
*condition*  will automaticli convert into boolean

The if statement may contain an optional *else* block. It executes when the condition is false.
Something we can skip *else* :
```(javascript)
if (condition) {
  return true
} 
  return false;
}
```
## Several conditions: “else if”
We can do multiplicate time "else if" if its needed. Same as "else"
```(javascipt)
if (condition){
  ...
} else if(condition2){
  ...
}
}
```

# Ternary operator ‘?’

same as "if, else" but with ternary operator its much simple and shorter.
 Example:
 ```(javascript)
let result = condition ? value1 : value2;
```
# Logical operators

 There are three logical operators in JavaScript: 
 1.   || (OR) -  Getting the first truthy value from a list of variables or expressions.
 2.   && (AND) - If the result isfalse, stops and returns the original value of that operand. If       all operands have been evaluated (i.e. all were truthy),returns the last operand.
 3.   ! (NOT) :
 ```
result = !value;
```
The operator accepts a single argument and does the following:

    Converts the operand to boolean type: true/false.
    Returns the inverse value.

A double NOT !! is sometimes used for converting a value to boolean type:
```
alert( !!"non-empty string" ); // true
alert( !!null ); // false
```
That is, the first NOT converts the value to boolean and returns the inverse, and the second NOT inverses it again. In the end, we have a plain value-to-boolean conversion.

The precedence of NOT ! is the highest of all logical operators, so it always executes first, before && or ||.

### Precedence of AND && is higher than OR ||
So the code a && b || c && d is essentially the same as if the && expressions were in parentheses: (a && b) || (c && d).

  Just like OR, the AND && operator can sometimes replace if.

```(javascript)
 let x = 1;

 (x > 0) && alert( 'Greater than zero!' );
```
The action in the right part of && would execute only if the evaluation reaches it. That is, only if (x > 0) is true.

transform to standart:
```(javascript)
let x = 1;

if (x > 0) {
  alert( 'Greater than zero!' );
}
```

 # Loops: while and for

 We have 3 type of loops:
1. *while* - when condition is checked before each iteration.
  ```(javascript)
  while (condition) {
  // code
  // so-called "loop body"
  ```
2. *do..while* - when condition is checked after each iteration.
   ```(javascript)
   let i = 0;
   do {
    alert( i );
    i++;
   } while (i < 3);
   ```
   Used when you want the body of the loop to execute at least once regardless of the condition being truthy.
3. *for (;;)* - when condition is checked before each iteration, additional settings available.

  ```(javascript)
  for (begin; condition; step) {
  // ... loop body ...
  }
  ```
(if condition true → run body and run step);

 ## Inline variable declaration
 Here, the “counter” variable i is declared right in the loop. This is called an “inline” 
 variable declaration. Such variables are visible only inside the loop.
 Example:
 ```(javascript)
for (let i = 0; i < 3; i++) {
  alert(i); // 0, 1, 2
}
alert(i); // error, no such variable
 ```
 
## Breaking the loop
 We can force the exit at any time using the special break directive.
 ```(javascript)
 let sum = 0;

while (true) {

  let value = +prompt("Enter a number", '');

  if (!value) break; // (*)

  sum += value;

}
alert( 'Sum: ' + sum );
```

 ## Continue to the next iteration
 The continue directive is a “lighter version” of break. It doesn’t stop the whole loop. Instead, it stops the current iteration and forces the loop to start a new one (if the condition allows).

The loop below uses continue to output only odd values:
```(javascript)
for (let i = 0; i < 10; i++) {

  // if true, skip the remaining part of the body
  if (i % 2 == 0) continue;

  alert(i); // 1, then 3, 5, 7, 9
}
```
```(javascript)
for (let i = 0; i < 10; i++) {

  if (i % 2) {
    alert( i );
  }
}
```

## Labels for break/continue
Sometimes we need to break out from multiple nested loops at once.
And for this manipulation we will use "Labels";
Example:
```(javscript)
labelName: for (...) {
  ...
}
```
Exanple in code:
```(javascript)
outer: for (let i = 0; i < 3; i++) {

  for (let j = 0; j < 3; j++) {

    let input = prompt(`Value at coords (${i},${j})`, '');

    // if an empty string or canceled, then break out of both loops
    if (!input) break outer; // (*)

    // do something with the value...
  }
}
alert('Done!');
```
So, break outer will breal general(global) loops from coomand inside of any loops.
Example:
```(javascript)
loop1: for (begin,condition,step) { //first loop
  for (begin,condotion,tep) {       // second loop in the first loop
body                             //body of loop
 if (!body) break loop1;
 do something with the value
  }
}
```
We also can have label into a separate lines:
```(javascipt)
loop1:
for (let i = 0; i < 3; i++) { ... }
```
To make an “infinite” loop, usually the while(true) construct is used. Such a loop, just like any other, can be stopped with the break directive.

If we don’t want to do anything in the current iteration and would like to forward to the next one, we can use the continue directive.


## **The "switch" statement**
A switch statement can replace multiple if checks. It gives a more descriptive way to compare a value with multiple variants:
```(javascript)
switch(x) {
  case 'value1':  // if (x === 'value1')
    ...
    [break]

  case 'value2':  // if (x === 'value2')
    ...
    [break]

  default:
    ...
    [break]
}
```
 If there is no break then the execution continues with the next case without any checks:
  ```(javascript)
     let a = 2 + 2;
     switch (a) {
      case 3:
       alert( 'Too small' );
      case 4:
       alert( 'Exactly!' );
      case 5:
      alert( 'Too big' );
     default:
      alert( "I don't know such values" );
      }
  ```
 So, in this example execution starts from 4(skip 3 because a=4 -> execution start from cas '4'), end we will see 3 results:

   (javascript)
     alert( 'Exactly!' );
     alert( 'Too big' );
     alert( "I don't know such values" );
     ```
    Grouping of “case”
     We can group any cases if they hhave same execution
     Example:
   ```(javascript)   
    let a = 2 + 2;
    switch (a) {
    case 4:
    alert('Right!');
    break;
    case 3:                    // (*) grouped two cases
    case 5:
    alert('Wrong!');
    alert("Why don't you take a math class?");
    break;
    default:
    alert('The result is strange. Really.');
     }
   ```
  So, if we run case 3 and or case 5 we will have same execution.       
  The values must be of the same type to match. If not - then execute 'default'.

# Functions
 Function declaration:

```(Javascript)
function nameFunction(parameters) {
  the function body
}
```
### Local variables
Local variable - variable that created in function and this variable can be used only in this function, outside this function this variable is not working.

### Outer variables
Outer variables - variable created outside of function and can be used at any function(global variable).
Global variables are visible from any function (unless shadowed by locals).
 Usually, a function declares all variables specific to its task. Global variables only store project-level data, and it’s important that these variables are accessible from anywhere. Modern code has few or no globals. Most variables reside in their functions.

 ### Parameters
  We can pass arbitrary data to functions using parameters (also called function arguments) .
  Example:
  ```(javascript)
function showMessage(from, text) { // arguments: from, text
  alert(from + ': ' + text);
}

showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
showMessage('Ann', "What's up?"); // Ann: What's up? (**)
  ```

  ### When the function is called in lines (*) and (**), the given values are copied to local variables from and text. Then the function uses them.


### Returning a value
 A function can return a value back into the calling code as the result:
 ```(javascript)
function sum(a, b) {
  return a + b;
}

let result = sum(1, 2);
alert( result ); // 3
 ```
 Return can be placed in any place, when execution reaches it, the function stops and the value is returned to the calling code.

 We can use return without a value. That causes the function to exit immediately.
 If checkAge(age) returns false, then showMovie won’t proceed to the alert:
```(javascript)
function showMovie(age) {
  if ( !checkAge(age) ) {
    return;
  }

  alert( "Showing you the movie" ); // (*)
  // ...
}
```
### A function with an empty return or without it returns undefined
 ```(javascript)
function doNothing() { /* empty */ }

alert( doNothing() === undefined ); // true
 ```
 An empty return is also the same as return undefined:
```(javascript)
function doNothing() {
  return;
}

alert( doNothing() === undefined ); // true
```
## Function expressions and arrows
Function Declaration:
```(javascript)
function sayHi() {
  alert( "Hello" );
}
```
Function Expression.
```(javascript)
let sayHi = function() {
  alert( "Hello" );
};
```
Copy functions to another variable:

```(javascript)
function sayHi() {   // (1) create
  alert( "Hello" );
}

let func = sayHi;    // (2) copy

func(); // Hello     // (3) run the copy (it works)!
sayHi(); // Hello    //     this still works too (why wouldn't it)
```

What happens:

 The Function Declaration (1) creates the function and puts it into the variable named sayHi.

 Line (2) copies it into the variable func.

There are no parentheses after sayHi. If there were, then func = sayHi() would write the result of the call sayHi() into func, not the function sayHi itself.

 Now the function can be called as both sayHi() and func().
By syntax  Function Expression have a semicolon `;` but Function Declaration does not.

### Callback functions
We’ll write a function ask(question, yes, no) with three parameters:

question
    Text of the question
yes
    Function to run if the answer is “Yes”
no
    Function to run if the answer is “No”

The function should ask the question and, depending on the user’s answer, call yes() or no():

```(javascript)
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

function showOk() {
  alert( "You agreed." );
}

function showCancel() {
  alert( "You canceled the execution." );
}

// usage: functions showOk, showCancel are passed as arguments to ask
ask("Do you agree?", showOk, showCancel);
```
###The arguments of ask are called callback functions or just callbacks.
We can use Function Expressions to write the same function much shorter:
```(javascript)
function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

ask(
  "Do you agree?",
  function() { alert("You agreed."); },
  function() { alert("You canceled the execution."); }
);
```



###A function is a value representing an “action”
Regular values like strings or numbers represent the data.

A function can be perceived as an action.

We can pass it between variables and run when we want.

##Function Expression vs Function Declaration

Function Declaration: a function, declared as a separate statement, in the main code flow.

 
Function Declaration:
```(javascript)
function sum(a, b) {
  return a + b;
}
```

Function Expression: a function, created inside an expression or inside another syntax construct. Here, the function is created at the right side of the “assignment expression” =:

 Function Expression:
```(javascript)
let sum = function(a, b) {
  return a + b;
};
```


A Function Expression is created when the execution reaches it and is usable from then on.

Once the execution flow passes to the right side of the assignment let sum = function… – here we go, the function is created and can be used (assigned, called, etc. ) from now on.

A Function Declaration is usable in the whole script/code block.

And after all of the Function Declarations are processed, the execution goes on.

As a result, a function declared as a Function Declaration can be called earlier than it is defined.

For example, this works:
```(javascript)
sayHi("John"); // Hello, John

function sayHi(name) {
  alert( `Hello, ${name}` );
}
```

The Function Declaration sayHi is created when JavaScript is preparing to start the script and is visible everywhere in it.

…If it was a Function Expression, then it wouldn’t work:

```(javascript)
sayHi("John"); // error!

let sayHi = function(name) {  // (*) no magic any more
  alert( `Hello, ${name}` );
};
```

Function Expressions are created when the execution reaches them. That would happen only in the line (*). Too late.



###When should you choose Function Declaration versus Function Expression?
In general we use Declaration fucntion because it much easy read and we need declare a function. 

### Arrow functions

```(javascript)
let func = (arg1, arg2, ...argN) => expression
```
This creates a function func that has arguments arg1..argN, evaluates the expression on the right side with their use and returns its result.

In other words, it’s roughly the same as:

```(javascript)
let func = function(arg1, arg2, ...argN) {
  return expression;
};
```

```(javascript)
let sum = (a, b) => a + b;

/* The arrow function is a shorter form of:

let sum = function(a, b) {
  return a + b;
};
*/

alert( sum(1, 2) ); // 3
```
If we have only one argument, then parentheses can be omitted, making that even shorter:
```(javascript)
// same as
// let double = function(n) { return n * 2 }
let double = n => n * 2;

alert( double(3) ); // 6
```
If there are no arguments, parentheses should be empty (but they should be present):
```(javascript)
let sayHi = () => alert("Hello!");

sayHi();
```
example arrow function:
```(javascript)
let age = prompt("What is your age?", 18);

let welcome = (age < 18) ?
  () => alert('Hello') :
  () => alert("Greetings!");

welcome(); // ok now
```

### Multiline arrow functions
In multiline arrow function we need use curly braces:
```(javascript)
let sum = (a, b) => {  // the curly brace opens a multiline function
  let result = a + b;
  return result; // if we use curly braces, use return to get results
};

alert( sum(1, 2) ); // 3
```





# Objects

 For creating objects we use {..}, example of empty Objects:

 ```(javascript)
let user = new Object(); // "object constructor" syntax
let user = {};  // "object literal" syntax
```
That declaration is called an object literal.

## Literals and properties

We can immediately put some properties into {...} as “key: value” pairs:

```(javascript)
let user = {     // an object
  name: "John",  // by key "name" store value "John"
  age: 30        // by key "age" store value 30
};
```
For get accesible to value of objects we use dot notation:
```(javascript)
// get fields of the object:
alert( user.name ); // John
alert( user.age ); // 30
```

## Square brackets
For multiword properties, the dot access doesn’t work:

```(javascript)
// this would give a syntax error
user.likes birds = true
```
That’s because the dot requires the key to be a valid variable identifier. That is: no spaces and other limitations.

Square brackets also provide a way to obtain the property name as the result of any expression – as opposed to a literal string – like from a variable as follows:

```(javascript)
let key = "likes birds";

// same as user["likes birds"] = true;
user[key] = true;
```
Example of square brackets:
```(javascript)
let user = {
  name: "John",
  age: 30
};

let key = prompt("What do you want to know about the user?", "name");

// access by variable
alert( user[key] ); // John (if enter "name")
```

## Computed properties
We can use square brackets in an object literal. That’s called computed properties:
```(javascript)
let fruit = prompt("Which fruit to buy?", "apple");

let bag = {
  [fruit]: 5, // the name of the property is taken from the variable fruit
};

alert( bag.apple ); // 5 if fruit="apple"
```
The meaning of a computed property is simple: [fruit] means that the property name should be taken from fruit.

So, if a visitor enters "apple", bag will become {apple: 5}.
Same as:
```(javascript)
let fruit = prompt("Which fruit to buy?", "apple");
let bag = {};

// take property name from the fruit variable
bag[fruit] = 5;
```

We can use more complex expressions inside square brackets:

```(javascript)
let fruit = 'apple';
let bag = {
  [fruit + 'Computers']: 5 // bag.appleComputers = 5
};
```

## Property value shorthand

In real code we often use existing variables as values for property names:
```(javascript)
function makeUser(name, age) {
  return {
    name: name,
    age: age
    // ...other properties
  };
}

let user = makeUser("John", 30);
alert(user.name); // John
```
In the example above, properties have the same names as variables. The use-case of making a property from a variable is so common, that there’s a special property value shorthand to make it shorter.

Instead of name:name we can just write name, like this:
```(javascript)
function makeUser(name, age) {
  return {
    name, // same as name: name
    age   // same as age: age
    // ...
  };
}
```
We can use both normal properties and shorthands in the same object:

```(javascript)
let user = {
  name,  // same as name:name
  age: 30
};
```

## Existence check

A notable objects feature is that it’s possible to access any property. There will be no error if the property doesn’t exist! Accessing a non-existing property just returns undefined. It provides a very common way to test whether the property exists – to get it and compare vs undefined:

```(javascript)
let user = {};

alert( user.noSuchProperty === undefined ); // true means "no such property"
```

There is a special operator to check existence of a property "in" (instead of "... === undefined" ): 
```(javascript)
let user = { name: "John", age: 30 };

alert( "age" in user ); // true, user.age exists
alert( "blabla" in user ); // false, user.blabla doesn't exist
```
On the left side must be a property name. That’s usually a quoted string.
But if we omit quotes then its mean that a variable containing the actual name will be tested.
So if we skip quotes, we will check if on this variable have value that contained on this objects:
```(javascript)
let user = { age: 30 };

let key = "age";
alert( key in user ); // true, takes the name from key and checks for such property
```

## The “for…in” loop
To walk over all keys of an object, there exists a special form of the loop: for..in. This is a completely different thing from the for(;;) construct that we studied before.
The syntax:
```(javascript)
for (key in object) {
  // executes the body for each key among object properties
}
```
Example:
```(javascript)
let user = {
  name: "John",
  age: 30,
  isAdmin: true
};

for (let key in user) {
  // keys
  alert( key );  // name, age, isAdmin
  // values for the keys
  alert( user[key] ); // John, 30, true
}
```
Note that all “for” constructs allow us to declare the looping variable inside the loop, like let key here.

Also, we could use another variable name here instead of key. For instance, "for (let prop in obj)" is also widely used.

## Ordered like an object

Are objects ordered? In other words, if we loop over an object, do we get all properties in the same order they were added? Can we rely on this?

The short answer is: “ordered in a special fashion”: integer properties are sorted, others appear in creation order. The details follow.

```(javascript)
let codes = {
  "49": "Germany",
  "41": "Switzerland",
  "44": "Great Britain",
  // ..,
  "1": "USA"
};

for (let code in codes) {
  alert(code); // 1, 41, 44, 49
}
```
The phone codes go in the ascending sorted order, because they are integers. So we see 1, 41, 44, 49.

### Integer properties? What’s that?
The “integer property” term here means a string that can be converted to-and-from an integer without a change.
```(javascript)
// Math.trunc is a built-in function that removes the decimal part
alert( String(Math.trunc(Number("49"))) ); // "49", same, integer property
alert( String(Math.trunc(Number("+49"))) ); // "49", not same "+49" ⇒ not integer property
alert( String(Math.trunc(Number("1.2"))) ); // "1", not same "1.2" ⇒ not integer property
```
…On the other hand, if the keys are non-integer, then they are listed in the creation order, for instance:

```(javascript)
let user = {
  name: "John",
  surname: "Smith"
};
user.age = 25; // add one more

// non-integer properties are listed in the creation order
for (let prop in user) {
  alert( prop ); // name, surname, age
}
```
So if we add a plus "+" sign before each code it will be not sorted:
```(javascript)
let codes = {
  "+49": "Germany",
  "+41": "Switzerland",
  "+44": "Great Britain",
  // ..,
  "+1": "USA"
};

for (let code in codes) {
  alert( +code ); // 49, 41, 44, 1
}
```

## Copying by reference
One of the fundamental differences of objects vs primitives is that they are stored and copied “by reference”.
Primitive values: strings, numbers, booleans – are assigned/copied “as a whole value”.
So, if we copy variable - it will be save new value. But if we copy object - it will just give acces to this "value" for another object. 
Variable:
Here pharse = "Hello", if we change prhare value - message value are not chage, and we if chage message value - phrase value not changed.
```(javascript)
let message = "Hello!";
let phrase = message;
```
Object:
When an object variable is copied – the reference is copied, the object is not duplicated.
If we imagine an object as a cabinet, then a variable is a key to it. Copying a variable duplicates the key, but not the cabinet itself.

So if we copy object1 to object2 then we just get acces to same value for object1 and object2, and if we change sometihng in object1 it will be changed in object2 also.
```(javascript)
let user = { name: 'John' };

let admin = user;

admin.name = 'Pete'; // changed by the "admin" reference

alert(user.name); // 'Pete', changes are seen from the "user" reference
```
The example above demonstrates that there is only one object. As if we had a cabinet with two keys and used one of them (admin) to get into it. Then, if we later use the other key (user) we would see changes.

It means that we have only one object with 2 different name and with one common value.



## Comparison by reference

The equality == and strict equality === operators for objects work exactly the same.

Two objects are equal only if they are the same object.

For instance, two variables reference the same object, they are equal:

```(javascript)
let a = {};
let b = a; // copy the reference

alert( a == b ); // true, both variables reference the same object
alert( a === b ); // true
```

And here two independent objects are not equal, even though both are empty:

```(javascript)
let a = {};
let b = {}; // two independent objects

alert( a == b ); // false
```

For comparisons like obj1 > obj2 or for a comparison against a primitive obj == 5, objects are converted to primitives. We’ll study how object conversions work very soon, but to tell the truth, such comparisons are necessary very rarely and usually are a result of a coding mistake.


## Const object
An object declared as const can be changed.

```(javascript)
const user = {
  name: "John"
};

user.age = 25; // (*)

alert(user.age); // 25
```
It's not error, because we dont change any property of user, we just add new. 
But if we try change - we will see error:
```(javascript)
const user = {
  name: "John"
};

// Error (can't reassign user)
user = {
  name: "Pete"
};
```

## Cloning and merging, Object.assign
Somethimes we need copy object with all properies instead of a just link.
Need to create new object and then copy property from another onbject:
```(javascript)
let user = {
  name: "John",
  age: 30
};

let clone = {}; // the new empty object

// let's copy all user properties into it
for (let key in user) {
  clone[key] = user[key];
}

// now clone is a fully independent clone
clone.name = "Pete"; // changed the data in it

alert( user.name ); // still John in the original object
```
Also we can use the method Object.assign for that.

The syntax is:

```(javascript)
Object.assign(dest[, src1, src2, src3...])
```
Arguments dest, and src1, ..., srcN (can be as many as needed) are objects.
It copies the properties of all objects src1, ..., srcN into dest. In other words, properties of all arguments starting from the 2nd are copied into the 1st. Then it returns dest.

For instance, we can use it to merge several objects into one:
```(javascript)
let user = { name: "John" };

let permissions1 = { canView: true };
let permissions2 = { canEdit: true };

// copies all properties from permissions1 and permissions2 into user
Object.assign(user, permissions1, permissions2);

// now user = { name: "John", canView: true, canEdit: true }
```
If the receiving object (user) already has the same named property, it will be overwritten:

```(javascript)
let user = { name: "John" };

// overwrite name, add isAdmin
Object.assign(user, { name: "Pete", isAdmin: true });

// now user = { name: "Pete", isAdmin: true }
```

We also can use Object.assign to replace the loop for simple cloning:

```(javascript)
let user = {
  name: "John",
  age: 30
};

let clone = Object.assign({}, user);
```
It copies all properties of user into the empty object and returns it. Actually, the same as the loop, but shorter.

Now it’s not enough to copy clone.sizes = user.sizes, because the user.sizes is an object, it will be copied by reference. So clone and user will share the same sizes:
```(javascript)
let user = {
  name: "John",
  sizes: {
    height: 182,
    width: 50
  }
};

let clone = Object.assign({}, user);

alert( user.sizes === clone.sizes ); // true, same object

// user and clone share sizes
user.sizes.width++;       // change a property from one place
alert(clone.sizes.width); // 51, see the result from the other one
```
To fix that, we should use the cloning loop that examines each value of user[key] and, if it’s an object, then replicate its structure as well. That is called a “deep cloning”.

There’s a standard algorithm for deep cloning that handles the case above and more complex cases, called the Structured cloning algorithm. In order not to reinvent the wheel, we can use a working implementation of it from the JavaScript library lodash, the method is called _.cloneDeep(obj).

### Summary of objects
To access a property, we can use:
The dot notation: obj.property.
Square brackets notation obj["property"]. Square brackets allow to take the key from a variable, like obj[varWithKey].
Additional operators:
To delete a property: delete obj.prop.
To check if a property with the given key exists: "key" in obj.
To iterate over an object: for (let key in obj) loop.

To make a “real copy” (a clone) we can use Object.assign or _.cloneDeep(obj).


# Garbage collection
  Javascript have garbage collection. Simple example:
  ```(javascript)
  let user = {
  name: "John"
};
```
  If we delete user, then proparty name will be also automatical deleted.


~~!!!(need create note ablut Symbol() ) #Symbol
  Symbol is a primitive tupe for unique identifiers and created by Sybmol() with an optional description.
  Symbols don’t auto-convert to a string 
  ```(javascript)
  let id = Symbol("id");
  alert(id); // TypeError: Cannot convert a Symbol value to a string
  ```



 # Object methods, *this*
  If functino stored in the object it's called method.

  Methods allow objects to “act” like object.doSomething().

  Methods can reference the object as this.

  When a function is called in the “method” syntax: object.method(), the value of this during the call is object.

  Arrow functions are special: they have no this. When this is accessed inside an arrow function, it is taken from outside.


  To access the object, a method we can use the *this* keyword.
  Example:
  ```(javascript)
  let user = {
  name: "John",
  age: 30,

  sayHi() {
    alert(this.name);
  }
 };
 user.sayHi(); // John
  ```
  So *this* call the mail/global name of the object/etc.. .
 We use *this* becase name of variable can be changed while machine do our code, that's why we prefer to use *this*.

## **this* is not bound
  One function can have different *this* :
  ```(javascript)
let user = { name: "John" };
let admin = { name: "Admin" };

function sayHi() {
  alert( this.name );
}

// use the same functions in two objects
user.f = sayHi;
admin.f = sayHi;

// these calls have different this
// "this" inside the function is the object "before the dot"
user.f(); // John  (this == user)
admin.f(); // Admin  (this == admin)

admin['f'](); // Admin (dot or square brackets access the method – doesn't matter)
  ```
  also, we can call function without an object:
  ```(javascript)
function sayHi() {
  alert(this);
}

sayHi(); // undefined
  ```