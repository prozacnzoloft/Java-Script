
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

  
JavaScript has several built-in data types, which can be grouped into two main categories: primitive data types and reference data types.

#### Primitive data types:

 String: a set of characters (e.g. "Hello World").
 
 Number: a numerical value (e.g. 42 or 3.14).
 
Boolean: a value that can either be true or false.

Undefined: a value that represents a variable that has been declared but has not been assigned a value.

Null: a special value that represents the intentional absence of any object value.

#### Reference data types:

Object: a collection of key-value pairs, used to store data.

Array: an ordered list of values, represented by square brackets (e.g. [1, 2, 3]).
Function: a block of code that performs a specific task and can be called multiple times.

Symbol: a new data type in ECMAScript 6 (ES6) that is used to create unique values that are not equal to any other value.

Note that the type of a value in JavaScript can be determined using the typeof operator.

##### Object:
JavaScript objects are a fundamental data type in the language and can be thought of as collections of key-value pairs. The keys are strings, and the values can be any type of data (numbers, strings, arrays, other objects, etc.)

Example:
   

     let person = {
    	      name: "Nawadit Sharma",
    		    age: 19,
          job: "software engineer",
          hobbies: ["reading", "traveling", "coding"],
          address: {
            street: "Campus Road",
            city: "Tansen",
            state: "Lumbini"
          }
        };
    <hr>
   To access the values stored in an object, you can use dot notation or square bracket notation.
   Example:

       console.log(person.name);
       console.log(person[name]);
       console.log(person[hobbies[1]]);
Above example will result in `John Doe` `John Doe` `reading`

Accessing elements of and object using [ ] did'nt work. 
<hr>
