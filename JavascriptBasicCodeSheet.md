- Download `Node.js` from the official website and install it according to your platform.
#### Key Definitions
- `Package` => In this context, we're not dealing with packages like in Java. JavaScript doesn't have the same package concept; it's more about modules and files.
- `Functions` => Functions are blocks of code that can be executed. They are defined using the function keyword.
- `Class` => Classes in JavaScript are used to define blueprints for creating objects. This was introduced with ES6 (ECMAScript 2015).
#### Naming conventions
- For classes and functions, `camelCaseConvention` is commonly used in JavaScript.
- Variables, including constants, are typically named using `camelCase`.
- Object properties also follow `camelCase`.
---
## Data Types and Variables
- Types of Data Types
    - Primitive Data Types =>
        - `number` => Represents both `integer` and `floating-point` numbers.
        - `boolean` => Represents `true` or `false` values.
        - `string` => Represents sequences of characters.
        - `undefined` => Represents an uninitialized variable.
        - `null` => Represents an intentional absence of any object value.
        - `symbol` => Introduced in ES6, used for unique values.
    - Non-Primitive Data Types =>
        - `object` => A collection of key-value pairs, similar to dictionaries in Python.
        - `array` => An ordered collection of values.
        - `function` => A reusable block of code.

#### Variables

- `let` =>
    - Block Scope => Variables declared with let have block scope, which means they are limited to the block, statement, or expression where they are defined. They are not accessible outside of that scope.
    ```javascript
    if (true) {
        let x = 10; // x is only accessible within this block
    }
    console.log(x); // Throws an error => "x is not defined"
    ```
- `var` =>
    - Function Scope => Variables declared with var have function scope, which means they are accessible within the function they are defined in. However, they are not restricted to block-level scope and can sometimes lead to unintended global scope issues.
    ```javascript
    function example() {
    var y = 20; // y is accessible within the function
    }
    console.log(y); // Throws an error => "y is not defined"
    ```
- `const` => 
    -  Constant Values => Variables declared with const are constants, which means their values cannot be changed after they are assigned. They also have block scope, similar to let, ensuring that they are limited to the block, statement, or expression where they are defined.
    ```javascript
    const z = 30; // z is a constant variable
    z = 40; // Throws an error: "Assignment to constant variable"
    ```
- Note => In modern JavaScript, it's generally recommended to use let for variables whose values may change and const for variables whose values should remain constant. The use of var is less common due to its different scoping behavior.
---
#### Little Snippet
- Adding three numbers and printing the output
```javascript
function main() {
  var num1 = 123;
  var num2 = 321;
  var num3 = 233;
  var sum = num1 + num2 + num3;
  console.log(`sum of ${num1}, ${num2}, and ${num3} is ${sum}`);
}

main();
```
---
## Literals in Javascript
A constant value which can be assigned to the variable is called as a literal

- 101 => Integer literal
    ```javascript
    let integerLiteral = 101;
    ```
- 10.1f => Float literal
    In JavaScript, there is no distinct float type; numbers are represented as a generic Number type:

    ```javascript
    let floatLiteral = 10.1;
    ```
- 10.1 => Double literal (default decimal value is double)

    Similar to float literal, JavaScript uses the Number type for both integers and decimals:

    ```javascript
    let doubleLiteral = 10.1;
    ```
- 11111111111111111111111L => Long literal

    ```javascript
    let longLiteral = 11111111111111111111111;
    ```
- 'A' => Character literal

    JavaScript doesn't have a distinct character type; single characters are represented as strings:
    ```javascript
    let charLiteral = 'A';
    ```
- true => Boolean literal 
    ```javascript
    let booleanLiteral = true;
    ```
- "Javascript is cool" => String literal
    ```javascript
    let stringLiteral = "Javascript is cool";
    ```
    Remember that JavaScript is dynamically typed, so variables can change types during runtime, unlike Java. Also, JavaScript uses single or double quotes interchangeably for defining strings.
---
## Getting User Input in JavaScript
```javascript
// TalkingInput.js
const readline = require('readline');
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question("Talking input where the whole line is considered input:- ", (input) => {
  console.log(input);
  rl.close();
});

```
---
#### Exercise => Converting km to miles
```javascript
// Exercise1.js
const readline = require('readline');
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question("Enter the km's: ", (input) => {
  const km = parseFloat(input);
  const miles = km * 0.621371;
  console.log(`Converted to miles:==> ${miles}`);
  rl.close();
});
```
---
## JavaScript Operators / Types of Operators and Expressions
- Types of operators
    - Arithmetic operators: `+, -, *, /, %, ++, --`
    - Assignment operators: `=, +=`
    - Comparison operators: `==, >=, <=`
    - Logical operators: `&&, ||, !`
    - Bitwise operators: `&, | (operate bitwise)`

```javascript
...
let b = 9;
b += 4;
b *= 3; // Assignment operator
console.log(b);
console.log(64 > 5 && 64 > 8); // Logical operators
console.log(64 > 5 || 2 > 8); // Logical operators
...
```
---
### Increment / Decrement Operators
```javascript
let i = 56;
console.log(i++); // 56 (first use the i then increment its value)
console.log(i); // 57
console.log(++i); // 58 (first increment then use its value)
console.log(i); // 58
```
---
## If else and else if statement
```javascript
if (condition) {
 // code to run
} else if (condition) {
// code to run
} else {
// code to run
}

```
--- 
## Switch statements
```javascript
switch (value) {
  case 1:
    // code to run
    break;
  case n:
    // code to run
    break;
  default:
    // Default code to run
}
```
---
## Loops
- For loop
- While loop
- Do-while loop

> `For Loop`
```javascript
for (initialization; condition; updation) {
  // do something
}

for (let c = 0; c < 3; c++) {
  console.log("Hello World!!!");
}
```
> `While` loop
```javascript
while (condition) {
  // do something
}

let i = 0;
while (i < 11) {
  console.log("Hello World!");
  i++;
}
```
> `Do while` loop
```javascript
do {
  // do something
} while (condition);

let i = 0;
do {
  console.log(i);
  i = i + 1;
} while (i < 11);
```
---
## Arrays in Javascript
- JavaScript arrays can hold mixed data types
```javascript
// Syntax
let arrayName = new Array(); // or let arrayName = [];

// Example
let marks = new Array(76, 26, 61);

// Another way of defining an array
let anotherArray = [1, 2, 3, n];

// Example
let exampleArray = [97, 96, 56];
```
---
## 2D Arrays
```javascript
// Syntax
let arrayName = new Array(rows);

for (let i = 0; i < rows; i++) {
  arrayName[i] = new Array(columns);
}

// Example
let numbers = new Array(3);

for (let i = 0; i < 3; i++) {
  numbers[i] = new Array(5);
}

// Accessing values
numbers[0][1];
numbers[1][3];
```
---
## `Strings` in JavaScript
```javascript
// String declaration
let name = "Tanishq";
let fullName = "Tanishq Rathore";

// Taking input from the user
let inputName = prompt("Enter a name: ");
console.log(inputName);

// String manipulation

// Concatenation
let firstName = "Sri";
let lastName = "Krishna";
let fullName = firstName + " " + lastName;

// Length calculation
console.log(fullName.length);

// charAt
for (let i = 0; i < fullName.length; i++) {
  console.log(fullName.charAt(i));
}

// String comparison
let name1 = "Rama";
let name2 = "Krishna";

if (name1 === name2) {
  console.log("Strings are equal");
}

// Substring
let sentence = "Hare Rama,Hare Krishna";
let name = sentence.substring(11, sentence.length);
console.log(name);
```
---
## String Builder (Using JavaScript's String Object)
```javascript
let sb = "Tony";

// get character
console.log(sb.charAt(0));

// set character
sb = sb.substr(0, 1) + "P" + sb.substr(2);
console.log(sb);

// Insert
sb = sb.substr(0, 0) + "S" + sb.substr(1);
console.log(sb);

sb = sb.substr(0, 2) + "n" + sb.substr(3);
console.log(sb);

// Delete characters
sb = sb.substr(0, 2) + sb.substr(3);
console.log(sb);

// Appending
sb += " Stark";
console.log(sb);

// Length
console.log(sb.length);
```
---
## Operators
- `+`, `-`, `*`, `/`, `%` => Binary operators
- `++`, `--` => Unary operators
    - Pre Increment `++a`
    - Post increment `a++`
- `==`, `!=`, `>`, `<`, `>=`, `<=` => Relational operator
- `&&`, `||`, `!` => Logical operators
- `&`, `|`, `^`, `~`, `<<`, `>>` => Bitwise operator
- `=`, `+=`, `-=`, `*=`, `/=` => Assignment operator
---
## Bit Manipulation
- Concepts covered:
    - Getting a bit value
    - Setting a bit value
    - Clearing a bit value
    - Updating a bit value
#### Get Bit
- Bit Mask `1 << i`
- Operation `AND`
- `1 << 2`
```javascript
let n = 5;
let pos = 2;
let bitMask = 1 << pos;
if ((bitMask & n) === 0) {
  console.log("bit was zero");
} else {
  console.log("bit was one");
}
```
#### Set Bit
- Bit Mask ``1 << i`
- Operation `OR`
```javascript
let n = 5;
let pos = 2;
let bitMask = 1 << pos;
let newNumber = bitMask | n;
console.log(newNumber);
```
#### Clear Bit
Bit Mask `1 << i`
Operation `AND` with `NOT`
```javascript
let n = 5;
let pos = 2;
let bitMask = 1 << pos;
let notBitMask = ~(bitMask);

let newNumber = notBitMask & n;
console.log(newNumber);
```
#### Update Bit
- For 0 => Clear Operation
- Bit Mask `1 << i`
- Operation `AND` with `NOT`
- For 1 => Set Operation
- Bit Mask `1 << i`
- Operation `OR`
---
## Hoisting

- Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use a variable or call a function before they are actually declared in your code. However, it's important to note that only the declarations are hoisted, not the initializations.

Here's an example of hoisting in JavaScript:

```javascript
console.log(myVariable); // Output: undefined
var myVariable = 10;

myFunction(); // Output: "Hello, hoisting!"
function myFunction() {
    console.log("Hello, hoisting!");
}
```
Note => While declarations are hoisted, variable assignments are not. This can sometimes lead to unexpected behavior, so it's a good practice to declare variables before using them to avoid confusion.