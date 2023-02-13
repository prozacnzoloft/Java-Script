
## History and Introduction

JavaScript is a high-level, interpreted programming language that is widely used for web development. It was created in 1995 by Brendan Eich while he was working at Netscape Communications Corporation. The initial purpose of JavaScript was to add interactivity to web pages, such as form validation, dynamic content updates, and creating animations.

JavaScript quickly became popular and was standardized in 1997 by the European Computer Manufacturers Association (ECMA) as ECMAScript. Today, JavaScript is supported by all modern web browsers and is used not only for client-side web development but also for server-side programming through technologies such as Node.js.

JavaScript has become one of the most important and widely used programming languages in the world and is an essential tool for front-end web developers. It has a rich set of libraries and frameworks, such as React, Angular, and Vue, that make it easier for developers to build complex, interactive web applications.

## About variables

### Variable declaration

In JS variable can be declared using var, let and const keywords. `const` stands for constant meaning once you initialize the variable, it’s value cannot be changed. `var` and `let` function almost identically. Emphasis on almost because they are different, we just don’t discuss those differences now.

### Variable naming rules

First character of name must be a letter $ or _

You cannot use reserve key words as name

You cannot use operation signs

### Hoisting

Hoisting is the process whereby the interpreter appears to have moved the declaration of function and variables (var) to the top of their scope.

Hoisting doesn’t work on function expressions, let or const

Examples

    greet();
    
    function greet(){
    
    console.log(“Hello”)
    
    }

This will return “hello” in console
<hr>

    console.log(a)
    
    var a;

This will return “undefined” in console
<hr>

    Console.log(a)
    
    let a = 0;

This will give an error
<hr>

    greet();
    
    const greet = function (){
    
    console.log(“Hello”)
    
    }
    
This will give an error
<hr>

### Variable Scope

In JS there are three variable scopes, block, function and global.

Block: `let` is an example of block scope variable. This mean a variable initialized using `let` can only be used with in the curly braces {} they are initialized in. They are used in loops.

Example:

    {let a = 9}
    
    console.log(a)


This will return an error
<hr>

    {let a = 9
    
    console.log(a)}

This will return `9` in console.
<hr>

Function: Variable declared within a function can only be used within that function.

Example

        function greet(){  
        var a = “hello”
        
        console.log(a)
        
        }
    
    console.log(a)

This will return `hello` and then an error in console.
<hr>

Global: Variable declared outside curly braces and functions can be used anywhere in a program.

Example:

    var a = “hello”
    
    function greet(){  
    console.log(a)
    
    }
    
    console.log(a)

This will return `hello` `hello` in console.
<hr>

### Data Types
#### Primitive
Number, String, Boolean, Null, Undefined, BigInt

#### Non-Primitive
Objects, Arrays 
