1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// function expression
let getPercent = function percentage(marks, total) {
  return (marks * 100) / total;
};

let getPercent = function (marks, total) {
  return (marks * 100) / total;
};

let getPercent = (marks, total) => {
  return (marks * 100) / total;
};

let getPercent = (marks, total) => (marks * 100) / total;
```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

//  Function Declaration
```

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};

// Function Expression
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};

// function expression anonymous
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};

//Arrow Function Expression
```

```js
let percentage = (marks, total) => (marks * 100) / total;
//implicit return Function Expression
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

- The funtion is an object in javascript and we can store any object inside variable. that is why a function definition an expression in JavaScript.
  example -

```js
let addNumbers = function add(a, b) {
  console.log(a + b);
};
```

4. Why is a function call an expression in JavaScript?

- Function call always gives us a value .

5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
} // valid

let five = add(2, 3); // invalid
five = add; // invalid
five = five(10, 11); // invalid
five = function () {
  return "Hello";
}; // valid
```

6. What is the difference between function definition and function call? Explain with an example.

- function defination starts with function keywords.A function is a block of code that does a particular operation and returns a result. It usually accepts inputs as parameters and returns a result. The parameters are not mandatory.
  ex-

```js
function add(a,b)
return a+ b
```

- A function call is the code used to pass control to a function.

```js
add(5, 6);
```

- A function should have its name and paranthesis brackets.
  In a function call there will be a semicolon too.

7. What is the similarities between function definition and function call?

- Both of them should have its name and paranthesis brackets.

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log("Hello World!");
}

hello.user = "Sam"; // valid because all functions are objects.
```

9. What is higher order function explain with an example.

- A function that accepts a function defination as an arguments or returns a function defination from the function are known as higher order function.

```js
let isOdd = function (num) {
  return num % 2 !== 0;
};

// higher order function
function filterOdd(arr, fn) {
  console.log(fn(23));
  return arr;
}

function filterEven(arr) {
  return function () {};
}

filterOdd([1, 2, 3, 5, 67], isOdd);
```

10. Explain what is callback function. Why you can pass a function inside a function?
