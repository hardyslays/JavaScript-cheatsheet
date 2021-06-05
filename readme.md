# **JAVASCRIPT CHEATSHEET**

---

---

# PREFACE:

Hello readers, I have created this JavaScript cheatsheet as I was learning the language itself, for future references and also to help my lads out there, obviously. This covers up the basic functionalities and some special cases in brief. Many things are not explained in this document, as, well, **IT IS NOT A DOCUMENTATION.**

Relax bro, this is just a cheatsheet, you can find the detailed explanation and tutorials on various sites as well as youtube. The purpose of this cheatsheet is to accumulate all the basic functionalities present in JavaScript at one place, so you can partially rely on it.

At last, nothing comes without practice, so if you want to get some real experience, go get your hands dirty.

---

---

# TABLE OF CONTENTS:

1. [VARIABLES IN JAVASCRIPT](#variables:)
2. [OPERATORS IN JAVASCRIPT](#operators)
3. [ARRAYS](#array)
4. [FUNCTIONS](#function)
5. [FLOW-CONTROL STATEMENTS](#control)
   - [IF-ELSE STATEMENTS](#if-else)
   - [SWITCH STATEMENTS](#switch)
6. [OBJECTS](#object)
7. [LOOPS](#loops)
   - [WHILE LOOP](#while)
   - [FOR LOOP](#for)
   - [DO WHILE LOOP](#do-while)
   - [SPECIAL FUNCTIONS](#special-func)
     - [RANODM](#random)
     - [PARSE-INT](#parse-int)
8. [VAR VS LET](#varvslet)
9. [OBJECT FREEZING](#object-freeze)
10. [ARRAY FILTER METHOD](#arr-filter)
11. [ARRAY MAP METHOD](#arr-map)
12. [ARRAY REDUCE METHOD](#arr-reduce)
13. [REST PARAMETERS](#rest)
14. [SPREAD PARAMETERS](#spread)
15. [DESTRUCTURING](#destructure)
    - [DESTRUCTURING OBJECTS](#des-obj)
    - [DESTRUCTURING ARRAYS](#des-arr)
    - [DESTRUCTURING FUNCTION ARGUMENTS](#des-func)
16. [SPECIAL STRING-TEMPLATE LITERALS](#template)
17. [CLASSES](#class)
    - [SYNTAX](#class-syn)
    - [PRIVATE AND PROTECTED PROPERTIES](#private-protect)
    - [GETTERS AND SETTERS](#get-set)
18. [IMPORT AND EXPORT](#imp-exp)
19.

# VARIABLES: {#variables}

Types of variables:

- undefined
- null
- string "HELLO"
- number 13, 3.1419
- symbol
- array [1, 2, "Hello" 3, "there"]
- object { title: "first", id: 101}

Declaration of variables:

- var :- Global scope
- let :- Local scope
- const :- constant literal

Declaring variable using 'var':

```js
var a;
a = "hello";

var b = 7.0;
```

Declaring variable using 'let':

```js
let a;
a = "hello";

let b = 7.0;
```

Declaring variable using 'const':

```js
const p = 3.1419;
```

---

# OPERATORS: {#operators}

Types of operators:

1. Arithmatic operation:
   - Addition (+)
   - Substraction (-)
   - Multiplication (\*)
   - Power (\*\*)
   - Division (/)
   - Modulus (%)
   - Increment (++)
   - Decrement(--)
     <br>
2. Assignment operators:
   - equal assignment (=)
   - Sum assignment (+=)
   - Difference assigment (-=)
   - Product assignment (\*=)
   - Division assignment (/=)
   - Mod assignment (%=)
     <br>
3. Comparision operator:
   - Equal to (==)
   - Strictly equal to (===)
   - Not equal to (!=)
   - Not equal value or type (!==)
   - Greater than (>)
   - Less than (<)
   - Greater or euqal to (>=)
   - Less or equal to (<=)
     <br>
4. Logical operators:
   - And (&&)
   - Or (||)
   - Not (!)
     <br>
5. Bitwise operator:
   - Bitwise AND (&)
   - Bitwise OR (|)
   - Bitwise NOT (!)
   - Bitwise XOR (^)
   - Left shift (<<)
   - Right shift (>>)
     <br>
6. Other:
   - Typeof operator (**typeof** var)
   - Delete operator (**delete** var)
   - in operator (element **in** arr)
   - instanceof operator (**instanceof** obj)
   - void operator ( **void(0)** )
   - Ternery operator [ ()? yes : no;]

---

# ARRAYS: {#array}

An example of array could be:

```js
var arr = [2, 3, 5, 7, 11];
```

We can have nested arrays also, it can be made by:

```js
var arr = [0, [1, 2], [3, 4, 5], 6, 7, [8, 10, 9], 6];
```

Functions for array:

- push()
- pop()
- shift()
- unshift()

## PUSH:

To push an element at the and of the array:

```js
var arr = [0, 1, 2];
//CURRENTLY ARRAY HAS 0, 1 & 2

arr.push(3);
arr.push(4);

//Array is now:
//arr = [0, 1, 2, 3, 4];
```

## POP:

To remove the last element of the array and return it.

```js
var arr = [0, 1, 2, 3, 4];
var last = arr.pop();
//THIS WILL MAKE
//  last = 4;
//  arr = [0, 1, 2, 3];
```

## SHIFT

To remove the first element of the array and return it.

```js
var arr = [0, 1, 2, 3, 4];
var first = arr.pop();
//THIS WILL MAKE
//  first = 0;
//  arr = [1, 2, 3, 4];
```

## UNSHIFT:

To add an element to the beginning of the array.

```js
let arr = [0, 1, 2, 3, 4];
let first = -1;
arr.unshift(first);

//THIS WILL MAKE:
//  arr = [-1, 0, 1, 2, 3, 4];
```

---

# FUNCTIONS: {#function}

## INTRODUCTION:

Function is a created for the block of code which is to be used many time in the program.
Ex: If the function is to calculate sum of factorials of first N natural numbers, we have to calculate factorial many times. So, we can create a function to calculate factorial of a number N.

## SYNTAX:

The syntax of a function is:

function functionName(args)
{
&nbsp;&nbsp;&nbsp;&nbsp; statements;
}

An example to return sum of two numbers is:

```js
function addThem(a, b) {
  let c = a + b;
  return c;
}

//Calling the function
console.log(addThem(8, 10)); //Returns 18
```

---

# CONTROL FLOW STATEMENTS: {#control}

## IF-ELSE: {if-else}

If-else statement block is used to check if a given statement is true or false and then proceed with the result.

### SYNTAX:

if(condition)
{
statements if true
}
else
{
statement if false
}

### EXAMPLE:

An if else statmenet checking if **var a\*** is greater than **var b** :

```js
function max(a, b) {
  if (a > b) {
    return a;
  } else {
    return b;
  }
}
```

### NESTED IF-ELSE:

We can have many if-else statements to create a multiple direction control flow.

Ex: If we have to choose the greatest number from three numbers a, b and c:

- Check if a > b:
  - If yes, Check if a > c.
    - If Yes, return a.
    - If no, check if b > c:
      - If yes, return b.
      - Else return c.
  - If no, Check if b > c:
    - If yes, return b.
    - If no, return c.

So, the syntax would be:

```js
if (a > b) {
  if (a > c) return a;
  else if (b > c) return b;
  else return c;
} else if (b > c) return b;
else return c;
```

## SWITCH-CASE STATEMENTS: {#switch}

When we have to check for the value of an statement and have the control flow according to only **"equal to" logic**, we use switch-case code block as its syntax is shorter than many nested if-else statements.

###SYNTAX:
Swich statement takes one argument, that could be a variable or an expression:

```js
switch (arg) {
  case 1:
    //If arg = 1, do this
    break;
  case "Hi":
    //If arg = "Hi", do this
    break;
  default:
  //If arg matches with nothing, do this
}
```

---

# OBJECTS: {#object}

Objects are the datatype that exhibit the OOPS feature of the JavaScript.

The objects can be understood as "Objects are a real life entity having many features and functions. The features are called its **Properties** and the function it can perform are called its **method**.

## SYNTAX:

To define an object named Child, having properties:

- Name
- Age

And having functions:

- SetName
- SayAge

The code would look something like this:

```js
var Child = {
  Name : "Lucy",
  Age  : 23,

  SetName : (name) => {
    Child.Name = name;
  }

  SayAge : () => {
    console.log(`My age is: ${Child.Age}.`);
  }
}
```

We can access the object values by either using **Dot notation** or by using the **Bracket notation**.

```js
var DotObj = {
  Name: "Hardy",
  Age: 23,
};
var BracObj = {
  Name: "Slays",
  Age: 32,
};

//Accessing the object properties using dot
var DotName = DotObj.Name;

//Accessing the object property using Bracket
var BracAge = BracObj["Age"];
```

Deleting a property:

```js
var Obj = {
  Name: "Hardy",
  Age: 23,
  Gender: "Male",
};

//This will delete the Obj's property of Gender:
delete Obj.Gender;
```

NOTE: Objects can also by thought of as the Dictionary datatype of some languages, as it also stores the properties in the "{Key, Value}" fashion.

We can check if the object has a property in it or not, by using **hasOwnProperty**:

```js
var Obj = {
  Name: "Hardy",
  Age: 23,
  Gender: "Male",
};

console.log(Obj.hawOwnProperty("Name")); //Returns true
console.log(Obj.hawOwnProperty("Last Name")); //Returns false`
```

---

# LOOPS: {#loops}

The loops are the code block which run again and again till the condition provided to them is **true**.
The types of loops in JavaScript are:

- Whille loop
- For loop
- Do while loop

## WHILE LOOP: {#while}

### SYNTAX:

```js
var arr = [];

var i = 0;
while (i < 5) {
  arr.push[i];
  i++;
}

//This will push the elements 0, 1, 2, 3, 4 in the Array.
```

### WORKING:

The while loop First check for the condition and if the condition provided is correct, it executes the code block.

After executing the code block once, it again checks for the condition and so on.

The updatation of Condition should be done inside of the while loop.

<br>

## FOR LOOP: {#for}

### SYNTAX:

```js
var arr = [];
for (var i = 0; i < 5; i++) {
  arr.push[i];
}

//This will push elements 0, 1, 2, 3, 4 into the Array.
```

### WORKING:

The for loop has thrre statements in the first line:

- **Initialization**: Setting up the variable for the condition.
- **Condition**: Checking for the condition.
- **Update**: Updating the var of Condition.

<br>

## DO WHILE LOOP: {#do-while}

### SYNTAX:

```js
var arr = [];
var i = 0;

do {
  arr.push(i);
} while (i < 0);
```

### WORKING:

The working of Do-while loop is similar to the While loop except for the fact that:

    Do while loop first executes the code block then check for the condition.

This means that the do while loop will run for atleast one time, irrespective of the condition.

---

# SPECIAL FUNCTIONS: {#special-func}

## MATH.RANDOM() {#random}

Random() is a function that returns a decimal value between 0 to 1, 1 excluded.

```js
var ran = math.random();

//ran contains a random value between 0 and 1.
```

We can also get random whole number using this:

```js
var Random;
Random = math.floor(math.random() * 20);

//Random contains a random whole number from 0 to 19.
```

<br>

## ParseInt() {#parse-int}

ParseInt function is used to convert the string type to integer type:

```js
var s = "54";
var num = parseInt(s);

//num = 56 (integer type)
```

<br>

## ParseInt with radix

We can also convert the string type to integer type where string type has different base quantity(i.e. the base is not 10):

```js
var s = "110";
var num = parseInt(s, 2);

//num = 6
```

---

# VAR vs LET: {#varvslet}

Some major differences between **var** and **let** keywords are:

- You can declare a variable more than one time in a block using var, but not using let:

  ```js
  var Name = "Hardy";
  var Name = "himanshu"; //No error in this

  let age = 12;
  let age = 23; //Gives an error
  ```

- The scope of var keyword is global or local to a function, while the scope of a let keyword is limited to the block or expression it is decleared into:

  ```js
  var Name = "Hardy";
  if (true) {
    var Name = "Nothing";
    console.log(name);
  }
  console.log(name);
  //This will print:
  //Nothing
  //Nothing

  //While if we use let keyword:
  let Name = "Hardy";
  if (true) {
    let Name = "Nothing";
    console.log(name);
  }
  console.log(name);
  //This will print:
  //Nothing
  //Hardy

  //As the scope of Name defined by let inside the if block is limited to the if block itself, and that is desructed upon coming out of that block.
  ```

<br>

---

# OBJECT.FREEZE: {#object-freeze}

If we declare an array or an object as const, we cannot change the whole array or object. But still, we can mutate the elements inside them one by one:

```js
const arr = [1, 2, 3, 4];

arr = [1, 2, 3]; //Gives error
arr[0] = 3; //Doesn't give an error :')
```

So we use object.freeze for this purpose:

```js
  const obj = {
    pi: 3.141528;
  }

  obj["pi"] = 3.1415; //valid here

  object.freeze(obj);
  obj["pi"] = 99; //Gives error as we can't change properties of an frozen object
```

<br>

---

# ARRAY FILTER FUNCTION: {#arr-filter}

Filter method creates an array filled with the elements of the reference array which pass a given test(function passed as arg).

## SYNTAX:

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

var evenArr = arr.filter((num) => num % 2 == 0);
```

<br>

---

# ARRAY MAP FUNCTION: {#arr-map}

Array map method returns an array which is modified using the given reference array with the provided instruction.

EX: To get an array containing squares of elements of a given array, we can use Map method:

```js
var arr = [1, 2, 3, 4, 5];

var sqr = arr.map((x) => x * x);
//The sqr array is:
// [1, 4, 9, 16, 25];
```

<br>

---

# ARRAY REDUCE METHOD: {#arr-reduce}

Array reduce method reduces the array of elements to a single value using the commands specified.

It proceeds from left to right.

EX:

- We can get sum of all elements present in the array.
- We can get the min or max element present in the array.

```js
var arr = [1, 2, 3, 4, 5, 6];

//To return the sum of elements of an array:
var sum = arr.reduce((a, b) => a + b, 0);

//To return the max element of an array:
var max = arr.reduce((max, a) => (max < a ? a : max), 0);
```

<br>

---

# REST PARAMETERS: {#rest}

Rest parameter are useful when we have to create a function where we don't know the exact quantity of the arguments to be passed.

In such case, we declare the rest parameter and all the arguments passed in the function are embeded into an array.

## SYNTAX:

```js
function Sum(...args)
{
  //Here we will have an array "args" having all the arguments sequence wise.

  return args.reduce((a, b) a + b, 0));

  console.log(Sum(1, 3)); //Prints 4

  console.log(Sum(1, 3, 5, 7)); //Prints 16
}
```

<br>

---

# SPREAD PARAMETERS: {#spread}

While the rest parameter combines a bunch of arguments into an array, the spread parameter is used to divide an array into a bunch or arguments.

It is used to pass the elements of an array as arguments in a function.

It is also used to copy the elements of an array into another array.

Its syntax is the same as that of the REST param.

## SYNTAX:

```js
var arr = [0, 1, 2, 3, 4, 5];
let arr1 = arr; //This will copy the memory address of arr into arr1, so if we chang anything in arr, it will also be changed in arr1.

let arr2 = [...arr]; //This will spread the elements of arr ans then a new array will be formed for arr2 having the elements copied from arr.
```

## SPREAD for objects:

The object literals could also be spread into various (key, value) pairs using the spread parameter. The syntax is same as of array.

<br>

---

# DESTRUCTURING {#destructure}

## DESTRUCTURING OBJECTS: {#des-obj}

Destructuring an object means to get the values of object's properties in variables.

## SYNTAX:

```js
  Let person = {
      Name: "Himanshu",
      Age: 23,
      Height : "180cm"
  }; //Declaring object person with 3 properties

  //THE OLD WAY TO COPY THA VALUES OF PROERTIES TO VARIABLES:
  let name = person.Name;
  let age = person.Age;
  let height = person.Height;

  //Using destructuring, we can do this in onje line:
  let { Name : name, Age : age, Height: height} = person;

  //Or, if we want the names of variables to be same as name of properties, we just use ames of properties:
  let { Name, Age, Height } = person;

```

## DESTRUCTURING ARRAYS: {#des-arr}

We can also destructure the array variables in the same manner as objects:

```js
let arr = [1, 2, 3, 4, 5];

let [x, y, , z] = arr;
//THIS ASSIGNS THE VALUES AS:
//x = 1
//y = 2
//z = 4
```

We can also swap values of two variables in the same manner:

```js
let a = 6,
  b = 5;
[a, b] = [b, a];

//Now a = 5 and b = 6
```

## DESTRUCTURING FUNCTION ARGUMENTS: {#des-func}

Very often in API calls, we pass objects where we just need some of the properties of the objects. In such cases, we destructe the object to get just the ueful data:

```js
let books = {
  fiction: 2,
  hollywood: 4,
  horror: 5,
  drama: 12,
  others: 21,
};

//If we just need to use the horror and drama genre of objet

//Without destructuring:
function sumHorrorAndDrama(books) {
  return books.horror + books.drama;
}

//With destructuring:
function sumHorrorAndDrama({ horror, drama }) {
  return horror + drama;
}
```

<br>

---

# TEMPLATE LITERALS: {#template}

Very often we have to use a fixed literal with some values changd inside them, for example:

You have 5 chances left.

You have 4 chances left.

You have 3 chances left.

You have 2 chances left.

You have 1 chances left.

For these types of output, you have to create a new string literal each time, or have to edit the string again and again.

You can use template string instead.

## SYNTAX:

The template literals are written using backtick ( ` ) instead of single or double qoutes:

```js
let chances = 5;
let warning = `You have ${chances} chances left.\n`;

do {
  console.log(warning);
} while (chances--);
```

<br>

---

# CLASSES: {#class}

Classes can be said to be templates for creating objects having same properties and methods.

They are used when we have to create many instances having same properties.

Their usage is to replace the need of constructor function, which is harder to create and understand.

## SYNTAX: {#class-syn}

The class is created using class keyword:

```js
  class Person
  {
    constructor(name, age, gender)
    {
      this.name = name;
      this.age = age;
      this.gender = gender;
    }
    const syaHi = () => {
      console.log(`Hello, my name is ${this.name}`);
    }
  }

  let Himanshu = new person("Himanshu", 23, "Male");

  let Natasha = new person("Natasha", 24, "Female");

```

## PRIVATE AND PROTECTED PROPERTIES: {#private-protect}

In javascript, the properties of a class are PUBLIC by nature, i.e. they can be accessed by anyone.

To apply the concept of data abstraction of OOPS(You can learn about functionalities of OOPS on internet), We have to have a way to set the properties to PRIVATE and PROTECTED nature.

This is acheived by using special prefixes before the variables:

- underscore ( \_ ) : Protected
- hashtag ( # ) : Private

For example, to set the age to private and gender to protected of person class taken in last example:

```js
  class Person
  {
    constructor(name, age, gender)
    {
      this.name = name;
      this.#age = age;
      this._gender = gender;
    }
    const syaHi = () => {
      console.log(`Hello, my name is ${this.name}`);
    }
  }

  let Himanshu = new person("Himanshu", 23, "Male");

  let Natasha = new person("Natasha", 24, "Female");

```

## GETTER AND SETTERS:{#get-set}

Not all of the methods can access the **private/protected** properties of their object, so if we want a function to be able to interact with the private/protected properties of the object, we have to add get and set before functions, where:

- get is used to be able to read the value of private/protected value
- set is used to be able to write or change the value of private/protected property

```js
  class Person
  {
    constructor(name, age, gender)
    {
      this.name = name;
      this.#age = age;
      this._gender = gender;
    }
    const syaHi = () => {
      console.log(`Hello, my name is ${this.name}`);
    }
    get Age(){
      return this.age;
    }

    set Age(val){
      this.age = parseInt(val);
    }
  }

  let Himanshu = new person("Himanshu", 23, "Male");

  let Natasha = new person("Natasha", 24, "Female");
```

### NOTE:

The getters and setters are accessed as properties of objects rather than as being a method.

This means that you do not provide the paranthesis when clling them.

So, if we want to call the getters and setters provided in above code sample, we have to do this:

```js
let Himanshu = new person("Himanshu", 23, "Male");

//To set the age to 24:
Himanshu.Age = 24;

//To get the age:
console.log(Himanshu.Age);
```

<br>

---

# IMPORT AND EXPORT {#imp-exp}

The import and export functionalities are used in JavaScript while working with multiple files.

These are used to send the functions and properties of one file to another, to be used there.

- IMPORT is used to import a functionalities of a foreign file to your ccurrent file.
- EXPORT is used to export the particular property or function of current file to foreign files.

## SYNTAX FOR EXPORTING:

We can export any variable or const of a file:

```js
  //file: "pi.js"

  const pi = 3.141528;

  export pi;
```

```js
//file: "math.js"
const sqr = (x) => x * x;
const pow = (a, x) => {
  let prod = 1;
  for (var i = 0; i < x; i++) {
    prod *= a;
  }

  return prod;
};

export { sqr, pow };
```

## SYNTAX FOR IMPORTING

```js
import pi from "./p.js";

console.log(pi);
```

```js
import { sqr, pow } from "./math.js";

console.log(sqr(4)); //Prints 16
console.log(pow(2, 3)); //Prints 8
```

## ALIASING IMPORT NAMES

We can change names of properties while importing from modules, using **as** keyword:

```js
  import pi as PI from './pi.js';

  console.log( PI ); // prints the value of pi
```

## IMPORTING EVERYTHING

We can import everything using \* keyword:

```js
// import { sqr, pow } from "./math.js";
import * as maths from "./math.js";

console.log(maths.sqr(4)); //Prints 16
console.log(maths.pow(2, 3)); //Prints 8
```

## DEFAULT EXPORT

Default exports are useful when we have to export only one object from a module.

It enables the foreign files to import that object with any name they prefer.

```js
//file = './file1.js'

var name = "Himanshu",
  age = 25,
  gender = "Male";

let obj = {
  Name: name,
  Age: age,
  Gender: gender,
};

export default obj;
```

```js
import person from "./file1";

cosole.log(person);
//{ Name : "Himanshu", Age : 25, Gender : "Male" }
```

---

---

<style>
#anim{
  opacity: 0.5;
}
#block:hover span{
  cursor:pointer;
  opacity: 1;
}
</style>

<div style="background-color: #d2d2d2; padding:0.5rem;border-radius:2rem; box-shadow:0 0 10px 5px;" id="block">
<h1 style="text-align:center; font-family:verdana;font-size:3rem;">WITH <span id="anim">❤️</span> FROM <a href="">HARDY</a></h1>
</div>

---

---

---
