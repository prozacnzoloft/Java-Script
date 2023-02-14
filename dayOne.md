
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
## Loops and Iterations
In any programming language we use Loops and Iterations to automate repeating tasks/code multiple times with a statement whose Boolean value decides if the loop is to be executed or nor. Here, we talk about `for loop` and `while loop` and their derivatives. 
### For loop
Syntax:

    for(statement1; statement2; statement3){
    codehere;
    }
   We now discuss about how the program control flows in a `for loop`. When the control reaches the starting if the `for loop`, the first statement, `statement1` is executed. After that, the second statement, `statement2`, which is usually a condition check statement, if the second statement returns `true`, we run the code bounded by curly braces {}, and if not, the loop is terminated, and control is passed to the command following the loop after the closing curly brace. Once it is established that the second statement is true, the code is run and then the third statement, `statement3` is executed which is where value of some variable is changed to as to keep the iteration of loop under control.
    
   #### For in loop
   The `for in` loop is a variation of `for` loop that is used to deal with objects of Java Script. It is used to access the keys of an object. This is better explained by example below:
   

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
   <hr>
    
#### For of loop
We'll come back to this later, for now this is what you need to know. The for of loop is used to access only the values of keys in an object. This loop doesn't work with just any object, it asks for and iterable object like an array.
<hr>

### While Loop
The while loop is another kind of loop we have in JS, similar to the for loop, it is used to repeat a block of code until a condition is met. 
Example: 

	    var x = 10;
	    while(x>=0){
	    console.log(x);
	    x--;
	    }
This code will return 10 9 8 7 6 5 4 3 2 1 0 to the console.
<hr>

#### do while loop
The do while loop can be considered as a variant of the while loop. While the while loop checks the condition prior to the execution of the code, the do while loop checks at the end of one iteration for should there be next iteration or not. Because of this the code in a do while loop is executed at least once.
Example:

	    var x = 0;
	    do{
	    console.log(x);
	    x--;
	    } while (x>10);
This will return `0` to the console.
<hr>

### Break and continue
The break and continue statements are used to work with program control in a loop. The continue statement terminates the current iteration and passes the control to start of the loop. Similarly, the break statement terminates the current iteration and passes the control to statement following the loop.
Example:

    var x = 10;
	    do{
	    console.log(x);
	    x--;
	    if (x==4){
	    console.log("Four");
	    continue;
	    }
	    if(x==8){
	    console.log("Bye Bye")
	    break;
	    } while (x>0);
This code will return `1` `2` `3` `Four` `5` `6` `7` `Bye Bye` to the console. 
<hr>

#### Labeled Statements
From what I gathered the labeled statements are useless in most cases but it's better to know about anything about the topic you're learning so let's get started. There is no `goto label;` statement in Java Script. We can only use labels with `break;` and `continue;` statements. These labeled statements are used mostly in data filtering using nested loops. A simple use case of these statements is given below:

 

       var  obj1  = [{    
    name: "Nawadit1",    
    address: "Tansen1",
    favriouteNO: 31,
    favriouteSongs: ["Dress1", "Midnight rain1", "Gorgeous2"]
    },
    {
    name: "Nawadit2",
    address: "Tansen2",
    favriouteNO: 32,
    favriouteSongs: ["Dress2", "Midnight rain3", "Gorgeous2"]
    },
    {
    name: "Nawadit3",
    address: "Tansen3",
    favriouteNO: 33,
    favriouteSongs: ["Dress3", "Midnight rain", "Gorgeous3"]    
    },    
    {    
    name: "Nawadit",
    address: "Tansen",
    favriouteNO: 3,
    favriouteSongs: ["Dress", "Midnight rain", "Gorgeous","Midnight rain3"]
    }]   
    primaryLoop:
    for (let  a  =  0; a<obj1.length; a++){
    secondaryLoop:
    for(let  b=0; b<obj1[a].favriouteSongs.length; b++){
    if (obj1[a].favriouteSongs[b]==="Midnight rain3"){
    console.log(obj1[a])
    break primaryLoop;
    }    
    }    
    }

This will return 

    {name: 'Nawadit2', address: 'Tansen2', favriouteNO: 32, favriouteSongs: Array(3)}address: "Tansen2"favriouteNO: 32favriouteSongs: (3) ['Dress2', 'Midnight rain3', 'Gorgeous2']name: "Nawadit2"[[Prototype]]: Object

to the console
<hr>

## Control flow
### Exception handling
It's very frequent for a code to run into a bug every once in a while. In a normal scenario the execution of the rest of the code after where there is a mistake is skipped and the code terminates, and this is where exception handling or error handling comes in. Error handling as the name suggests is used to handle errors in your code.
#### The try-catch statement
The `try-catch` statement is used to handle error in parts of your code. It's syntax is something like this:

    try{
    //code that may cause error
    }
    catch(error_variable){
    code to run if there occurs an error
    }
   When the program is run, the control is first passed to the code of the try block. If that code runs w/o any error, then the code of catch block is skipped and the control is passed to statement following the try-catch statement. If there does occur and error in the code in the try block, then the execution of the rest of the code in try block is skipped and the control is passed to the top of the code in catch block. 
   An important thing to note while working with try-catch statement is that it only handles error of synchronous code of the try block and not the asynchronous one. This is explained by the examples below: 
   
    function  nawadit(){
    console.log(taylor);
    console.log("Code of nawadit() ran sucessfully.")
    } 
    try {
    setTimeout(nawadit(), 1000);
    console.log("code of `try` ran sucessfully.")
    } catch (error) {
    console.log("error handeled")
    }

   This will return `error handled` to the console.

    try {
	    setTimeout(() => {
	    console.log(taylor);
	    console.log("code of `try` ran sucessfully.")
    }, 1000);
    }
    catch (error) {
    console.log("error handeled");
    }
   This will return an error in the console.
   <hr>
   
This is because the first problem the function is scheduled and then executed and checking and handling errors of nawadit() function or the code written directly here instead of calling a function,  falls under the scope of this try-catch statement whereas in second example the setTimeout() is used to schedule the code which it does w/o any problem and now the error arises with that code, handling which is not the responsibility of this try-catch statement.
<hr>


### Error objects
Error object is the object passed from try clause to catch clause. This object properties like name, message and stack that are used to identify the error that occurred. All three of there properties contain string data.
The name property contains the type of error that occured like reference error etc.
The message error contains the message that is to be displayed in the console  
The stack error contains the location of the line of code where the error occurred. To access these members we use . operator after error name.
We can throw our own costume error objects using the `throw` statement


#### Throw statement
Syntax:
throw new errorName ("Error message")
<hr>


### Finally statement
The try-catch statement can have an additional block of code enclosed with in curly braces of finally statement that get executed regardless of if there is an error or not. This code gets executed even if the code of try or catch block isn't executed to the end. 

Example:

    try{
    var age = prompt("Enter your age");
    console.log(a)
    throw new age("There was an error with getting the age)"
    }
    catch(error){
    console.log(error.message);
    }
    finally{
    console.log("The code of finally bock was executed")
    }
   This code should return `There was an error with getting the age` `The code of finally block was executed` to the console.
   <hr>
   
   ### If else statement
   The if else statement in JS is used to change flow of program control according to a condition. 
   Example:
   

    int a = 2
    if (a==3){
    console.log("Three")
    }
    else if (a==4){
    console.log("Four")
    else if (a==2){
    console.log("Two")
   This code will return `Two` in console.
   <hr>

### Switch case statement
The switch case executes the code only of that case who's case index matches the switch argument. 
Example:

    var a = 2;
    switch(a):
	    case 1:
	    console.log("One")
	    break;
	    case 2:
	    console.log("Two")
	    break;
	    case 3:
	    console.log("Three")
	    default:
	    console.log("Invalid input")
	    break;
This code will return `Two` in console.

## Expressions and operators
An expression is a valid unit of code that resolves to a value. an operator is a character that represents a specific mathematical or logical action or process.
In this section, we will introduce the following operators:

Assignment operators
Comparison operators
Arithmetic operators
Bitwise operators
Logical operators
BigInt operators
String operators
Conditional (ternary) operator
Comma operator
Unary operators
Relational operators

### Assignment Operators
An assignment operator assigns a value to its left operand based on the value of its right operand. There are also compound assignment operators that are shorthand for the operations. 
Example:
`=` `+=` `-=` `*=` `/=` `**=` and so on

### Comparator operator
A comparison operator compares its operands and returns a logical value based on  the comparison.
Example `==` `===` `!==` `!===` `<=` `>=` `<` `>`

#### Strict and loose comparators.
The loose equal `==` returns `true` if the operands are equal and strict equal `===`  Returns `true` if the operands are equal and of the same type. Similarly, the loose not equal != returns true if the operands are unequal and the strict not equal returns true if the operands and their data type are unequal.

### Arithmetic operators
An arithmetic operator takes numerical values (either literals or variables) as their operands and returns a single numerical value. The standard arithmetic operators are addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`).  Apart from these some other frequently used operators are increment operator `++`, decrement operator `--`, remainder operator `%`, Urinary negation operator `-`, Urinary plus operator `+` tries to change the data into a number if not already, Exponential operator `**`

### Bitwise operators
A bitwise operator treats their operands as a set of 32 bits.
Bitwise AND	

    a & b

Returns a one in each bit position for which the corresponding bits of both operands are ones.

Bitwise OR	

    a | b
   Returns a zero in each bit position for which the corresponding bits of both operands are zeros.
Bitwise XOR	

    a ^ b

	
Returns a zero in each bit position for which the corresponding bits are the same. [Returns a one in each bit position for which the corresponding bits are different.

Bitwise NOT

    ~a

Inverts the bits of its operand. Left shift	a << b	Shifts a in binary representation b bits to the left, shifting in zeros from the right.
 
Sign-propagating right shift
		

    a >> b
				

Shifts a in binary representation b bits to the right, discarding bits shifted off.

Zero-fill right shift

    a >>> b	

Shifts a in binary representation b bits to the right, discarding bits shifted off, and shifting in zeros from the left.

 and   `15 & 9=9	1111 & 1001 = 1001`

 or   `15 | 9	=15	1111 | 1001 = 1111`

xor    `15 ^ 9	=6	1111 ^ 1001 = 0110`

 negation   `~15 =	-16	~ 0000 0000 … 0000 1111 = 1111 1111 … 1111 0000`

 negation   `~9 =	-10	~ 0000 0000 … 0000 1001 = 1111 1111 … 1111 0110`

left shift `<<` 	9<<2 yields 36

right shift `>>` 9>>2 yields 2

### Logical operators
Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value.

Logical AND (`&&`)	

    expr1 && expr2

When used with Boolean values, `&&` returns `true` if both operands are `true`; otherwise, returns `false`.

Logical OR (`||`)	

    expr1 || expr2

When used with Boolean values, || returns true if either operand is true; if both are false, returns false.

Logical NOT (`!`)	

    !expr

Returns false if its single operand that can be converted to true; otherwise, returns true.

### String operators
In addition to the comparison operators, which can be used on string values, the concatenation operator (+) concatenates two string values together, returning another string that is the union of the two operand strings.
Example

    console.log("my " + "string");
 This will console logs the string "my string".
 
The shorthand assignment operator += can also be used to concatenate strings.

Example

    let mystring = "alpha";
    mystring += "bet"; 
   This code evaluates to "alphabet" and assigns this value to mystring.

### Conditional (ternary) operator

The conditional operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition. 
The syntax is:

    condition ? val1 : val2


If condition is true, the operator has the value of val1. Otherwise, it has the value of val2. You can use the conditional operator anywhere you would use a standard operator.
Example:

    const status = age >= 18 ? "adult" : "minor";

This statement assigns the value "adult" to the variable status if age is eighteen or more. Otherwise, it assigns the value "minor" to status.

### Comma operator
This operator is primarily used inside a for loop, to allow multiple variables to be updated each time through the loop.
Example: 

    const x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
    const a = [x, x, x, x, x];
    
    for (let i = 0, j = 9; i <= j; i++, j--) {
                                    
      console.log(`a[${i}][${j}]= ${a[i][j]}`);
    }
   This will return 
a[0][9]= 9
a[1][8]= 8
a[2][7]= 7
a[3][6]= 6
a[4][5]= 5
to the console.

### Unary operators
A unary operation is an operation with only one operand.

#### delete
The delete operator deletes an object's property. The syntax is:

    delete object.property;
    delete object[propertyKey];
    delete objectName[index];

Where object is the name of an object, property is an existing property, and propertyKey is a string or symbol referring to an existing property.

If the delete operator succeeds, it removes the property from the object. Trying to access it afterwards will yield `undefined`. The delete operator returns `true` if the operation is possible; it returns `false` if the operation is not possible.

## Asynchronous JavaScript
To be vivid, asynchronous javascript refers to the parallel running of functions. Most easy example of this is `setTimeout()` and `setInterval()` function.
### Set time out
Syntax:

    setTimeout(function,delay time in ms, argumens...)
   The function will be scheduled to run after said time and the control will be passed to next statement. When the time comes, the control comes back to the setTimeout-ed function and then the function is passes to where it came from.
   <hr>

### Set Interval
Syntax:

    setInterval(function, delay, arguments...)
   Think of this as a repeated and infinite do while loop. When the given time is up, the setInterval-ed function runs. 



   
   

  
    

