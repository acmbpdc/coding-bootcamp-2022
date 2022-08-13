<p align="center">
  <img src="assets/images/js_logo.png" alt="JavaScript logo" title="JavaScript tutorial" width="200" />
</p>
   # Javascript Session 1
Section 07. Operators
-----------
07.01. What is the Operator?
---------------------
- We know/use many operators since our initial school days, they are things like addition +, multiplication *, subtraction -, open-close round bracket ( ) or square bracket [ ]
- Operators are symbols/keywords that tell the JavaScript engine to `perform some sort of actions`
- JavaScript operators are symbols that are used to perform operations on operands
- Operators used along with our variables and constants to create
expressions to implement logic and algorithms

> **Note**: <br/>
Let us take a simple expression `var sum = 1 + 2`;
- Here 1 and 2 are called `operands` and 
- `=` & `+` are called the `operator`
- `= is the assignment` operator, `+ is the arithmetic` operator

> **Syntax & Example**: `07.01.script.js`
```javascript
// Lets take a look on simple expression 
var sum = 1 + 2;

// Here 1 and 2 are called `operands` and 
// `=` & `+` are called the `operator`
// `= is the assignment` operator, `+ is the arithmetic` operator
```

**JavaScript supports the following types of operators**:
1. Arithmetic Operators
2. Assignment Operators
3. Logical Operators
4. Comparison (or Relational) Operators
5. Conditional (or ternary) Operators
6. String Operators
7. Bitwise Operators

07.02. Arithmetic Operators
----------------------

- Arithmetic operators are used to performing arithmetic operations (just like mathematics - calculations) on numbers/the operands

JavaScript supports the following Arithmetic operators (List of Arithmetic operators):

| Operators | Description                           | Example / Result                                |
| ----------|---------------------------------------|-------------------------------------------------|
| +         | Addition                              | 10 + 20 = 30 (Sum of num1 and num2)             |
| -         | Subtraction                           | 20 - 10 = 10 (Difference of num1 and num2)      |
| *         | Multiplication                        | 10 * 20 = 200 (Product of num1 and num2)        |
| /         | Division                              | 20 / 10 = 2 (Quotient of num1 and num2)         |
| %         | Modulus (Division Remainder)          | 20 % 10 = 0 (Remainder of num1 divided by num2) |
| ++        | Increment                             | var num1 = 100; num1++; Now num1 = 11           |
| --        | Decrement                             | var num1 = 100; num1--; Now num1 = 9            |
| **        | Exponentiation (ES2016 / ES6)         | 2 ** 2 = 4 ; 2 ** 3 = 8 (Multiply num1 for num2 times)  |
| | | |

> **Syntax & Example**: `07.02.script.js`
```javascript
// Arithmetic operators
var num1 = 10;
var num2 = 4;

alert('Addition ' + (num1 + num2)); // 14
alert('Subtraction ' + (num1 - num2)); // 6
alert('Multiplication ' + num1 * num2); // 40
alert('Division ' + num1 / num2); // 2.5
alert('Modulus reminder ' + num1 % num2); // 2
num1++
alert('after Increment ' + num1); // 11
num2--; 
alert('after Decrement ' + num2); // 3

num1 = 10;
num2 = 4;
alert('Exponentiation ' + (num1 ** num2)); // (10 ** 4) = 10* 10 * 10 * 10 = 10000
```

07.03. Assignment Operators
---------------------

- The Assignment operators are used to assign particular values to variables

JavaScript supports the following Assignment operators (List of Assignment operators):

| Operators | Description                           | Example / Result                      |
| ----------|---------------------------------------|---------------------------------------|
| =         | Simple Assignment                     | 10 + 20 = 30; / var total = num1 + num2; (assigns a value to the variable)   |
| +=        | Add and assign                        | var num1 = 10; num1 += 20; Now num1 = 30 (assigns and adds value to the variable, num1 += 20; is equivalent to num1 = num1 + 20;) |
| -=        | Subtract and assign                   | var num1 = 10; num1 -= 5; Now num1 = 5 (assigns and subtract value to the variable, num1 -= 5; is equivalent to num1 = num1 - 5;) |
| *=        | Multiply and assign                   | var num1 = 10; num1 *= 5; Now num1 = 50 (assigns and multiply value to variable, num1 *= 5; is equivalent to num1 = num1 * 5;)    |     
| /=        | Divide and assign                     | var num1 = 10; num1 /= 5; Now num1 = 2 (assigns and divide value to the variable, num1 /= 5; is equivalent to num1 = num1 / 5;)   |
| %=        | Modulus and assign                    | var num1 = 10; num1 %= 5; Now num1 = 0 (assigns and Modulus value to the variable, num1 %= 5; is equivalent to num1 = num1 % 5;)  |
| | | | 

> **Syntax & Example**: `07.03.script.js`
```javascript
// Assignment operators
var num1 = 10;
var num2 = 20

// old methodology
// num1 = num1 + num2;
// console.log(num1); // 30

// new techniques
num1 += num2; 
console.log(num1); // 30

// num2 -= num1; 
// console.log(num2); // 10

// num1 *= num2; 
// console.log(num1); // 200

// num2 /= num1; 
// console.log(num2); // 2
```

07.04. Logical Operators
---------------------

- The Logical operators are used to make decisions based on multiple conditions
- The logical operators are typically used to combine multiple conditional statements and evaluate

JavaScript supports the following Logical operators (List of Logical operators):

| Operators       | Description                           | Example / Result                      |
| ----------------|---------------------------------------|---------------------------------------|
| &&              | Logical AND                           | x && y; (True if both operands like x and y are true) |
| &#124;&#124;    | Logical OR                            | x &#124;&#124; y; (True if either x or y is true)|
| !               | Logical NOT                           | !x; (True if x is not true)           |
| | | |

> **Syntax & Example**: `07.04.01.script.js`
```javascript
// Logical operators - basic examples

// && (Logical AND) - returns true if both operands are true
console.log('true && true: ', true && true);
console.log('true && false: ', true && false);
console.log('false && true: ', false && true);

// ------------------------------

// || (Logical OR) - returns true if one of the operand is true
console.log('true || true: ', true || true);
console.log('true || false: ', true || false);
console.log('false || true: ', false || true);

// ------------------------------

// ! (Logical NOT) True if operand is not true (means I will be true if other is false)
var iamcrazy = true;

var iamnotcrazy = !iamcrazy;
console.log('I am crazy?: ', iamnotcrazy);
console.log('My mother had me tested');
```
<hr/>
<p align="center">
  <img src="assets/images/crazy.png" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>

> **Syntax & Example**: `07.04.02.script.js`
```javascript
// Logical operators - real world scenario/example

// check credit/loan eligibility - (if applicant have HIGH INCOME & GOOD CREDIT SCORE, he is eligible for credit/loan)
var isEarningHighIncome = true;
var isGoodCibilScore = false;
var isEligibleForLoan;

// check eligibility with && Logical AND operator
isEligibleForLoan = isEarningHighIncome && isGoodCibilScore;
alert('isEligibleForLoan: ' + isEligibleForLoan);

// check eligibility with || Logical OR operator
isEligibleForLoan = isEarningHighIncome || isGoodCibilScore;
alert('isEligibleForLoan: ' + isEligibleForLoan);

// ! Logical NOT
var isLoanRefused = !isEligibleForLoan;
alert('isLoanRefused: ' + isLoanRefused);
```

07.05. Comparison (or Relational) Operators
---------------------
07.05. Comparison Operators
---------------------
07.05. Relational Operators
---------------------

- The JavaScript comparison operator compares the two operands
- It compares two values in a Boolean fashion
- The comparison operators are used to determine the similarity and difference between different variables

JavaScript supports the following Comparison (or Relational) operators (List of Comparison (or Relational) operators):

| Operators | Description                           | Example / Result                      |
| ----------|---------------------------------------|---------------------------------------|
| ==  <br/>(Loose Equality Operator)      | Is equal to / identical               | x == y    (True if x is equal to y)     |
| === <br/>(Strict Equality Operator)      | Eqaul/identical value and identical type| x === y (True if x is equal to y, and they are of the same type) |
| !=        | Not equal to / different              | x != y (True if x is not equal to y)           |
| !==       | Not identical    / different value or different type | x !== y )True if x is not equal to y, or they are not of the same type) |
| <         | Less than                             | x < y (True if x is less than y)|
| >         | Greater than                          | x > y    (True if x is greater than y)|
| <=        | Less than or equal to                    | x <= y (True if x is less than or equal to y) |
| >=        | Greater than or equal to                | x >= y (True if x is greater than or equal to y)|
| | | |

> **Syntax & Example**: `07.05.script.js`
```javascript
// Comparison (or Relational) operators
var num1 = 25;
var num2 = 35;
var num3 = "25";
 
alert(num1 == num3);  // true
alert(num1 === num3); // false
alert(num1 != num2);  // true
alert(num1 !== num3); // true
alert(num1 < num2);   // true
alert(num1 > num2);   // false
alert(num1 <= num2);  // true
alert(num1 >= num2);  // false
```

07.06. Conditional (? or ternary) Operator
---------------------
07.06. Conditional Operator
---------------------
07.06. Ternary Operator
---------------------

- Conditional Operator returns a value based on the condition, it is like if-else
- The conditional (ternary) operator is the only JavaScript operator that takes three operands 
- The conditional operator that assigns a value to a variable based on some condition
- This operator is frequently used as a shortcut/short-hand method for the if statement
- **Syntax**: variablename = (condition) ? TRUE value: FALSE value 

| Operators | Description                           | Example / Result                      |
| ----------|---------------------------------------|---------------------------------------|
| ?         | Ternary operator                      | var result = x < y ? 'x is smaller' : 'y is smaller' (short hand method to write if condition)  |
| | | |

> **Syntax & Example**: `07.06.script.js`
```javascript
// Conditional (? or ternary) Operator

// age category
var currentAge = 100;
var category;

category = (currentAge < 18) ? 'Minor' : 'Major';
alert('AGE category: ' + category);

// fees category
var isAuthorisedMember = true;
var fees;

fees = (isAuthorisedMember == true) ? 5 : 10;
alert('fees / charges: ' + fees); 
```

07.07. String Operators
---------------------

Variables can also have string values, `+ operator` can be used to concatenate strings as well as numbers.

There are two operators which can also be used be for strings:

| Operators | Description                           | Example / Result                      |
| ----------|---------------------------------------|---------------------------------------|
| +         | Concatenation                         | string1 + string2 (Concatenation of string1 and string2) |
| +=        | Concatenation assignment              | string1 += string2 (Appends the str2 to the str1) |
| | | |

> **Syntax & Example**: `07.07.script.js`
```javascript
// String Operators
var message1 = "Its your birthday!";
var message2 = " Smile!";
 
alert(message1 + message2); 
 
message1 += message2;
alert(message1); 
```
<p align="center">
  <img src="assets/images/string_concat.png" alt="I haven't watched the show. Hopefully its a meme :)" title="JavaScript tutorial" width="500" />
</p>
   

07.08. Operator precedence
---------------------

- If an expression has more than one operator, the `execution order is defined by their precedence`, or the implicit priority order of operators
- Operator precedence determines/describes the way in which operators are parsed with respect to each other / `order in which operations are performed`
- The operations inside the `parentheses ()` are computed first
- If many operations have the same precedence (like addition and subtraction), they are `computed from left to right`

> **Syntax & Example**: `07.08.script.js`
```javascript
// Operator precedence
var result1 = 10 + 2 * 5
alert('10 + 2 * 5 =  ' + result1); // answer is 20 NOT 60 (12 * 5 ), actually * or multiplication have higher precedence so the actual calculation is like 10 + ( 2*5 ) = 10 + 10 = 20

// change precedence with `parentheses ()` 
var result2 = (10 + 2) * 5;
alert('(10 + 2) * 5 =  ' + result2); // (12) * 5 = 60

// same precedence operators
var result3 = 10 + 5 - 2
alert('10 + 5 - 2 =  ' + result3); // 13 first addition than subtraction

var result4 = 10 + (5 - 2);
alert('10 + (5 - 2) =  ' + result4); // 13 first subtraction ie. ( ) than addition
```

Section 08. Functions
=====================

08.01. What is a Function?
---------------------

- A function is basically a `group of statements that perform specific tasks/operations`
- Functions provide a way to `create reusable code packages` which are more portable and easier to debug
- Functions allow a programmer to `divide a big program` into a number of/several small and manageable functions
- It helps programmers in writing `modular codes`
- The function is a kind of reusable tool where we can write code/functionality to reuse whenever we want (Function allow the code to be called many times without repetition)
- Wrapping up / making smaller chunks of statements / reusable codes together for readability or separation of concern/proper organization is functions – (Grouping of a repetitive task)
- Functions (logical block of code) are one of the most important control structure in any programming language
- In other languages, it might be called `MODULES, SUBROUTINES(SUB-ROUTINES)`
- There are two steps to utilize function: 
  1. create/define a function with `function` keyword  
  2. call/invoke a function

> **Note**: <br/>
Best Practice - First Define function than call/envoke it!

#### 08.01.01. Here are some advantages of using functions:

- **Code reusability** - call a function several times
- **Less coding** - makes our program compact, no need to write lines of code each time
- **Easier to maintain** - changes are done only at one location
- **Easier to eliminate the errors** - fixing errors becomes much easier

#### 08.01.02. Function Definition / Function Declaration / Creating Function

- The function declaration starts by using the `function keyword`, 
- followed by a `unique function name`, 
- a list of `parameters in parentheses` i.e. () (that might be empty), 
- and a statement block surrounded by `curly braces { }`

> **Syntax & Example**: `08.01.script.js`
```javascript
//1. define / declare / create function

function showMessage () {
  //Body of function 
  //code to be executed
  console.log('welcome to JavaScript function');
  alert('welcome to JavaScript function');    
}
```

#### 08.01.03. Function Invocation / Calling a Function / Run a Function

- Defined function can be invoked/called/run from anywhere in the document, by typing `function name followed by a set of parentheses, like functionName()`

> **Syntax & Example**: `08.01.script.js`
```javascript
//2. invoke / call the function

showMessage();
```

#### 08.01.04. Function Naming

Function `denotes an action/task`. The function name should be `brief, as accurate as possible and describe` what the function does, like a `verb`.

Usually, Function name starts with:

- "getSomething" – returns value,
- "createSomething" – create something,
- "calcSomething" – calculate something,
- "checkSomething" – check something and return a boolean, etc.

Examples of function names:
- getSum();
- createFields();
- calcAge();
- checkUserType();

08.02. Types of Function
---------------------

- Regular Function
- Parameterized Function
- Return Type Function (Function returning values)

#### 08.02.01. Regular Function

- Simple/Normal function which we use daily to perform some action/task
<p align="center">
  <img src="assets/images/butter.png" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>

> **Syntax & Example**: `08.02.01.script.js`
```javascript
var food = 'butter';

//1. define / declare / create function
function passButter() {
  //Body of function 
  //code to be executed
  console.log('Please pass the ' + food);
  alert('Please pass the ' + food);    
}

//2. invoke / call the function
passButter();
```

#### 08.02.02.01. Parameterized Function

- One can pass data to functions using parameters (function arguments)
- You can specify parameters when you define your function to accept input values at run time

> **Syntax & Example**: `08.02.02.01.script.js`
```javascript
// Parameterized function
//1. define / declare / create function
function passButter(food) {
  //Body of function 
  //code to be executed
  console.log('Please pass the ' + food);
  alert('Please pass the ' + food);    
}

//2. invoke / call the function
passButter('butter');

passButter('butter!!!');

// ------------------------------

var total;

function calculateSum (num1, num2) {
  total = num1 + num2;
  console.log(total);
}

calculateSum(10, 20);
calculateSum(100, 200);
```

#### 08.02.02.02. Default Values for Function Parameters ES6

With ES6, now you can specify default values to the function parameters. This means that if no arguments are provided to the function when it is called these default parameters values will be used.

> **Syntax & Example**: `08.02.02.02.script.js`
```javascript
// Parameterized function with default parameters

//1. define / declare / create function
function sayHello (name = 'User') {
  //Body of function 
  //code to be executed
  console.log('Hello ' + name);
  alert('Hello ' + name);    
}

//2. invoke / call the function
sayHello();

sayHello('Sheldon');

// ------------------------------

var total;

function calculateSum (num1=1, num2=2) {
  total = num1 + num2;
  console.log(total);
}

calculateSum();
calculateSum(100, 200);
```

#### 08.02.03. Return Type Function (Function returning values)

- A function can `return a value` back to the script that called the `function, as a result, using the return statement`
- We can call a function that returns a value and use it in our program
- The return statement usually placed as the last line of the function

> **Syntax & Example**: `08.02.03.script.js`
```javascript
// Return type function
//1. define / declare / create function
function getSum (num1, num2) {
  //Body of function 
  //code to be executed
  var sum = num1 + num2;
  return(sum);
}

//2. invoke / call the function
console.log(getSum(10,20));
console.log(getSum(100,200));

var total = getSum(50,50);
alert(total);
```

08.03. Different ways to define Function
---------------------

The syntax that we've used before to create functions is called `function declaration`. There is another syntax for creating a function that is called a `function expression` and `Immediately invoked function expression (IIFE)`

#### 08.03.01. function declaration (Regular/Normal function)

#### 08.03.02. function expression

- Variables contain the expressions of a function
  - Anonymous function expression
  - Named function expression

> **Syntax & Example**: `08.03.02.01.script.js`
```javascript
// function declaration (Regular / normal function)
function getSum1(num1, num2) {
  var total = num1 + num2;
  return total;
}

// ------------------------------

// function expression - Anonymus
var getSum2 = function(num1, num2) {
    var total = num1 + num2;
    return total;
};

alert(getSum2(10,20));

// ------------------------------

// assign function to another variable
var sum1 = getSum2;
alert(sum1(100,200));
```

> **Syntax & Example**: 
```javascript
// function expression - named
var getSum2 = function getTotal(num1, num2) {
  var total = num1 + num2;
  return total;
};

alert(getSum2(10,20));

// ------------------------------

// assign function to another variable
var sum1 = getSum2;
alert(sum1(5,10));
```

#### 08.03.03. Immediately invoked function expression (IIFE)

- It runs as soon as the browser finds it
- Declare and run the function at the same time

> **Syntax & Example**: `08.03.03.script.js`
```javascript
// Immediately invoked function expression (IIFE)
(function () {
  console.log('Welcome to Immediately invoked function expression (IIFE)');
}());


(function(userName) {
  console.log('Welcome', userName);
})('Sheldon');
```

08.04. String Methods and Concatenation
---------------------

> **Syntax & Example**: 
```javascript

const firstName = 'Sheldon';
const lastName = 'Cooper'

const fullName = (firstName) + (lastName);
console.log(fullName);
console.log(typeof fullName);

// concatenation
console.log(firstName + ' ' + lastName);

console.log('Hello ' + firstName + ' ' + lastName + 'Welcome to JavaScript!');

// append
let name1 = 'Sheldon ';
let name1 += 'Cooper';
console.log(name1);

// concat() method
console.log(firstName.concat(' ', lastName));

// length
console.log(firstName.length);

// change case
console.log(firstName.toLowercase());
console.log(firstName.toUppercase());

// escaping
// let statement1 = 'wait I'm coming, that's good';
let statement1 = "wait I'm coming, that's good";
let statement2 = 'wait I\'m coming, that\'s good';

// string array - get specific character from string like an array
console.log(firstName[0]);

// indexOf
console.log(firstName.indexOf('i'));
console.log(firstName.lastIndexOf('a'));

// charAt()
console.log(firstName.charAt(2));

// get last character from string
console.log(firstName.charAt(firstName.length - 1));

// replace();
let replaceString = ('Sheldon', 'DJ');
console.log('My name is:', replaceString); 

// substring();
console.log(firstName.substring(0,4));

// slice();
console.log(firstName.slice(0,4));

// slice(); negative number starts from backside
console.log(firstName.slice(-2));

// includes();
let message2 = 'Hello Sheldon, welcome to JavaScript';
console.log(message2.includes('Hello'));
console.log(message2.includes('Hi'));

// split()
let message2 = 'Hello Sheldon, welcome, to JavaScript';
console.log(message2.split(','));
console.log(message2.split(' '));

let courses = 'If I Could, I Would But I Can't So I Shan't';
console.log(courses.split(','));

```
<p align="center">
  <img src="assets/images/split.png" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>
08.05. Template String
---------------------
08.05. Template Literals
---------------------

- ES6 new feature `Strings Template` offers a convenient way to work with string concatenation/interpolation
- Template literals provide an easy and clean way to create multi-line strings and perform string interpolation
- Intuitive expression interpolation for single-line and multi-line strings
- Use `back-tick (grave accent)` character and `{ var name in curly brace }`, no + plus sign required
- The best part of Template Literals (Template Strings) is we can `use 'single' "double" quotes inside`

- It is part of ES6 but compatible with all the modern browsers and its latest versions

> **Syntax & Example**: 
```javascript

//old plain javascript approach
let user = 'Sheldon';
let greetMessage1 = 'Welcome' + ' ' + user + ' ' + 'to JavaScript.';

console.log(greetMessage1);
 
console.log('// ------------------------------');

const firstName = 'Sheldon';
const lastName = 'Cooper'
const course = 'JavaScript'

const fullName = `Hey ${firstName} ${lastName} Welcome to ${course}.`

console.log('// ------------------------------');

//ES6 Template Literals (Template Strings) approach
let greetMessage2 = `Hello ${firstName}, How are you?`;

console.log(greetMessage2);

console.log('// ------------------------------');
// ------------------------------

//ES6 multi-line string
let greetMessage3 = `ES6 Template Literals (Template Strings):
                    With Template Literals (Template Strings)
                    we can add multiple lines in string concatenation/interpolation
`;

console.log(greetMessage3);

let greetMessage4 = ES6 Template Literals (Template Strings):
                    With Template Literals (Template Strings)
                    we can add multiple lines in string concatenation/interpolation
;

console.log(greetMessage4);
```

Section 09. Loops
=====================  
Section 09. Loops and Iterations
=====================

- Loops are used to execute the `same block of code again, with a different value, until a certain condition is met`
- Loops can execute/repeat a block of code (an action) a number of/several times
- The basic idea behind a loop is to `automate the repetitive tasks within a program to save time and effort`
- It makes the `code compact`
- It is mostly used in array or object (to iterate through series)
- Loops/iterations is an instruction repeat until a specific condition is reached

### Different Types of Loops in JavaScript:

1. for loop
2. while loop
3. do...while loop
4. for...in loop
5. for...of loop (ES6)
6. for...each

09.01. The for loop
---------------------

- The `For` loop is used to run a piece of code a `set amount of times`
- Loops through a block of code until the `counter reach a specified number`
- The for loop `repeats a block of code until a certain condition` is met
- The for loop is the most simple/compact form of looping
- For loop consists of 3 statements (), mostly `i = index` is used for loop initialization

> **Syntax & Example**: `09.01.01.script.js`
```javascript
// for loop

/* for (statement 1; statement 2; statement 3) {
  // Code to be executed
} */


/* for(variable definition/index/initialization; condition checking; increment/decrement expression) {
  // Code to be executed
} */

for (let i=1; i<=5; i++) {
  alert('Hello, The current index/num is: ' + i);
  document.write('<li>Hello, The current index/num is: ' + i + '</li>');
  console.log('Hello, The current index/num is: ' + i);
}
```

### 09.01.01. The for loop - Reverse order

> **Syntax & Example**: `09.01.02.script.js`
```javascript
// for loop - reverse order

for (let i = 5; i >= 1; i--) {
  alert('Hello, The current index/num is: ' + i);
  document.write('<li>Hello, The current index/num is: ' + i + '</li>');
  console.log('Hello, The current index/num is: ' + i);
}
```

### 09.01.02. The for loop - Find Even or Odd number

> **Syntax & Example**: `09.01.03.script.js`
```javascript
// for loop - to find out odd even number

for (let i = 1; i <= 10; i++) {
  if (i % 2 == 0) {
    console.log('The current index/num is EVEN : ' + i);
  } /* else {
    console.log('The current index/num is ODD : ' + i);
  } */
}
```

09.02. The while loop
---------------------

- Loops through a block of code until the specified condition evaluates to true
- In For loop, a variable is part of a loop, but in While loop, we need to declare variable externally

> **Syntax & Example**: `09.02.01.script.js`
```javascript
// while loop

/*while(condition) {
  // Code to be executed
}*/

let i = 1;

while (i <= 5) {
  alert('Hello, The current index/num is: ' + i);
  document.write('<li>Hello, The current index/num is: ' + i + '</li>');
  console.log('Hello, The current index/num is: ' + i);
  i++;
}
```

09.03. The do while loop
---------------------
09.03. The do...while loop
---------------------

- The do...while loop is similar to the while loop except that the `condition check happens at the end of the loop`
- The do...while loop will always be `executed at least once (before checking if the condition is true)`, even if the condition is false

> **Syntax & Example**: `09.03.01.script.js`
```javascript
// do...while loop

/*do {
    // Code to be executed
}
while(condition);*/

let i = 1;

do {
  alert('Hello, The current index/num is: ' + i);
  document.write('<li>Hello, The current index/num is: ' + i + '</li>');
  console.log('Hello, The current index/num is: ' + i);
  i++;
}
while (i <= 5); 
```

09.04. The for in loop
---------------------
09.04. The for...in loop
---------------------

- The for-in loop is a special type of a loop that `iterates over the properties of an object or the elements of an array`

<p align="center">
  <img src="assets/images/love.png" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>

#### 09.04.01. The for...in Loop - array

> **Syntax & Example**: `09.04.01.script.js`
```javascript
// for...in loop

/*for(variable/key in array/object) {
    // Code to be executed
}*/

// An array with some elements
let air = ["Nitrogen", "Oxygen", "Carbon Dioxide", "Water Vapour"];

// Loop through all the elements in the array 
for (let love in air) {
  alert('' + air[love] + ' is in the air!');
  document.write('<li>' + air[love] + ' is in the air!</li>');
  console.log('' + air[love] + + ' is in the air!');
}
```

#### 09.04.02. The for...in Loop - object

> **Syntax & Example**: `09.04.02.script.js`
```javascript
// for...in loop

/*for(variable/key in array/object) {
    // Code to be executed
}*/

// An object with some properties 
let objEmployee = {'emp_name': 'Sheldon', 'emp_addres': 'Mumbai', 'emp_id': '029', 'emp_age':35};

// Loop through all the properties in the object  
for (emp in objEmployee) {
  alert('Employee '+ emp + ' is: ' + objEmployee[emp]);
  document.write('<li>Employee '+ emp + ' is: ' + objEmployee[emp] + '</li>');
  console.log('Employee '+ emp + ' is: ' + objEmployee[emp]);
}
```

#### 09.04.03. The for...in Loop - Inbuilt JavaScript objects

> **Syntax & Example**: `09.04.03.script.js`
```javascript
// for...in loop

/*for(variable/key in array/object) {
    // Code to be executed
}*/

// Loop through all the properties in the inbuilt object - window, document, navigator
for (props in window) {
  // alert('document object properties ' + props);
  document.write('<li>document object properties ' + props + '</li>');
  console.log('document object properties ' + props);
}
```

09.05. The for of loop
---------------------
09.05. The for...of loop (ES6)
---------------------

- Loops over `iterable objects such as arrays, strings`, etc.
- ES6 introduces a new for-of loop which allows us to iterate over arrays or strings very easily
- The code inside the loop is executed for each element of the iterable object

> **Syntax & Example**: `09.05.01.script.js`
```javascript
// for...of loop

/*for(element in array/string) {
  // Code to be executed
} */

// Iterating over an array
let arrDays = ["Monday", "TuesDay", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"];

for (let day of arrDays) {
  console.log(day);
  document.write('<li>' + day + '</li>');
}

// Iterating over string
let name = 'JavaScript';
for (let letter of name) {
  document.write(letter + ',');
  console.log(letter + ',');
}
