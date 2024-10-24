# DAY 1: JavaScript Variables and Data Types

## What is a Variable?
A variable is a named storage that programmers can use to store data and retrieve it later using the variable name.

## Why Use Variables?
   1. Variable can store information.
   2. We can use that information later. 
   3. we can change the information later.

## What are Data Types?
Data types specify the kind of data that can be stored and manipulated within a program. JavaScript supports various data types, each serving a unique purpose.

 There are 7 data types available in JavaScript.You need to remember that JavaScript is loosely typed(or dynamiclanguage),so
 any value can be assigned to variables in JavaScript.

  According to latest ECMAScript standard there are 6 primitive data types and  1 object. 

   - **Number :** represents integer and floating values.
   - **String :** represents textual data.
   - **Boolean :** Logical  Entity with values are **true** and
   **false**.
   - **undefined :** represents variable whose value is not yet assigned.
   - **Null :** represents intentional absence of value. 
   - **Symbol :** represents unique value. 
   - **Object :** represents key value pair.  
   > **All of them except Object have immutable values,i.e.  the values which cannot be changed.**
   ## Why Use Data Types? 
 1. The data is stored appropriately for its type.
 2. Data is retrieved correctly according to its type.
 3. Data is manipulated in ways suitable for its type.
 ## Rules for Declaring Variables
  1. Variable names must start with a letter, underscore (_), or dollar sign ($).
 2. Variable names cannot start with a number.
 3. Variable names are case-sensitive.
 4. Reserved words (like JavaScript keywords) cannot be used as variable names.
 ```javascript 
 // 1. You cannot start with number
var value1 = 10;
console.log(value1);

// 2. You can use only underscore _ or dollar symbol $
var first_name = "Manoj";
var _lastname = "Kumar";
console.log(first_name + " " + _lastname);

var first$name = "Rohit";
var $firstname = "Jain";
console.log(first$name + " " + $firstname);

// Convention 1. Use camelCase writing(prefferable)
var firstName = "camelCase";
console.log(firstName);

// Convention 2. Use snake_case writing
var first_name = "snake_case";
console.log(first_name);


 ``` 

## `var`, `let` and `const` 
  ## Declare variable using var
  ```javascript 
  // Declare a variable
var firstName = "Vinay KUMAR";

// Use a variable
console.log(firstName);

// Change value
firstName = "CSE Vinay";
console.log(firstName);

/*
Expected Output:
Vinay Kumar
CSE Vinay
*/
  ```
  ##  Declare variable using let
  ```javascript 
  // Declare a variable
let value = 10;

// Use a variable
console.log(value);

// Change value
value = 11;
console.log(value);

/*
Expected Output:
10
11
*/
  ```

##  Declare variable using const 
```javascript 
// Declare a variable
const value = 10;

// Use a variable
console.log(value);
//value = 11;// Type error

/*
Expected Output:
10
*/
``` 
## Data Types in JavaScript 
JavaScript is a dynamically typed language, meaning that a variable isn’t associated with a specific type. In other words, a variable can hold a value of different types. For example:

>To determine the current type of the value stored in a variable, you use the `typeof` operator. 
```js 
let x = 120;
console.log(typeof x); // "number"

x = false;
console.log(typeof x); // "boolean"

x = "Hi";
console.log(typeof x); // "string"

```
1. ## ``undefined`` type 
    it has only one value undefined 
    ```js
    let x;
    console.log(x); // undefined
    console.log(typeof x); // undefined
    ```
    **Note 1**: When a variable is declared but not initialized, it defaults to undefined.
2. ## ``null`` type 
    it has only one value null 
    ```js 
    let x = null;
    console.log(x);//null 
    console.log(typeof x);//object 
    console.log(typeof(x));//object
    /* 
    Here We Observe both typeof , typeof() both is valid to check an type of an variable
    */
    ```

    ```js 
    let x = null;
      console.log(typeof x); // object

       console.log(null == undefined); // true
       console.o
    ```
    Note 1: The ``typeof`` null returns ``object`` is a known ``bug in JavaScript``.
    -  A proposal to fix was rejected due to the potential to break many existing sites.
    - So, even though null is supposed to represent "no value" or "nothing," typeof null mistakenly returns "object". In a well-designed system, it should have returned "null".
```js 
console.log(null == undefined);//true
/*
-Loose equality (==) allows JavaScript to convert or "coerce" the values to the same type before comparing them.

When you use ==, JavaScript thinks, "Hmm, null and undefined are both empty or 'nothing' values."

So, it treats them as equal because they both represent "nothing" in a loose way.
*/
``` 
```js 
console.log(null === undefined) ; //false
 /*
 Strict equality (===) does not convert or change the values. It checks if both the value and the type are exactly the same.

Even though null and undefined both seem like "nothing," they are still different types.

null is an object-like value.
undefined is its own type.
Since null and undefined are not the same type, JavaScript says they are not equal when using ===.
 */
``` 
3. ##  ``number`` type  
JavaScript uses the number type to represent both integer and floating-point numbers. 
```js
let num = 100; // interpreted as an integer 100
let price = 12.5; // interpreted as floating 12.5
let discount = 0.05; // interpreted as floating 0.05
let offer = 200.0; // interpreted as an integer 200 
``` 
4. ## `` Big Integers`` type 
To make a BigInt, you append n to the end of the number literal 
```js 
let bigInt = 9007199254740991n;
// OR
let bigInt = BigInt(9007199254740991);
```
5. ## ``Symbol()`` type 
The Symbol function creates a new unique value every time you call it.



```js
console.log(typeof Symbol() === typeof Symbol()); //true
console.log(typeof Symbol() == typeof Symbol());  //true 
console.log(typeof Symbol);//function 
console.log(typeof Symbol()); //symbol  
console.log(Symbol(5));//Symbol(5)
console.log(Symbol() == Symbol) //false 
``` 

8. # ``object`` type 
 In JavaScript, an object is a collection of properties, where each property is defined as a key-value pair.

```js
// Defines an empty object
let obj = {};

// Defines the person object with two properties: firstName and lastName.
let person = {
  firstName: "John",
  lastName: "Doe",
};

console.log(person === person);//true 
console.log(person == person );//true
``` 
