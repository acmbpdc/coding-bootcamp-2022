<p align="center">
  <img src="assets/images/js_logo.png" alt="JavaScript logo" title="JavaScript tutorial" width="200" />
</p>

<center><h1>Javascript Session 2</h1></center>

Section 03.06 Break and Continue Statements
----------  

03.06. Break and Continue statement
---------------------

- `break` and `continue` keywords/statement can change `how the loop behaves`
- `break` and `continue` keywords can be used in all loops to stop or continue the loop
- The `break` statement is used to exit a loop early, to "jump out" of a loop, stops executing/running a loop
- The `continue` statement tells the interpreter to immediately start the next iteration of the loop and skip the remaining code block

> **Syntax & Example**
```javascript
// break continue statement

/* break */
let arrDays = ["Monday", "TuesDay", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"];

let i = 1;
while (i <= 10) {
  if (i == 5) {
    break;
  }
  console.log(i);
  i++
}

console.log('// ------------------------------');

for (let i = 0; i <= arrDays.length; i++) {
  if (i == 3) {
    break;
  }
  console.log(arrDays[i]);
}

console.log('// ------------------------------');

/* continue */
i = 1;
while (i <= 20) {
  if (i % 2 == 0) {
    // console.log('Even Number ', i);
    i++;
    continue; // skip rest of the loop body

    i + 100; // non of use 
    console.log('just in even num continue'); // non of use 
  }
  console.log('Odd Number ', i);
  i++;
}

console.log('// ------------------------------');

for (i = 1; i <= 10; i++) {
  if (i === 5) {
    continue; // skip rest of the loop body
    console.log('just after 5 continue...'); // non of use 
  }
  console.log(i);
}

console.log('// ------------------------------');

for(let int = 0; int < 10; int++) {

  if(int === 2) {
    console.log('2 is favorite EVEN number');
    continue;
  }

  if(int === 5) {
    console.log('at 5 stop the loop');
    break;
  }

  console.log('current Number is:', int); 
}

```

03.07. for each loop
---------------------
03.07. for...each loop
---------------------

> **Syntax & Example**: ``
```javascript

let arrDays = ["Monday", "TuesDay", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"];

arrDays.forEach(function(day)){
  console.log(day);
}

```


Section 4. Conditions - Control Flow
=====================

- Conditional statements are used to perform different action based on different condition
- Conditional statements allow the developer to make correct decisions and perform right actions as per condition
- It helps to perform different actions for different decisions
- We can use conditional operator to check our condition: >, <, >=, <=, ==, !=, ===

#### We can use the following conditional statements in JavaScript to make decisions:

1. If Statement
2. If...else Statement
3. If...else if...else Statement
4. Switch...Case Statement

04.01. The if statement
---------------------
04.01. The if statement and comparison operators
---------------------

- If the conditional statement is the simplest and basic control statement make decisions and execute statements conditionally
- The if statement is used to execute a block of code `only if the specified condition evaluates to true`
- It evaluates the content only `if an expression is true`

If conditional statements are used to evaluate some kind of condition and do something/perform some actions based on the result

> **Note**: <br/>
Use `if` to specify a block of code to be executed, `if a specified condition is true`

> **Syntax & Example**
```javascript
// if conditional statement

/*if(condition/expression) {
  // Code to be executed if condition/expression is true
}
*/

let user = 'Sheldon';

if (user == 'Sheldon') {
  console.log('Welcome Sheldon!');
  window.alert('Welcome Sheldon!');
}

if (user == 'Sheldon') {
  console.log('Welcome Authorised User: ' + user + '!');
  window.alert('Welcome Authorised User: ' + user + '!');
}

// ------------------------------

let age = 20;

if (age >= 18) {
  console.log('MAJOR! Eligible for Voting');
  window.alert('MAJOR! Eligible for Voting');
}

// ------------------------------

let currentHours = 10;

if(currentHours < 12) {
  console.log('Good Morning!');
  window.alert('Good Morning!');
}

if(currentHours >=6 && currentHours < 12) {
  console.log('Good Morning!');
  window.alert('Good Morning!');
}
```

04.02. The if else statement
---------------------

- The JavaScript `if...else statement` is used to execute the code `weather condition is true or false`
- The developer can enhance the decision-making capabilities by providing an alternative choice through adding an `else` statement to the `if` statement
- The condition can be any expression that evaluates to true or false
- If the condition evaluates to true, statements_1 are executed; otherwise, statements_2 are executed

> **Note**: <br/>
Use `else` to specify a block of code to be executed, `if the same condition is false`

> **Syntax & Example**
```javascript
// if...else conditional statement

/*if(condition/expression){  
// content to be executed if condition is true - statements_1  
}  
else{  
// content to be executed if condition is false - statements_2
}*/

let user = 'Ambar';

if (user == 'Sheldon') {
  console.log('Welcome Sheldon!');
  window.alert('Welcome Sheldon!');
} else {
  console.log('Welcome Guest!');
  window.alert('Welcome Guest!');
}

// ------------------------------

let age = 15;

if (age >= 18) {
  console.log('MAJOR! Eligible for Voting');
  window.alert('MAJOR! Eligible for Voting');
} else {
  console.log('MINOR! NOT Eligible for Voting');
  window.alert('MINOR! NOT Eligible for Voting');
}

// ------------------------------

let currentHours = 10;

if(currentHours < 12) {
  console.log('Good Morning!');
  window.alert('Good Morning!');
} else {
  console.log('Good Evening!');
  window.alert('Good Evening!');
}
```

04.03. The if else if else statement
---------------------

- The `if...else if...else` a special statement that is used to `combine multiple if...else statements`
- It is an advanced form of if...else that allows us to `make a correct decision out of several conditions`

> **Note**: <br/>
Use `else if` to specify a new condition to test, `if the first condition is false`

> **Syntax & Example**
```javascript
// If...else if...else conditional statement

/*if(condition/expression 1) {
    // Code to be executed if condition1 is true statements_1
} else if(condition/expression 2) {
    // Code to be executed if the condition1 is false and condition2 is true statements_2
} else {
    // Code to be executed if both condition1 and condition2 are false statements_3
}*/

let num1 = 200;
let num2 = 100;

if (num1 == num2) {
  console.log('Both numbers are equal');
} else if (num1 < num2 ) {
  console.log('Number2 is greater!');
} else {
  console.log('Number1 is greater!');
}

// ------------------------------

let age = 15; 

if (age >= 60) {
  console.log('SINIOR CIRIZEN!');
} else if (age < 18) {
  console.log('MINOR!');
} else {
  console.log('MAJOR - Middle Age!');
}

// ------------------------------

let currentHours = 15;

if(currentHours >=6 && currentHours< 12) {
  console.log('Good Morning!');
  window.alert('Good Morning!');
} else if (currentHours >12 && currentHours <=18) {
  console.log('Good AfterNoon!');
  window.alert('Good AfterNoon!');
} else {
  console.log('Good Evening!');
  window.alert('Good Evening!');
}
```

04.04. The switch case statement
---------------------

- The switch...case statement is alternative to an if...else if...else statement, both do almost the same thing
- This matches the `case` and the `value of condition` and if the case matches, the subsequent block is executed and if none of the case matches `default block` is executed
- The JavaScript switch statement is used to execute one code from multiple blocks of expressions

> **Note**: <br/>
Use `switch` to specify many `alternative blocks of code to be executed`

> **Syntax & Example**
```javascript
// switch...case conditional statement

/* switch(variable/expression){
  case value1:
    // Code to be executed if variable/expression === value1
    break;
  case value2:
    // Code to be executed if variable/expression === value2
    break;
  default:
    // Code to be executed if variable/expression is different from all values
} */

let grade = 'B'; // A.B,C, or something

switch (grade) {
  case 'A':
    console.log('Great Job! - A Grade');
    break;
  case 'B':
    console.log('Good! - B Grade');
    break;
  case 'C':
    console.log('Congratulations! - Passed');
    break;
  default:
    console.log('Sorry! - Failed...Keep trying!');
    break;
}

// ------------------------------
```
<p align="center">
  <img src="assets/images/food.png" alt="JavaScript logo" title="JavaScript tutorial" width="300" />
</p>

``` javascript
let sweets = ''; //cake, chocolates, biscuits

switch (sweets) {
  case 'chocolates':
    console.log('Chubby Chocolates!');
    break;
  case 'cake':
    console.log('Happy BirthDay Cake!');
    break;
  case 'biscuits':
    console.log('Enjoy Biscuits!');
    break;
  default:
    console.log('No Sweets! Try some other sweets!');
    break;
}
``` 
``` javascript
const color = 'red';

switch(color) {
  case 'red':
    console.log('The Dark RED');
    break;
  case 'green':
    console.log('Go Green');
    break;
  case 'blue':
    console.log('Boys are Blue');
    break;
  case 'yellow':
    console.log('Golden Yellow');
    break;
  default:
    console.log('Its some other Color, Enter correct color');
    break;
}
```
``` javascript
let currentDate = new Date();
let currentDay;

switch(currentDate.getDay()) {
  case 0:
    currentDay = 'Sunday';
    break;
  case 1:
    currentDay = 'Monday';
    break;
  case 2:
    currentDay = 'Tuesday';
    break;
  case 3:
    currentDay = 'Wednesday';
    break;
  case 4:
    currentDay = 'Thursday';
    break;
  case 5:
    currentDay = 'Friday';
    break;
  case 6:
    currentDay = 'Saturday';
    break;
}

console.log(`Today is ${currentDay}!`);

```
<p align="center">
  <img src="assets/images/bazinga.png" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>

04.05. Objects in  Javascript 
---------------------
04.05.01 Objects
- An object in javascript is a variable that can have multiple attributes and methods.
- Attributes of objects are values that represent different features of that  class.
- Methods of objects are actions that can be performed by the class using functions.

> **Syntax & Example**
> Let us make an object to represent a person, we will begin with atributes of the person such as their name and age.
```javascript
const person = {
  firstName: "Sheldon",
  lastName : "Cooper",
  age      : 35
};

// We can view these atributes with the syntax variable_name.atribute_name
console.log("The name of this person is: " + person.firstName + " " + person.lastName);
```

> We can also alter these atributes to update their values
```javascript
console.log("Current age: " + person.age);

person.age += 1;

console.log("Current age: " + person.age);
```

> Javascript also allows us to add and remove atributes of a class
```javascript
// We can add an atribute using the syntax variable_name.atribute_name = value
person.iq = 187;
console.log("Sheldon's iq: " + person.iq);

// We can also delete these atributes using the delete keyword
delete person.iq;

// This line will now give us an error as the atribute has been deleted
console.log("Sheldon's iq: " + person.iq);
```
> If we need to check if and object has a paticular atribute we can use the hasOwnProperty method which is inbuilt into all classes

```javascript
console.log("Do we have this person's iq?\n" + person.hasOwnProperty("iq"));
```


- We can now add our own methods to our class using functions
```javascript
const person = {
  firstName: "Sheldon",
  lastName : "Cooper",
  age      : 35,
  greetPenny : function() {
   for (let i = 0; i < 3; i++) {
        console.log("Hey Penny!");
    }
  }
};

person.greetPenny(); // This calls the method greetPenny 
```

<p align="center">
  <img src="assets/images/hello_penny.jpeg" alt="JavaScript logo" title="JavaScript tutorial" width="400" />
</p>


04.05.02 Lookup Tables

> In javascript, we can use objects to create a lookup or mapping between different values.
> A lookup is a variable that maps an input value to a paticular output value.

```javascript
// This is a lookup table that maps names to mobile numbers
var mobile_number_lookup = {"Penny":58538902, "Raj" : 98745689, "Sheldon" : 789023456};

// To get the corresponding mobile number from a name we use the syntax variable[input value]
console.log("Raj's number is: ", mobile_number_lookup["Raj");
```
04.05.03 Object Freeze
> If we want to prevent our object or lookuptable from having any future changes, we make use of the Object.freeze function.
```javascript
const person = {
  firstName: "Sheldon",
  lastName : "Cooper",
  age      : 35
};
// We can chage atributes like normal
person.age = 37;
console.log(person.age);

// We now freeze to prevent future changes
Object.freeze(person);

// This will not take effect since this object is now frozen
person.age = 35;

console.log(person.age);
```


04.06. Regular Expressions (RegEx) in  Javascript 
---------------------

> Regular Expressions is a type of format for strings that allows you to easily find and replace characters as you like.

04.06.01 Search
> The search method allows us to get the index of the substring in the text. 
> Note that this search is regardless of case sensitivity.

```javascript
var text = "Big Bang Theory";

console.log(text.search(/Theory/i));
```

04.06.02 Replace
> The replace method allows us to replace a substring with any string of our choice.

```javascript
var text = "Big Bang Theory";

console.log(text.replace(/Big/i, "Massive"));
```

04.06.03 The Test Method
> This checks if the substring contains a string that meets the following criteria.
```javascript
var expression = /Season 1/ // this expression will return true for all strings with the term Season 1

console.log(expression.test("Season 1 Episode 12"));
console.log(expression.test("Season 2 Episode 12"));
```

04.06.04 The | Operator
> This operator searches for any of the alternatives provided by the user
```javascript
var expression = /Season 1|Season 2/g // this expression will return true for all strings with Season 1 or Season 2

console.log(expression.test("Season 1 Episode 12"));
console.log(expression.test("Season 2 Episode 12"));
console.log(expression.test("Season 3 Episode 12"));
```
04.06.05 The Match Function
> This returns all instances where a substring matching the regex expression is found.
```javascript
var text = "Big Bang Theory";

console.log(text.match(/Big/g));
```

04.06.06 RegEx Wildcards
> Wildcards are placeholders that can represent multiple characters in a string.

* \d represents numbers
* \s represents whitespace
* \b represents the beginning of a word
*  \* represents zero or more whitespaces
* \A represents the start of a string
* [a-z | A-z] can represent any character
```javascript
var expression = /[a-z | A-z]/g // checks if the string contains an alphabet

console.log(expression.test("a"));
console.log(expression.test("xy"));
console.log(expression.test("1"));
```

Section 11. Promise
=====================  

## What is a promise?

Why is a JavaScript ES6 `promise` called a 'promise'? Here is a snippet from the *Oxford Dictionary of English* definition of 'promise':

> **promise** |ˈprɒmɪs|<br>
noun<br>
1 a declaration or assurance that one will do something or that a particular thing will happen

This pretty well sums up what a promise means in JavaScript: something that will be delivered in the future (if and when the promise is *fulfilled*).

Traditionally, *callbacks* are used as a way to receive the data that is delivered asynchronously (meaning that the data is not likely to be available at the time it is requested but can be expected some time later). Using callbacks can quickly become unwieldy when dealing with many asynchronous events (e.g., ajax calls), especially when they depend on each other (google for *callback hell*).

JavaScript ES6 introduces promises as a better alternative for callbacks when dealing with asynchronous events.

We can state a number of simple facts about ES6 promises:

- A promise is a JavaScript object (`typeof somePromise === 'object'`) that serves as a placeholder for a (future) value.
- Because a promise is an ordinary JavaScript object you can pass it around as an argument to a function, return it from a function, assign it to a variable, push it to an array, etc.
- You can receive the 'promised' value by calling the `.then()` method of the promise, passing it a function that will receive that value as its argument as soon as it is available.
- You can create a promise by calling the ES6 `Promise` constructor function with `new` (see Listing 1 below), then call `resolve()` when results are ready or `reject()` on detecting an error.
- Sometimes you can get a ready-made promise by calling an appropriate API or library function, like the `fetch()` Web API function in Listing 1.
- Internally, a promise can be in one of three states:
   - **pending**: the asynchronous result is still awaiting delivery
   - **fulfilled**: the asynchronous result has been delivered and is available (`resolve()` was called)
   - **rejected**: an error was encountered: the promise could not be fulfilled (`reject()` was called)
- A promise that is no longer pending because it was either fulfilled or rejected is said to be _settled_.
- A promise that is _settled_ has reached its final state. Its state and value can no longer be changed. It has become _immutable_. Subsequently calling `resolve()` or `reject()` does no longer affect the outcome of the promise.

## Example code

Listing 1 shows an example based on an asynchronous XMLHttpRequest that we will use throughout the rest of this discussion.

```js
'use strict';

function fetchJSON(url) {
  return new Promise((resolve, reject) => {
    const xhr = new XMLHttpRequest();
    xhr.open('GET', url);
    xhr.responseType = 'json';
    xhr.onreadystatechange = () => {
      if (xhr.readyState === 4) {
        if (xhr.status < 400) {
          resolve(xhr.response);
        } else {
          reject(new Error(xhr.statusText));
        }
      }
    };
    xhr.send();
  });
}

// alternative:
// const fetchJSON = url => fetch(url).then(res => res.json());

const url = 'http://api.nobelprize.org/v1/laureate.json?gender=female';

fetchJSON(url)
  .then(data => renderData(data))
  .catch(err => renderError(err));

function renderData(data) {
  console.log(data);
}

function renderError(err) {
  console.error(err.message);
}
```

Listing 1. Asynchronous `XMLHttpRequest` (and `fetch` alternative) using a promise.

The `fetchJSON()` function in Listing 1 returns a `promise` that resolves to a value converted from JSON data received from a remote API end point. The alternative version of `fetchJSON()` (commented out here) uses a more modern browser function that natively returns a promise.


## The .then() method

A promise exposes a `.then()` method through which you can obtain its fulfilled value or an error value in the case the promise was rejected:

```js
somePromise.then(onFulfilled, onRejected);
```

The `.then()` method takes as its parameters two **optional** functions, the first one dealing with the 'happy' scenario (the promise is fulfilled) and the second one dealing with the error case (the promise is rejected). If you are only interested in the success case you can leave out the second parameter:

```js
somePromise.then(data => {
  // ...
});
```

If you are only interested in the error case, you can pass `null` for the first argument:

```js
somePromise.then(null, err => {
  //...
});
```

or you can use another method available on a promise, `.catch()`, which is just a shorthand for calling `then()` with `null` as its first argument:

```js
somePromise
  .then(data => {
    // ...
  })
  .catch(err => {
    // ...
  });
```

Note that the `onFulfilled` and `onRejected` handler functions always execute asynchronously. When the promise is settled, the `onFulFilled` or `onRejected` handler is placed on the event/callback queue. They execute when the currently executing JavaScript code runs to completion, causing the [call stack](./event_loop.md#call-stack) to become empty and enabling the event loop to process the next event from the queue. This holds true even if the promise is immediately fulfilled or rejected, as in this example:

```js
Promise.resolve(42)
  .then(data => console.log(data));

console.log('after promise');

// console output:
// after promise
// 42
```

This example also shows how you can create a promise that is immediately resolved. There is no need to use `new` or to pass a `(resolve, reject) => {}` function to the `Promise` constructor. Similarly you can create a promise that is immediately rejected:

```js
Promise.reject(new Error('oops'))
  .catch(err => console.log(err.message));

console.log('after promise');

// console output:
// after promise
// oops
```

## Promise chaining

It is important to understand that the `.then()` method returns a new promise that resolves to the return value of `onFulfilled` (if specified) in case of the 'happy' scenario or the return value of `onRejected()` (if specified) in case of an error. If the return value of these functions is a plain JavaScript value, the new promise is immediately fulfilled with that value. If the return value is yet another promise then the outcome is determined by the inner promise, once settled. If the function does not return a value, the new promise is immediately fulfilled with the value `undefined`.

Because `.then()` (and `.catch`) return new promises, you can chain them together such that your code can be read as: do *this*, then do *that* and then *that*, etc.:

```js
function fetchAndRender(url, otherUrl) {
  fetchJSON(url)
    .then(data => {
      renderData(data);
      return fetchJSON(otherUrl);
    })
    .then(otherData => {
      renderOtherData(otherData);
    })
    .catch(err => {
      renderError(err);
    });
}

fetchAndRender();
```

Listing 2. Chaining of `then` and `catch`

Let's examine Listing 2 in a bit more detail. There two calls to `fetchJSON()`. Errors are handled in one place, by means of the `.catch()` method that terminates the promise "chain".

If you embed another promise inside the function that you pass to the `.then()` method (in Listing 2 this is done in the first `.then()`) you should return that promise as the function's return value. If you don't return the promise, there is no way for the `.catch()` at the end of the chain to "see" a `reject()` of the inner promise, leaving the rejection unhandled.

In case a promise in the chain is rejected due to some error, the promise chain will be traversed until an `onRejected` handler (e.g., in a terminating `.catch()` method) is found. All intermediate `onFulfilled` handlers (e.g. `.then()`) will be skipped.

Handling errors at the end of a promise chain is a major advantage over the repetition of error handling code in the case of callbacks.

Note however that a `.catch()` method does not necessarily have to be the last method in the chain. It can be used to handle errors midway. As mentioned previously, the `.catch()` method returns a new promise which can be used to provide some "fallback" value in case of errors.

In the example below a promise is created that is immediately rejected. The promise is subsequently "consumed" twice.

1. In the first case ('consumer 1'), the rejection is caught by a `.catch()` method and the rejection value `'bad'` is printed on the console.

2. In the second case ('consumer 2'), the rejection is also caught by a `.catch()` method, but now the catch handler completely ignores the rejection value and just returns the fallback value `'good.`. This becomes the fulfilled value of the promise returned by `.catch()`. The next `.then()` in the chain, completely oblivious that an error ever occurred, now prints the fulfilled value `'good'` on the console.

```js
const promise = Promise.reject('bad');

// consumer 1
promise
  .catch(console.log); // -> "bad"

// consumer 2
promise
  .catch(() => 'good')
  .then(console.log); // -> "good"
```

## Promise.all()

There may be situations where you want to execute multiple promises in parallel and wait until all promises are resolved. Of course, these promises must not be interdependent (i.e. a promise must not depend on the result of another promise running in parallel). The `Promise.all()` method accepts an array (or more precisely, an _iterable_) of promises. It return a new promise that is resolved when all promises in the array are resolved, or rejected as soon as one of the promises in the array is rejected.

The fulfilled value of the new promise is an array of fulfilled values of the individual promises passed to `Promise.all()`, in the same order.

Project
=====================  
[Click here](https://anuragkj.github.io/JS_Project/) for a simple project made by the concepts we learnt till now. Try making more!!