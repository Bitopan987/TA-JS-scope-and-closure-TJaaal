1. Create a function by your choice that accepts a callback function.

```js
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 90, 34, 45];

function filter(arr, cb) {
  //Higher Order Function
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(cb(elm));
  }
  return finalArr;
}

let isAdd = function (num) {
  // Callback Function
  return num % 2 == 0;
};

let final = filter(numbers, isAdd);

//2

function outer(cb) {
  return cb(23);
}

outer(function inner(num) {
  return num + 1;
});
```

2. Create a function by you choice that returns a function reference.

```js
function multiplyBy(num) {
  return function (num2) {
    return num * num2;
  };
}

let multiplyBy10 = multiplyBy(10);
console.log(multiplyBy10(20));

//2

function outer() {
  function inner(num) {
    return num + 1;
  }
  return inner;
}

outer();
```

3. Create a higher order function called `map` that takes two inputs:
   - An array of numbers/string/boolean etc
   - A 'callback' function - a function that is applied to each element of the array (inside of the function 'map')

Have `map` return a new array filled with values that are the result of the 'callback' function on each element of the input array.

```js
function map(arr, cb) {
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(cb(elm));
  }
  return finalArr;
}

// Test Your Code
function multiplyByTwo(n) {
  return n * 2;
}
map([1, 2, 3, 4, 5], multiplyByTwo); //-> [2,4,6,8,10]
multiplyByTwo(1); //-> 2
multiplyByTwo(2); //-> 4
```

4. Create a higher-order function called `forEach` taht takes an array and a callback, and runs the callback on each element of the array. `forEach` does not return anything.

```js
function forEach(arr, cb) {
  for (let elm of arr) {
    cb(elm);
  }
}

// Test Your Code
let alphabet = "";
let letters = ["a", "b", "c", "d"];
forEach(letters, function (char) {
  alphabet += char;
});
console.log(alphabet); //prints 'abcd'
```

5. Create higher-order function called `filter` takes an array and a callback, and runs the callback on each element of the array if the return value of callback is `truthy` store in new array return the new array.

```js
function filter(arr, cb) {
  let finalArr = [];
  for (let elm of arr) {
    if (cb(elm)) {
      finalArr.push(elm);
    }
  }
  return finalArr;
}
// Test Your Code

var numbers = [1, 3, 5, 4, 7, 89, 234, 20];
let even = filter(numbers, function (n) {
  return n % 2 === 0;
});
console.log(even); // [4,234,20]
let odd = filter(numbers, function (n) {
  return n % 2 !== 0;
});
console.log(odd); // [1,3,5,7,89]
```