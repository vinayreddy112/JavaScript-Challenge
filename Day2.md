# DAY 2: **JavaScript Operators**
Welcome to Day 2 of JavaScript Basics! Today, we'll be focusing on JavaScript operators. This includes arithmetic, assignment, comparison, logical, and ternary operators. 
## Activity 1: Arithmetic Operations 
``Task 1``: Write a program to add two numbers and log the result to the console. 
```javascript
let a = 2;
let b = 3;
console.log(a+b); //5
console.log(typeof(a+b)); // number 
```
`Task 2`: Write a program to subtract two numbers and log the result to the console. 
```javascript
let a = 2;
let b = 3;
console.log(a-b); //-1
console.log(typeof(a-b)); // number 

``` 
`Task 3`: Write a program to multiply two numbers and log the result to the console. 
```javascript
let a = 2;
let b = 3;
console.log(a*b); //6
console.log(typeof(a-b)); // number 


```
``Task 4``: Write a program to divide two numbers and log the result to the console.

```js 
let a = 2;
let b = 3;
console.log(a/b); //0.6666666666666666  return floating value
console.log(typeof(a/b)); // number 
```
``Task 5``: Write a program to find the remainder when one number is divided by another and log the result to the console. 
```js
let a = 5;
let b = 2;
console.log(a%b); //1
console.log(typeof(a%b)); // number 
```
> ```**``` operator is used for exponent   ```5**2 = 25```
## Activity 2: Assignment Operators
``Task 6``: Use the += operator to add a number to a variable and log the result to the console.
```js 
let a = 5;
let b = 2;
console.log(a+=b); //7  it implicitly a=a+b;
```
```js
let a = 5;
let b = 2;
a+=b// a=a+b
console.log(a); //7  
```
```Task 7```: Use the -= operator to subtract a number from a variable and log the result to the console.
```js
let a = 5;
let b = 2;
a-=b// a=a-b
console.log(a); //3
```
> += , -= , /= , %= .. etc. 

## Activity 3: Comparison Operators  
``Task 8``: Write a program to compare two numbers using > and < and log the result to the console.
```javascript 
let a = 5;
let b = 2;
console.log((a > b )+" "+ (a < b)); // true false 
```
``Task 9``: Write a program to compare two numbers using >= and <= and log the result to the console. 
```js
let a = 5;
let b = 10;
console.log((a>=b) +" "+ (a<=b));//false true 
```
``Task 10``: Write a program to compare two numbers using == and === and log the result to the console.
```js
let a = 5;
let b = '5';
console.log(a == b); // true -> because == does type coercion
/* 
 == this operator only checks value But not its type
*/
console.log(a == b);// false ->because === checks for strict  equality 
/*
 === this operator is used to compare the equallity of two operands with type.
*/

```
## Activity 4: Logical Operators 
```Task 11```: Write a program that uses the && operator to combine two conditions and log the result to the console.
```js 
let a = true;
let b = false;
console.log("a && b:", a && b); // a && b: false -> because both conditions are not true
```
```js
let a = true;
let b = true;
console.log("a && b:", a && b); // a && b: true -> because both conditions are  true
```
```Task 12```: Write a program that uses the || operator to combine two conditions and log the result to the console. 
```js
let a = true;
let b = false;
console.log("a || b:", a || b); // a || b: true -> because at least one condition is true
```
```js
let a = false;
let b = false;
console.log("a || b:", a || b); // a || b: false -> because at least one condition is true
```
```Task 13```: Write a program that uses the ! operator to negate a condition and log the result to the console.
```js
let a = true;
console.log(!(a));//false
console.log(!a);//false
```

## `false` values and `true` values
>Here  **>0 and <0**  values are `true`.
```js
let a = 1; //
console.log(a && true);//true
console.log( false || a);//1
console.log(a && false);//false

```
```js
let a = 2; //
console.log(a && true);//true
console.log( false || a);//2
console.log(a && false);//false
```
```js
let a = -1; //
console.log(a && true);//true
console.log( false || a);//-1
console.log(a && false);//false
```
>Here  **0**  values are `false`.
```js
let a = 0; //
console.log(a && true);//0
console.log( false || a);//0
console.log(a && false);//0
```
>Here  **"vinay"**  values are `true`.
```js
let a = "vinay"; //
console.log(a && true);//true
console.log( false || a);//vinay
console.log(a && false);//false 
console.log("vinay" &&"sravan"); //sravan 
console.log("sravan" &&"vinay"); //vinay 
/*
console.log(1 && 2) ;//2
using && operator with same type if it is not falsy values it returns left && operator left side.
console.log(0 && 2); // 0  
here 0 is the falsy value return it

*/
``` 
>Here  **""**  values are `false` value.
```js
let a = "";
console.log(!a);//true
console.log( a && "vinay");//""
``` 
>Here **null** values are `false` value.
```js
let a = null;
console.log(!a);//true
console.log( a && 1);//null
console.log(a && true);//null
console.log(a || true);//true
console.log(a && "vinay");//null
```
> Here **undefined** values are `false` value. 
```js
let a;
console.log(!a);//true
console.log( a && 1);//undefined
console.log(a && true);//undefined
console.log(a || true);//undefined
console.log(a && "vinay");//undefined
```
> Here **NaN** values are `false` value. 

```js 
let a = NaN;
console.log(!a);//true
console.log( a && 1);//Nan
console.log(a && true);//NaN
console.log(a || true);//NaN
console.log(a && "vinay");//Nan
```
## Activity 5: Ternary Operator 
```Task 14```: Write a program that uses the ternary operator to check if a number is positive or negative and log the result to the console.
```js
let num = -5;
let result = num > 0 ? "Positive" : "Negative";
console.log("The number is:", result); // The number is: Negative
```
```js
let num = 5;
let result = num > 0 ? "Positive" : "Negative";
console.log("The number is:", result); // The number is: Positive
```
## Achievements: 
- By the end of these activities, students will:

- Understand and use arithmetic operators to perform basic calculations.
- Use assignment operators to modify variable values.
- Compare values using comparison operators.
- Combine conditions using logical operators.
- Use the ternary operator for concise conditional expressions.