# **Day 3: Control Structures in JavaScript**  
## **Activity 1: If-Else Statements**
`Task 1`: Write a program to check if a number is positive, negative, or zero, and log the result to the console. 
```javascript 
let num = 0;
if(num>0){
    console.log(` number is positive`);
}
else if(num < 0){
    console.log(`number is negaive")`);
}
else{
    console.log(`number is zero`);
}

```
## **Activity 2: Nested If-Else Statements** 
`Task 3`: Write a program to find the largest of three numbers using nested if-else statements. 

```javascript 
let a = 5;
let b = 6;
let c = 7;
if(a >= b){
    if(a>=c){
        console.log(`${a} is greater`);
    }else{
        console.log(`${c} is greater`);

    }

}
else if(b>=c){
    if(b>=a){
        console.log(`${b} is greater`);
    }else{
        console.log(`${a} is greater`);
    }
}else if(c>=a){ 
    if(c>=b){
        console.log(`${c} is greater`);
    }else{
        console.log(`${b} is greater`);
    }

}  //output: 7 is greater 
```
## **Activity 3: Switch Case**   
`Task 4`: Write a program that uses a switch case to determine the day of the week based on a number (1-7) and log the day name to the console.
```javascript 
function getDayOfWeek(dayNumber) {
  switch (dayNumber) {
    case 1:
      console.log("Sunday");
      break;
    case 2:
      console.log("Monday");
      break;
    case 3:
      console.log("Tuesday");
      break;
    case 4:
      console.log("Wednesday");
      break;
    case 5:
      console.log("Thursday");
      break;
    case 6:
      console.log("Friday");
      break;
    case 7:
      console.log("Saturday");
      break;
    default:
      console.log("Invalid day number. Please enter a number between 1 and 7.");
  }
}

getDayOfWeek(1); // Output: Sunday
getDayOfWeek(5); // Output: Thursday


``` 
>`Java`: __switch works with int, char, String, and enum types__ (since Java 7).

`JavaScript`:
- JavaScript: switch works with any data type (string, number, boolean, object, etc.), even complex types like Array or Object.
-  JavaScript uses strict equality (===) in switch, meaning the data types must match exactly. For example, case "5" won't match switch(5), because one is a string and the other is a number.
```javascript 
let value = "5";

switch (value) {
  case 5:
    console.log("This won’t match because 5 is a number.");
    break;
  case "5":
    console.log("This will match because it's a string.");
    break;
  default:
    console.log("No match");
}
/*
output :
This will match because it's a string.
*/
```
- The default case is conventionally placed at the end, but JavaScript allows it to appear anywhere:
```javascript 
let number = 3;
switch (number) {
  default:
    console.log("No match found.");
    break;
  case 1:
    console.log("One");
    break;
  case 3:
    console.log("Three");
    break;
}
/*
 output :
 Three
*/  


```
 - `Limitations` 
    1. `Strict Equality Only`: JavaScript’s switch uses strict equality (===), so type mismatches will result in unexpected results.
Unintended Fall-Through:
   2.  `If you forget a break`, JavaScript will continue executing the next case, which can introduce bugs if unintentional.
   3. `Limited to Constant Cases`: While expressions can be used in cases, complex conditions (like case x > 5) aren’t allowed. You’ll need if-else chains for those.
   4. `Readability in Complex Logic`: For more complex branching, switch can become harder to read and maintain, so if-else might be preferable.

`Task 5`: Write a program that uses a switch case to assign a grade ('A', 'B', 'C', 'D', 'F') based on a score and log the grade to the console. 
```javascript
function getGrade(score) {
  let grade;
  switch (true) {
    case score >= 90:
      grade = "A";
      break;
    case score >= 80:
      grade = "B";
      break;
    case score >= 70:
      grade = "C";
      break;
    case score >= 60:
      grade = "D";
      break;
    default:
      grade = "F";
  }
  console.log(`The grade is ${grade}.`);
}

getGrade(85); // Output: The grade is B.
getGrade(72); // Output: The grade is C.

```
 ## Activity 4: **Conditional (Ternary) Operator**  
 `Task 6`: Write a program that uses the ternary operator to check if a number is even or odd and log the result to the console. 
 ```javascript
 let num = 2;
 let result = num%2==0?"even Number":"Odd Number";
 console.log(result) ; //even Number
```
## Activity 5: **Combining Conditions** 
``Task 7``: Write a program to check if a year is a leap year using multiple conditions (divisible by 4, but not 100 unless also divisible by 400) and log the result to the console.
```javascript 
let year = 2024;
if(year%4==0&&year%100!=0||year%400==0){
    console.log(`${year} is leap year!`);
}
else{
    console.log(`${year} is  not a leap year!`);

}

```

## **Feature Request:**
1. **Number Check Script**: Write a script that checks if a number is positive, negative, or zero using if-else statements and logs the result.
2. **Voting Eligibility Script**: Create a script to check if a person is eligible to vote based on their age and log the result.
3. **Day of the Week Script**: Write a script that uses a switch case to determine the day of the week based on a number (1-7) and logs the day name.
4. **Grade Assignment Script**: Create a script that uses a switch case to assign a grade based on a score and logs the grade.
5. **Leap Year Check Script**: Write a script that checks if a year is a leap year using multiple conditions and logs the result.
## **Achievements**:
 - By the end of these activities, students will:

- Implement and understand basic if-else control flow.
- Use nested if-else statements to handle multiple conditions.
- Utilize switch cases for control flow based on specific values.
- Apply the ternary operator for concise condition checking.
- Combine multiple conditions to solve more complex problems.

