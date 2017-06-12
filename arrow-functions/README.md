# Arrow Functions

## Overview :
> Arrow functions are basically using `=>` to write functions in a more concise
way. Arrow functions are anonymous and change the way `this` binds in functions.

## Usage :

Let there be a function which adds `Double` in front of each of it's arguments.   

``` Javascript
const toppings = ['tomato', 'chicken', 'ham'];

// A normal function to add "Double to all toppings"
const doubleToppings = toppings.map(function(topping){
  return "Double "+topping;
})
```

### Various ways to implement arrow functions are as follow :

``` Javascript
const arrowDouble = toppings.map((topping) =>{
  return "Double "+topping;
})
```

#### Since there is a single argument being passed we can also write the above as :    

``` Javascript
const arrowDouble = toppings.map(topping =>{
  return "Double "+topping;
})
```

#### This is an implicit return implementation :     

``` Javascript
const arrowDouble = toppings.map((topping) =>"Double "+topping;)
```

#### If there are no arguments for some function, Then :    

``` Javascript
const arrowDouble = toppings.map(() =>{
  return " Everything Double";
})
```

### NOTE : Arrow functions are always Anonymous. ALWAYS.
![anonymous](anonymous.jpg)

-------------------------

## Arrow Functions and `this`

In previous versions of JS every function scope had it's own definition of this, which was not so convinient for OOP.    
In ECMA3/5, it was closed by assigning the value of `this` to a variable.    
An arrow function does not create its own `this` context, so this has its original meaning from the enclosing context
