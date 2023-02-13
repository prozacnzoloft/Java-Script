
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
Example:

    let num = parseInt("123");
    console.log(typeof num);
    console.log(num);
    
    let decimal = parseFloat("123.456");
    console.log(typeof decimal);
    console.log(decimal);
   This code will return number `123` `123.456` `number` `123.456`.
   <hr>
   
   
#### Difference between type conversion and type coercion.
`Type conversion` and `type coercion` in JavaScript refer to the process of converting a value from one data type to another. The main difference between the two is that type conversion is an explicit operation, while type coercion is an implicit operation.
### Data structures
JavaScript has several built-in data structures that can be used to store and organize data. These include `arrays`, `objects`, `maps`, `sets`. 
#### Structured data
Structured data in JavaScript refers to data that is organized in a specific, predefined format. It can be used to represent and manipulate complex data structures such as arrays, objects, and tables. The format of structured data in JavaScript is often defined using JSON.
#### JSON 
JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. It is based on a subset of the JavaScript programming language and is often used to transmit data over a network for which we first need to stringify this data structure in a string, but the string will be of a fixed format so that it can again be changed into the data structure. We use JSON.stringify() and JSON.prase() to convert data to and from string in Java Script.
Example

    obj = {
    firstName = "Nawadit",
    rollNo = 11
    };
    console.log(obj)
    let myString = JSON.stringify(obj)
    console.log(myString)
    obj2 =  JSON.parse(myString)
    console.log(obj2);
   This will return
    `ObjectfirstName: "Nawadit"rollNo: 11[[Prototype]]: Object` 	
    `{"firstName":"Nawadit","rollNo":11}`
	`ObjectfirstName: "Nawadit"rollNo: 11[[Prototype]]: Object` 
    to the console.
#### Indexed Collection
An indexed collection in JavaScript is a data structure that allows you to store and access elements using an index or key. The two main types of indexed collections in JavaScript are `arrays` and `objects`.
##### Arrays
Arrays are a type of indexed collection in which data can be accessed using a numeric index.
Example

    var array=[1, 2, 3, "a", "b", "c", true]
    console.log(array[3], typeof array[3], array[1], typeof array[1], array[6], typeof array[6])
   This will return `a` `string` `2` `number` `true` `boolean`
   Array itself is an object type data.

### Equality Comparators
To compare if two values are equal with one another we need equality comparators. In JS we use `==` `===` or `Object.is` to compare values of different data types.
<hr>
Difference between `==` and `===` is illustrated by code below

    console.log(2==2)
    console.log(2=="2")
    console.log(false=="0")
    console.log(0="")
    console.log("break")
    console.log(2===2)
    console.log(2==="2")
    console.log(false==="0")
    console.log(0=="")
   This code will give output `true` `true` `true` `true` `break` `true` `false` `false` `false`
   <hr>
   
   As we can see, the `loose equality`  `==` operator converts the values of two operand as possible and then check for equality whereas the `strict equality` `===` operator check only the value hence if two data are of different data types, it returns `false`.
   <hr>
   
Rest logical operators like `<` `>` `<=` `>=` `!==` `!===` all work as usual and so do `and` `or` and `not`.

#### Object.is ()

`Object.is()`  is not equivalent to the  `==`  operator. The  `==`  operator applies various coercions to both sides (if they are not the same type) before testing for equality (resulting in such behavior as  `"" == false`  being  `true`), but  `Object.is()`  doesn’t coerce either value.

`Object.is()`  is also not equivalent to the  `===`  operator. The only difference between  `Object.is()`  and  `===`  is in their treatment of signed zeros and  `NaN`  values. The  `===`  operator (and the  `==`  operator) treats the number values  `-0`  and  `+0`  as equal but treats  `NaN`  as not equal to each other. 
^This is wrong and IDK what right is soo...

This is further explained by code code below:

    console.log(NaN==NaN)
    console.log(-0==+0)
    
    console.log(NaN===NaN)
    console.log(-0===+0)
    
    console.log(Object.is(NaN, NaN))
    console.log(Object.is(-0, +0))

   This code returns `true` `false` `true` `false` `true` `false`
   
   ## Loops and Iterations
In any programming language we use Loops and Iterations to automate repeating tasks/code multiple times with a statement whose Boolean value decides if the loop is to be executed or nor. Here, we talk about `for loop` and `while loop` and their derivatives. 
### For loop
Syntax:

    for(statement1; statement2; statement3){
    codehere;
    }
   We now discuss about how the program control flows in a for loop. When the control reaches the starting if the for loop, the first statement, statement1 is executed. After that, the second statement, statement2, which is usually a condition is checked, if the second statement is true, we run the code bounded by curly braces {}, and if not, the loop is terminated, and control is passed to the command following the loop after the closing curly brace. Once it is established that the second statement is true, the code is run and then the third statement, statement3 is executed which is where value of some variable is changed to as to keep the iteration of loop under control.
    
   #### For in loop
   The for in loop is a variation of for loop that is used to deal with objects of Java Script. It is used to access the keys of an object. This is better explained by example below:
   

    let kathmandu = {
    Baneshwor : 8,
    Bhaktapur : 9,
    Kausaltaar: 2,
    }
    for (let a in kathmandu){
    console.log(`I rate ${a} ${kathmandu[a]} out of 10.`)
    }
   This will return these statements in console:

    I rate Baneshwor 8 out of 10.

    I rate Bhaktapur 9 out of 10.

    I rate Kausaltaar 2 out of 10.
#### For of loop
We'll come back to this later, for now this is what you need to know. The for of loop is used to access only the values of keys in an object. This loop doesn't work with just any object, it asks for and iteratable object like an array.

### While Loop
The while loop is another kind of loop we have in JS, similar to the for loop, it is used to repeat a block of code until a condition is met. 
Example: 

	    var x = 10;
	    while(x>=0){
	    console.log(x);
	    x--;
	    }
This code will return 10 9 8 7 6 5 4 3 2 1 0 to the console.
#### do while loop
The do while loop can be considered as a variant of the while loop. While the while loop check the condition prior to the execution of the code, the do while loop checks at the end of of one iteration for should there be next iteration or not. Because of this the code in a do while loop is executed atleast once.
Example:

	    var x = 0;
	    do{
	    console.log(x);
	    x--;
	    } while (x>10);
This will return `0` to the console.

### Break and continue


   
   

  
    

