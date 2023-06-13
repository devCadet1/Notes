
# `Hoisting` in JavaScript - 


## What is Hoisting? 
<br>

> ## Hoisting in JavaScript is a default behaviour of moving all declarations to the top of the current scope (to the top of the current script or the current function)
>
> ## JavaScript declarations are Hoisted:
- ### In JavaScript, a variable can be declared after it has been used.
- ### In other words, a variable can be used before it has been declared.

```js
// for eg - 
// using test before declaring

console.log(test);
var test;

// Output
undefined
```

## The above program works and the output will be undefined because the ```var test``` is only declared and has no value, so undefined value is assigned to it.


<br> 
<br>

# Variable Hoisting:

>## In JavaScript, ```var``` is hoisted and ```let``` and ```const``` does not allow hoisting.

```js
// for eg -

a = 10;
console.log(a);
var a;

// output
10
```

## In the above example, ``` var a``` is used before declaring it. And the program works and displays the output 5.


<br>
<br>

# ```let``` does not allow Hoisting : 
> ## While using ```let``` , the  variable must be declared first otherwise it will throw error.

```js
// for eg -

a = 10;
console.log(a);
let a;

// Output
Uncaught ReferenceError: Cannot access 'a' before initialization
```

<br>
<br>

# Initializations are not Hoisted :
> ## In JavaScript initializations are not hoisted.
 
```js
// for eg - 
console.log(a);
var a = 10;

// Output
undefined
```

## Only the declaration is moved to the memory in the compile phase. Hence the value of ```var a``` is undefined because `a` is printed without initializing it.

<br>
<br>

> # Conclusion: 
>- ## Hoisting is an unknown or overlooked behaviour of JavaScript.
>- ## If a developer doesn't understand `Hoisting`, programs may contain bugs and errors.
>- ## To avoid bugs, always  declare all variables at the beginning of every scope.
>- ## This is how JavaScript interprets the code so it is always a good rule to use `Hoisting`
   
 

 

