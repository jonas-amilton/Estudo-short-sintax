# Estudo-short-sintax

###

## 1. The Ternary Operator

### This is a great code saver when you want to write an if..else statement in just one line.

## Longhand

````
  const x = 20;
  let answer;

  if (x > 1) {
    answer = "greater tha 10";
  } else {
    answer = "less than 10";
  }
````

## Shorthand

````
const answer = x > 10 ? "greater than 10" : "less than 10";
````

## You can also nest your if statement like this:

````
const answer = x > 10 ? "greater than 10" : x < 5 ? "less than 5" : "between 5 and 10";
````

## 2. Short-circuit Evaluation Shorthand

### When assigning a variable value to another variable, you may want to ensure that the source variable is not null, undefined, or empty. You can either write a long if statement with multiple conditionals, or use a short-circuit evaluation.

## Longhand:

````
if (variable1 !== null || variable1 !== undefined || variable1 !== '') {
     let variable2 = variable1;
}
````

## Shorthand:

````
const variable2 = variable1  || 'new';
````

### Don’t believe me? Test it yourself (paste the following code in es6console):

````
let variable1;
let variable2 = variable1  || 'bar';
console.log(variable2 === 'bar'); // prints true

variable1 = 'foo';
variable2 = variable1  || 'bar';
console.log(variable2); // prints foo
````

### Do note that if you set variable1 to false or 0, the value bar will be assigned.

## 3. Declaring Variables Shorthand

### It’s good practice to declare your variable assignments at the beginning of your functions. This shorthand method can save you lots of time and space when declaring multiple variables at the same time.

## Longhand:

````
let x;
let y;
let z = 3;
````

## Shorthand:

````
let x, y, z=3;
````

## 4. If Presence Shorthand

### This might be trivial, but worth a mention. When doing “if checks”, assignment operators can sometimes be omitted.

## Longhand:

````
if (likeJavaScript === true)
````

## Shorthand:

````
if (likeJavaScript)
````

### Note: these two examples are not exactly equal, as the shorthand check will pass as long as likeJavaScript is a truthy value.

### Here is another example. If a is NOT equal to true, then do something.

## Longhand:

````
let a;
if ( a !== true ) {
// do something...
}
````

## Shorthand:

````
let a;
if ( !a ) {
// do something...
}
````

## 5. JavaScript For Loop Shorthand

### This little tip is really useful if you want plain JavaScript and don’t want to rely on external libraries such as jQuery or lodash.

## Longhand:

````
const fruits = ['mango', 'peach', 'banana'];
for (let i = 0; i < fruits.length; i++)
````

## Shorthand:

````
for (let fruit of fruits)
````

### If you just wanted to access the index, do:

````
for (let index in fruits)
````

### This also works if you want to access keys in a literal object:

````
const obj = {continent: 'Africa', country: 'Kenya', city: 'Nairobi'}
for (let key in obj)
  console.log(key) // output: continent, country, city
````

### Shorthand for Array.forEach:

````
function logArrayElements(element, index, array) {
  console.log("a[" + index + "] = " + element);
}
[2, 5, 9].forEach(logArrayElements);
// a[0] = 2
// a[1] = 5
// a[2] = 9
````

## 6. Short-circuit Evaluation

### Instead of writing six lines of code to assign a default value if the intended parameter is null or undefined, we can simply use a short-circuit logical operator and accomplish the same thing with just one line of code.

## Longhand:

````
let dbHost;
if (process.env.DB_HOST) {
  dbHost = process.env.DB_HOST;
} else {
  dbHost = 'localhost';
}
````

## Shorthand:

````
const dbHost = process.env.DB_HOST || 'localhost';
````