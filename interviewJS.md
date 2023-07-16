# JavaScript Interview ques&ans

## Q1 What is a 'typeof' operator? 
- JavaScript provides a 'typeof' operator that can examine a value and can tell you what type it is.
```js
var a;
typeof a;       // undefined

a = "hello world";
typeof a;       // "string"

a = "42"
typeof a;       // "number"

a = {b: 'c'}
typeof a;       // "object"
```

## Q2 What is equality in JavaScript? 
 - JavaScript has two types of comparisons
 ```js
 1. == Abstract comparison -(Checks for value equality only)
 2. === Strict comparison -(Checks for value quality without allowing coercion)

//  Type Coercion refers to the process of automatic or implicit conversion of values from one data type to another. 
 ```

 ## Q3 Explain Scope in JavaScript
  - JavaScript has 3 types of Scope
    - Block
    - Function 
    - Global

### Block scope
>  ### ES6 introduced two important new JS keywords ```let ``` and ```const```
> These two keywords provide Block Scope in JavaScript.
>Variables declared inside a ```{}``` block cannot be accessed from outside the block.
```js
eg-

{
    let x = 2;
}
console.log(x);     // x CANNOT be used here  
```

> Variables declared with the ```var``` keyword cannot have block scope .  
>Variables declared inside a ```{}``` block can be accessed from outside the block.

```js
{
    var x = 2;
}
console.log(x)      // x CAN be used here
```
# 
### Local scope
> Variables declared within a JavaScript ```function```, become LOCAL to the function.

```js
eg-
// code here CANNOT use carName

function myFunction() {
    let carName = "Volvo";
    // code here CAN use carName
}

// code here CANNOT use carName
```
> - local variables have function scope.They can only be accessed from within a funciton.
> - Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.
> - Local variables sare created when a funciton starts, and deleted when the function is completed.

#

### Function scope
> JavaScript has function scope: Each function creates a new scope.
> Variables defined inside a function are not accessible from outside that function.
> Variables declared with ```var, let ```and``` const``` are quite similar when declared inside a function

```js 
// They all have Function scope

function myFunction() {
    var carName = "Volvo";      //Function scope
}

function myFunction() {
    let carName = "Volvo";      //Function scope
}

function myFunction() {
    const carName = "Volvo";      //Function scope
}
```

#

### Global Scope
> A variablde declared outside a function becomes Global

```js
eg- 
let carName = "Volvo";
// code here can use carName

function myFunction(){
    // code here can also use carName
}

```

>- A global variable has Global Scope
>- All scripts and functions on a web page can access it.
> - Variables declared with ```var , let ``` and ```const ```are quite similar when declared outside a block.
