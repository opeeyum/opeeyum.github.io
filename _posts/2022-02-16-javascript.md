---
layout: template
author: Omprakash
date: 2022-02-16
category: cheatsheets

sidebar:
  - name: Comments
    key: comments
  - name: Data Types
    key: data-types
  - name: Variable Declaration
    key: variable-declaration
  - name: Arrays
    key: array-in-js
  - name: Functions
    key: functions-in-js
  - name: == / ===
    key: what-is--in-javascript
  - name: Conditonal Operators
    key: if-else-in-js
  - name: Loops
    key: loops
  - name: Random Numbers
    key: random-numbers
  - name: Ternary Operator
    key: ternary-operator
---
# Getting started with Javascript

### Comments 
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
// Single line comment or Inline comment

/* Multiline comment like C or CPP */
```
</div>
 
### Display Output
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
console.log("Hello World");
```
</div>

### Data Types
- undefined
- null
- boolean
- string
- symbol
- number
- object.

### Object datatype
 It is similar to dictionary in python.
 Has function `hasOwnProperty()` to check whether particular key exists in the **Object** or not.

<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
``` 
const my_dict = {
    "key 1": value,
    key: "value 2",
}; 
```
</div>

### Variable declaration
There are three ways to declare a variable.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
var myname = "Op";
let ourName = "Limited Scope";
```
</div>


- Variable declaration using `let`:

  Using `let` enables us **not to** override any variable within a **given scope**. 
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
let var_1 = "op";
let var_1 = "lol";
```
</div>

  It will raise an error, because we are trying to override the `var_1`, have local scope.

`NOTE: Variable declared with **var"** and **let** can have global or local scope.`

- Variable declaration using `const`:

  Value of variable declared with `const` can't be changed.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
const pi = 3.14;
```
</div>

### Array in JS
- Arrays are created using `const` keyword.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
const myArray = [1, 2, 3]
const multDimArray = [[1, 2, 3], [4, 5, 8]]
```
</div>

- Array have length function to get the length of an array
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
console.log(myArray.length) // without parenthesis
```
</div>
- Various other array functions:
- `push()` - push is used to append element at end in an array.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
myArray.push(1) 
```
</div>

- `pop()` - pop is used to pop element from end in an array.
- `shift()` - shift is used to pop first element from the array.
- `unshift()` - unshift is used to add element at the begining in an array.

### Function's in JS
 Functions are decalared as following:
 <div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
function myFunc(para1, para2)
{
    //body
}
```
</div>

### What is `==` in JavaScript?
- Double equals (==) is a comparison operator, which transforms the operands having the same type before comparison.
- So, when you compare string with a number, JavaScript converts any string to a number. 
- An empty string is always converts to zero. 
- A string with no numeric value is converts to NaN (Not a Number), which returns false.

### What is `===` in JavaScript?
- `===` - **Triple equals**, is a STRICT EQUALITY comparison operator in JavaScript, which returns false for the values which are not of a similar type. 
- This operator performs type casting for equality. 
- If we compare 2 with “2” using ===, then it will return a false value.

### If Else in JS
- Exactly similar to C or CPP
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
if(condition)
{
    //Body
}
else if(condtion)
{
    //Body
}
else
{
    //Body
}  
```
</div>

### Switch Case
- Exactly similar to C or CPP
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
switch(1)
{
    case 1: ;
    case 2: ;
    default: ;
}
```
</div>

### Loops
- Java script supports all loops (i.e for, while, and do while) having functionalty same as c/c++.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
for(var i=0; i<10; i++)
{
    //Body
}
```
</div>
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
while(condition)
{
    //Body
}
```
</div>
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
do
{
    //Body
}
while(condition);
```
</div>

### Random Numbers
- Javascript has `Math.random()` function that genrates decimal random numbers between [0, 1).
- It also has `Math.floor()` function to get the floor value of an decimal number.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
// To generate random number within specified range
Math.floor(Math.random()*(max-min+1))+min;
```
</div>

- The `parseInt()` function parses a string and returns an integer. 
- It takes a second argument for the radix, which specifies the base of the number in the string.
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
const a = parseInt("11", 2);
//This example converts the string 11 to an integer 3
```
</div>
The radix variable says that 11 is in the binary system, or base 2.

### Ternary Operator
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
function findGreaterOrEqual(a, b) {
    if (a === b) {
      return "a and b are equal";
    }
    else if (a > b) {
      return "a is greater";
    }
    else {
      return "b is greater";
    }
  }
```
</div>
The above function can be re-written using multiple conditional operators:
<div class="bg-dark bg-gradient text-white mb-3 p-2" markdown=1>
```
function findGreaterOrEqual(a, b) {
    return (a === b) ? "a and b are equal" 
      : (a > b) ? "a is greater" 
      : "b is greater";
}
```
</div>
It is considered best practice to format multiple conditional operators such that each condition is on a separate line, as shown above.