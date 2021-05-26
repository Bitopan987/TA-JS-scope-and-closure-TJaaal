Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = "Arya";
}
console.log(useranme); //  username is not defined
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = "Arya";
}
console.log(useranme); // ReferenceError: useranme is not defined
```

In above code we are looking for the variable named `usename`. The variable is inside block scope using const and we can't access the variable defined inside a block from outside.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = "Arya";
}
console.log(useranme); // ReferenceError: username is not defined
```

here let creates scope inside the if block. 4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = "Arya";
}
console.log(username); // "Arya"
```

here var does not creates scope inside the if block.we can excess username.

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  var username = "Arya";
}
console.log(username); // Identifier 'username' has already been declared
```

we cant't declare twice with the same name.

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
if (true) {
  let username = "Arya";
}
console.log(useranme); // "John"
```

username john is in global scope.

7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = "John";
function sayHello() {
  let username = "Arya";
}
sayHello();
console.log(useranme); // "John"
```

username would be John because the function execution will create and get delete and it will not do anything.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, "First"); // 0 "First", 1 "First", 2 "First", 3 "First", 4 "First", 5 "First", 6 "First",7 "First",8 "First",9 "First".
}
console.log(i, "Second"); // 10 "Second"
```

Here using var, var does not create any scope inside block. in lin no 89 the bvalue of i will be the last value.

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, "First"); // // 0 "First", 1 "First", 2 "First", 3 "First", 4 "First", 5 "First", 6 "First",7 "First",8 "First",9 "First".
}
console.log(i, "Second"); // ReferenceError: i is not defined
```

here the variable i only be accessible inside the loop. in line no 100 it will throw an error as i is not defined .
