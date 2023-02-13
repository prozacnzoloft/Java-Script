
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

## Data Types

  
JavaScript has several built-in data types, which can be grouped into two main categories: primitive data types and reference data types.

### Primitive data types:

 String: a set of characters (e.g. "Hello World").
 
 Number: a numerical value (e.g. 42 or 3.14).
 
Boolean: a value that can either be true or false.

Undefined: a value that represents a variable that has been declared but has not been assigned a value.

Null: a special value that represents the intentional absence of any object value.
<hr>

### Reference data types:

Object: a collection of key-value pairs, used to store data.

Array: an ordered list of values, represented by square brackets (e.g. [1, 2, 3]).
Function: a block of code that performs a specific task and can be called multiple times.

Symbol: a new data type in ECMAScript 6 (ES6) that is used to create unique values that are not equal to any other value.

Note that the type of a value in JavaScript can be determined using the typeof operator.
<hr>

#### Object:
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
Above example will result in `Nawadit Sharma` `Nawadit Sharma` `reading`

Accessing elements of and object using [ ] did'nt work. 
<hr>

#### Built-in Objects
JavaScript has several built-in objects that provide common functionality and make it easier to work with different types of data. A few of the most commonly used built-in objects are `string`, `array`, `number`, `math`, `date`.
##### String
`String`: Represents a sequence of characters. For example, you can use the `length` property to get the number of characters in a string, or the `toUpperCase` method to convert a string to all uppercase characters.

Example:

    let name = "Nawadit Sharma";
    console.log(name.length);
    console.log(name.toUpperCase());
This code will return `14` `NAWADIT SHARMA` 	to console
<hr>

##### Array

`Array`: Represents a collection of values that can be of any type. Arrays are zero-indexed, meaning the first item has an index of 0. You can use the `length` property to get the number of items in an array, and the square bracket notation (e.g. `array[index]`) to access specific items.
Example:

    let hobbies = ["reading", "traveling", "coding"];
    console.log(hobbies.length);
    console.log(hobbies[1]);
   This will return `3` `traveling` in console.
   <hr>
   
  ###### Number
  `Number`: Represents a numeric value. You can use the built-in methods of the `Number` object to perform mathematical operations, such as rounding or converting a number to a string.
  Example:

    let num = 123.456;
    console.log(num.toFixed(2)); // "123.46"
    console.log(num.toString()); // "123.456"
   This will return `123.46` `124.56` to console.
  <hr>
  
  ##### Math
  `Math`: Provides mathematical functions and constants, such as trigonometric functions, exponential functions, and `PI`.
  Example:

    console.log(Math.PI); 
    console.log(Math.sin(Math.PI / 2));
    console.log(Math.exp(1));
   This code will return `3.141592653589793` `1`  `2.718281828459045` to console.
   <hr>
   
   ##### Date
   `Date`: Represents a specific date and time. You can use the `Date` object to get the current date and time, format dates as strings, and perform date arithmetic.
   Example:
 

    let now = new Date();
    console.log(now); // "
    console.log(now.getFullYear()); // 2023
    console.log(now.toDateString()); // 
   This will return `Mon Feb 13 2023 18:11:21 GMT+0545 (Nepal Time)` `2023` `25 Mon Feb 13 2023` on console.
   
These are just a few of the many built-in objects in JavaScript. Understanding these objects and how to use them can make your JavaScript code more efficient and easier to write and maintain.
   <hr>
   
   ## Type casting
Type casting in JavaScript refers to the process of converting a value from one data type to another. JavaScript is a loosely typed language, meaning that the data type of a variable can change dynamically at runtime. However, sometimes you may need to explicitly convert a value to a different type. Some methods we use to do this are: `Number()` `String()` `Boolean()` `Parsenum()` `Parsefloat()` 
### Number() 
It converts data into number if possible or into NaN if not.
Example:

    let num = Number("123");
    console.log(typeof num);
    console.log(num);
    
    let str = Number("abc");
    console.log(typeof str);
    console.log(str);
  This code will return `number` `123` `number` `NaN`
  <hr>
  
  ### String
  It converts a value into string type.
  Example:

     let num = 123;
    console.log(typeof String(num));
    console.log(String(num));
    
    let bool = true;
    console.log(typeof String(bool));
    console.log(String(bool));
This code will return `string` `123` `string` `true` .
<hr>

### Boolean()
It converts a value into boolean type.
Example:

    let num = 0;
    console.log(typeof Boolean(num));
    console.log(Boolean(num));
    
    let str = "";
    let strr = "sdkfa";
    
    console.log(typeof Boolean(str));
    console.log(Boolean(str));
    
    console.log(typeof Boolean(strr));
    console.log(Boolean(strr));
   This code will return `boolean` `false` `boolean` `false` `boolean` `true`.
<hr>

### Parseint() and Parsefloat()
`parseInt()` and `parseFloat()`: Converts a string to a `Number` type, with `parseInt` only returning an integer and `parseFloat` allowing for decimal values.
Example

    let num = parseInt("123");
    console.log(typeof num);
    console.log(num);
    
    let decimal = parseFloat("123.456");
    console.log(typeof decimal);
    console.log(decimal);
   This code will return number `123` `123.456` `number` `123.456`.
   <hr>
   

