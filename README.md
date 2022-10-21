# TIL 21/10/2022

# 1. What are the characteristics of JavaScript - data type and JavaScript?
Javascript is the language we are going to learn from now on. So today, we will have spend some time digging deeper into what this language is and what qualities it has. if we input numerik number mede variabel become integer, if we input true/false it become boolean, and etc

loosely typed dynamic language
JavaScript is a loosely typed language, meaning you don’t have to specify what type of information will be stored in a variable in advance. JavaScript automatically types a variable based on what kind of information you assign to it (e.g., that '' or " " to indicate string values).
    
JavaScript Type Casting
Typecasting in JavaScript means converting one data type to another data type i.e., the conversion of a string data type to Boolean or the conversion of an integer data type to string data type. The typecasting in JavaScript is also known as type conversion or type coercion.

==, ===

== is a equal operator that use for check an equal on javascript

=== is a identical operator that check the variable if contains same information and same data types in javascript 

example:

#1 typeof

whenever a variable’s type is in doubt, you can employ the typeof operator:

typeof 1 //> “number”

typeof “1” //> “string”

typeof [1,2,3] //> “object”

typeof {name: “john”, country: “usa”} //> “object”

typeof true //> “boolean”

typeof (1 === 1) //> “boolean”

typeof undefined //> “undefined”

typeof null //> “object”

const f = () => 2

typeof f //> “function”

#2 Double Equals Versus Triple Equals

The === mean “equality without type coercion”. Using the triple equals, the values must be equal in type as well.

1 == “1” //> true

1 === “1” //> false

null == undefined //> true

null === undefined //> false

‘0’ == false //> true

‘0’ === false //> false

0 == false //> true

0 === false //> false, because they are of a different type

Note, you can use !== for checking inequality with type coercion:

1 != "1" //> false

1 !== "1" //> true

#3 Checking for Falsiness

Using the ! operator (called the “bang” operator) to check for falsiness, we notice the following:

!null //> true

!undefined //> true

!0 //> true

!"" //> true

!false //> true

![] //> false

!42 //> false

!"hello world" //> false


Answer the following questions:
What is the **problem** of a loosely typed dynamic language, and what are the ways to **supplement** it?
in javascript we don’t have to specify what type of information will be stored in a variable in advance, that made us cant make the method, so we need the define the type of data waht that variable contain to made the method.

Compare the difference between undefined and null.
The difference between undefined and null is, null is an object so er can add number to it, but undefined is not an object so if we add number it will results NaN

# 2. What is JavaScript object and Immutability?
Primitive type data, and Reference type data.
Primitive data types are simple and at lowest level of implementation, its not object and doesn't have any methods, such as strings, booleans, null and unified. javascript will converts primitives strings into objects, so we can using methods
Refrence data in javascript is dynamic so it no have fixed size, most of them are objects and have methods, such as arrays, collections.
Primitive data is treated something like this

![will3](https://user-images.githubusercontent.com/63656243/197225909-5a3220ef-42ce-4d74-8ace-86f0c7bd6fb1.png)

while reference data will treated like this

![will4](https://user-images.githubusercontent.com/63656243/197226224-a9fcb458-654f-4b75-af3f-330ae9fbe3c1.png)

How to make Immutable Object?
mutability means ability to change overtime, iimutability meaning the object will not change overtime, when immutability we cannot add new property, modify or delete it, wo make immutability we can use const function like this

![willjpeg](https://user-images.githubusercontent.com/63656243/197227160-c216aa08-32de-4dfa-83c9-7b4316c23d6d.jpeg)

What are shallow copy and deep copy. What are the differences?
shallow copy is when we copy data, the original is object is stored and only the reference address is copied, in deep copy both original and repetitive copies are stored.

# 3.Hoisting and TDZ
Scope, Hoisting and TDZ
Scope is current context of cide, Hoisting is mechanism that makes variables usable before they declared and execute, TDZ or temporal dead zone is region of scope which variable is defined but cant be used because variable didn't exist.

![will5](https://user-images.githubusercontent.com/63656243/197228046-f589167e-e68c-4f5a-b114-2fe87f3a8d87.png)


Different ways of hoisting in Function Declarations and Function Expressions.
in hoisting on function declaration, it must be begin with function statement, must have name and executing on compilation phase. in function expression it must be stored on variable, no need name and executing on execution phase of javascript engine, both of them are hoisted function declaration hoisted first and function expression hoisted fully, usually variable declarations get hoisted but their assignment expression dont.

Execution Context and Call Stack
execution context is environment to handle the transformation and execution of JS code, the execution stack or call stack keeps track of all execution context during life cycle of a script. both oof the process carried out under the hood to let our code run

Scope Chain and Information Hiding
Scope is context environment created when function is written, this context defines whatother data has access to, closure are functions that have access to variables from another functions scope, it will return another function, encapsulation or information hiding is key for object oriented programming (OOT) means separating desrtiption of how to use a class from the implementation details, it is to hide our method.

# 4. Let’s do some Exercise: 
What would be the “b” value printed on the console?

![will](https://user-images.githubusercontent.com/63656243/197222083-41f70ffd-5420-426f-a8a8-8d69997aca38.png)

Variable “b” will be printed as 1 in console.log as it was assigned.
There are 3 console lines that print “b”.

Which “b” value would be printed from which line of console.log? Explain why.
based on my text editor, it was : line 10, line 7, and line 13
line 10 : printed as 1 because the variable “b” is assigned as 1
line 7 : printed as 101 because there is an incrementation (b++) in the function hi(), and it’s going to adding 1 to the variable b when the function is called
line 13 : printed as 1 because the variable “b” was declared as 1 before the hi() function was created.

What would be //console.log(a); in the comment? If there’s an error, explain why and fix the error.

![erorwill](https://user-images.githubusercontent.com/63656243/197222613-77930e5a-211f-400f-9f92-493be6d6be70.png)

For the error part, “a” is a constant with a value is 1, which is defined and declare in the hi() function, so the constant “a” has a limited scope in the hi() function. That’s why the console give an alert ‘a is not defined’.
The way to fix this easily is turn const a into global scope variable by replace it to outside of the hi() function and const a is already global scope variable then you can access it from anywhere.

![will2](https://user-images.githubusercontent.com/63656243/197223020-6e450822-9c3c-4fd2-bfea-e6a2e56582b9.png)
