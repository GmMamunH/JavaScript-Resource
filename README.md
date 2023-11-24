# JavaScript-Resource
1. [JavaScript Numbers](https://www.w3schools.com/js/js_numbers.asp)
2. [JavaScript Number Methods](https://www.w3schools.com/js/js_numbers.asp)
3. [JavaScript Strings](https://www.w3schools.com/js/js_strings.asp)

# Primitive Data Types

## JavaScript Numbers

### Adding Numbers and Strings

```
WARNING !!

JavaScript uses the + operator for both addition and concatenation.

Numbers are added. Strings are concatenated.
```

```js
let x = 10;
let y = 20;
let z = "30";
let result = x + y + z;
```

**NB: The JavaScript interpreter works from left to right.**

## NaN - Not a Number

You can use the global JavaScript function isNaN() to find out if a value is a not a number:

```js
let x = 100 / "Apple";
isNaN(x);
```

## Infinity

Division by 0 (zero) also generates Infinity:

```js
let x =  2 / 0;
let y = -2 / 0;
```

**Infinity is a number: typeof Infinity returns number.**

---

## JavaScript Number Methods

These number methods can be used on all JavaScript numbers:

`toString()`
`toFixed()`

**The `toString()` Method**

```js
let x = 123;
x.toString();
(123).toString();
(100 + 23).toString();
```

By default, JavaScript displays numbers as **base 10** decimals.

But you can use the `toString()` method to output numbers from **base 2** to **base 36**.

Hexadecimal is **base 16**. Decimal is **base 10**. Octal is **base 8**. Binary is **base 2**.

```js
let myNumber = 32;
myNumber.toString(32);
myNumber.toString(16);
myNumber.toString(12);
myNumber.toString(10);
myNumber.toString(8);
myNumber.toString(2);
```

**The `toFixed()` Method**

```js
let x = 9.656;
x.toFixed(0);
x.toFixed(2);
x.toFixed(4);
x.toFixed(6);
```

### Converting Variables to Numbers

There are 3 JavaScript methods that can be used to convert a variable to a number:

- `Number()`
- `parseFloat()`
- `parseInt()`

**The `Number()` Method**

```js
 Number(true); // 1
 Number(false); // 0
 Number("10"); // 10
 Number("  10"); // 10
 Number("10  "); // 10
 Number(" 10  "); // 10
 Number("10.33"); // 10.33
 Number("10,33"); // NaN
 Number("10 33"); // NaN
 Number("John"); // NaN
```

If the number cannot be converted, NaN (Not a Number) is returned.

**The `parseInt()` Method**

The `parseInt()` parses a string and returns a whole number. Spaces are allowed. Only the first number is returned:

```js
 parseInt("-10"); // -10
 parseInt("-10.33"); // -10
 parseInt("10"); // 10
 parseInt("10.33"); // 10
 parseInt("10 20 30"); // 10
 parseInt("10 years"); // 10
 parseInt("years 10"); // NaN
```

If the number cannot be converted, NaN (Not a Number) is returned.

**The `parseFloat()` Method**

parseFloat() parses a string and returns a number. Spaces are allowed. Only the first number is returned:

```js
parseFloat("10"); //10
parseFloat("10.33"); // 10.33
parseFloat("10 20 30"); // 10
parseFloat("10 years"); // 10
parseFloat("years 10"); // NaN
```

# JavaScript Strings

You can use quotes inside a string, as long as they don't match the quotes surrounding the string:

```js
let answer1 = "It's alright";
let answer2 = "He is called 'Johnny'";
let answer3 = 'He is called "Johnny"';
```

## String Length

To find the length of a string, use the built-in length property:

```js
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let length = text.length;
```

## Escape Character

Because strings must be written within quotes, JavaScript will misunderstand this string:

```js
let text = "We are the so-called "Vikings" from the north.";
```

The string will be chopped to "We are the so-called ".

The solution to avoid this problem, is to use the **backslash escape character.**

The backslash `(\)` escape character turns special characters into string characters:

| Code | Result | Description  |
| ---- | ------ | ------------ |
| \'   | '      | Single quote |
| \"   | "      | Double quote |
| \\   | \      | Backslash    |

The sequence \" inserts a double quote in a string:

```js
let text = "We are the so-called \"Vikings\" from the north.";
```

The sequence \' inserts a single quote in a string:

```js
let text= 'It\'s alright.';
```

The sequence \\ inserts a backslash in a string:

```js
let text = "The character \\ is called backslash.";
```

## String Methods

### JavaScript String `concat()`

`concat()` joins two or more strings:

```js
let text1 = "Hello";
let text2 = "World";
let text3 = text1.concat(" ", text2);

// They both are same
let result1 = "Hello" + " " + "World!";
let result2 = "Hello".concat(" ", "World!");
```

<!-- OPERATORS -->

# JavaScript Operators

## What is an Operator?

In JavaScript, an operator is a special symbol used to perform operations on operands (values and variables). For example,

```js
2 + 3; // 5
```

Here `+` is an operator that performs addition, and `2` and `3` are operands.

## JavaScript Operator Types

Here is a list of different operators you will learn in this tutorial.

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- Logical Operators
- String Operators

---

## JavaScript Arithmetic Operators

Arithmetic operators are used to perform `arithmetic calculations`. For example,

```js
const number1 = 3 + 5; // 8
const number2 = 30 + 50; // 80
```

Here, the `+` operator is used to add two operands.

| Operator | Name                        | Example        |
| -------- | --------------------------- | -------------- |
| `+`      | Addition                    | `x + y `       |
| `-`      | Subtraction                 | `x - y `       |
| `\*`     | Multiplication              | `x \* y`       |
| `/`      | Division                    | `x / y`        |
| `%`      | Remainder                   | `x % y`        |
| `++`     | Increment (increments by 1) | `++x` or `x++` |
| `--`     | Decrement (decrements by 1) | `--x` or `x--` |

### Example 1: Arithmetic operators in JavaScript

```js
let x = 5;
let y = 3;

// addition
console.log('x + y = ', x + y);  // 8

// subtraction
console.log('x - y = ', x - y);  // 2

// multiplication
console.log('x * y = ', x * y);  // 15

// division
console.log('x / y = ', x / y);  // 1.6666666666666667

// remainder
console.log('x % y = ', x % y);   // 2

// increment
console.log('++x = ', ++x); // x is now 6
console.log('x++ = ', x++); // prints 6 and then increased to 7
console.log('x = ', x);     // 7

// decrement
console.log('--x = ', --x); // x is now 6
console.log('x-- = ', x--); // prints 6 and then decreased to 5
console.log('x = ', x);     // 5

```

## JavaScript Assignment Operators

Assignment operators are used to **assign values to variables**. For example,

```js
const num1 = 5;
```

Here, the `=` operator is used to assign value `5` to variable `num1`.

more below 👇🏻👇🏻

```js
// Assign the value 50 to x
let x = 50;
// Assign the value 2 to y
let y = 2;
// Assign the value x + y to z:
let z = x + y;
```

Here's a list of commonly used assignment operators:

| Operator | Name                      | Example                |
| -------- | ------------------------- | ---------------------- |
| =        | Assignment operator       | `a = 7; // 7`          |
| +=       | Addition assignment       | `a += 5; // a = a + 5` |
| -=       | Subtraction Assignment    | `a -= 2; // a = a - 2` |
| \*=      | Multiplication Assignment | `a *= 3; // a = a * 3` |
| /=       | Division Assignment       | `a /= 2; // a = a / 2` |
| %=       | Remainder Assignment      | `a %= 2; // a = a % 2` |

**Note:** The commonly used assignment operator is `=`. You will understand other assignment operators such as `+=`, `-=`, `*=` etc. once we learn arithmetic operators.

---
# Operators in JavaScript

## Types of JavaScript Operators

There are different types of JavaScript operators:

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- Logical Operators

### JavaScript Arithmetic Operators:

**Arithmetic Operators** are used to perform arithmetic on numbers:

Arithmetic Operators Example

```js
let a = 3;
let x = (100 + 50) * a;
```

| Operator | Description                  |
| -------- | ---------------------------- |
| `+`      | Addition                     |
| `-`      | Subtraction                  |
| `*`      | Multiplication               |
| `/`      | Division                     |
| `%`      | Modulus (Division Remainder) |

### JavaScript Assignment Operators

Assignment operators assign values to JavaScript variables.

The **Addition Assignment Operator** (`+=`) adds a value to a variable.

Assignment

```js
let x = 10;
x += 5;
```

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| `=`      | x = y   | x = y      |
| `+=`     | x += y  | x = x + y  |
| `-=`     | x -= y  | x = x - y  |
| `*=`     | x \*= y | x = x \* y |
| `/=`     | x /= y  | x = x / y  |
| `%=`     | x %= y  | x = x % y  |

### JavaScript Comparison Operators

> [!NOTE]
> Comparison operators compare two values and return a boolean value, either `true` or `false`

| Operator | Description                       |
| -------- | --------------------------------- |
| ==       | Equal to                          |
| ===      | Equal value and equal type        |
| !=       | Not equal                         |
| !==      | Not equal value or not equal type |
| >        | Greater than                      |
| <        | Less than                         |
| >=       | Greater than or equal to          |
| <=       | Less than or equal to             |

**Equal to (`==`)**

Example

```js
const a = 10;
const b = 20;

console.log(a == b);
console.log(50 == 50);
console.log("50" == 50);
console.log('A' == 'A');
console.log('Hello' == 'Hello');
console.log('Hello' == 'hello');
console.log('Hello' == 'world');
```

**Equal value and equal type / strict equal operator (`==`)**

Example

```js
const a = 10;
const b = 20;

console.log(a === b);
console.log(50 === 50);
console.log("50" === 50);
console.log('A' === 'A');
console.log('Hello' === 'Hello');
console.log('Hello' === 'hello');
console.log('Hello' === 'world');
```

**Not equal operator (`!=`)**

Example

```js
console.log(3 != 2); // true
console.log('hello' != 'Hello'); // true
console.log(5 != 5); // false
```

**Not equal operator (`!=`)**

Example

```js
console.log(2 !== '2'); // true
console.log(2 !== 2); // false
```

### JavaScript Unary Operators:

| Operator | Description |
| -------- | ----------- |
| `++`     | increment   |
| `--`     | deincrement |

### JavaScript Logical Operators:

<table>
<tr>
<th>Operator</th>
<th>Description</th>
</tr>

<tr>
<td>&&</td>
<td>logical AND</td>
</tr>

<tr>
<td>||</td>
<td>logical OR</td>
</tr>

<tr>
<td>!</td>
<td>logical NOT</td>
</tr>
</table>

## 123456789
## > <
```js
const a = 10;
const b = 20;
```
## > Greater than:-
```js
console.log(10 > 20);
console.log(a > b);
console.log(50 > 49);
```
## < Less than:-
```js
console.log(10 < 20);
console.log(a < b);
console.log(60 < 50);
```
## >= Greater than or Equal:-
```js
console.log(10 > 10);

const age = 17;
console.log(age >= 18);
```
## <= Less than or Equal
```js
const age2 = 45;
console.log(age2 <= 45);
```
## Problems Solve;
```js
const personAge = 18;
console.log('Condition = ', personAge >= 18);

if (personAge >= 18) {
  console.log('Yes. Tumi Vote Dite Parba. 🏆');
}
if (personAge < 18) {
  console.log('No. Tumi Vote Dite Parba Na. 😭');
}

// =======>
let num1 = 10;
num1 = num1 + 1;
console.log(num1);
console.log(num1 + 1);
```
======================================
# Unary Operatoers

## 1. Increment
### A. Pre Increment => (++num)
### B. Post Increment => (num++)

## 2. Decrement
### A. Pre Decrement => (--num)
### B. Post Decrement => (num--)
======================================
#### Pre Increment => (++num)
```js
let num = 5;

console.log(++num);
console.log(++num);
console.log(num);
console.log(num);
console.log(num);
```
### Post Increment => (num++)
```js
console.log(num + 1);
console.log(num++);
console.log(num++);
console.log(num);
```
### Pre Decrement => (--num)
```js
let num = 5;

console.log(--num);
console.log(--num);
console.log(--num);
```
### Post Decrement => (num--)
console.log(num--);
console.log(num--);
console.log(num--);
console.log(--num);
```

# JavaScript Logical Operators:
## 1. && - (AND)
## 2. || - (OR)
## 3. ! - (NOT)

## && - (AND)
```js
console.log(10 == 10 && 40 > 10); // true
console.log(10 == 10 && 4 > 10); // false
console.log(10 == 11 && 40 > 10); // false
console.log(10 == 11 && 4 > 10); // false
```
## || - (OR)
```js
console.log(10 == 10 || 40 > 10); // true
console.log(10 == 10 || 4 > 10); // true
console.log(10 == 11 || 40 > 10); // true
console.log(10 == 11 || 4 > 10); // false
```
## ! - (NOT)
```js
const isAdult = true;
console.log(!isAdult);
console.log(!true);
```
# AND (&&)
## A -  AND -  B  -   Result
## true  &&    true  =   true
## true  &&    false =  false
## false  &&    true =  false
## false  &&    true =  false

# OR (||)
## A -  OR -  B  -   Result
## true  ||    true  =   true
## true  ||    false =  true
## false  ||    true =  true
## false  ||    true =  false

# NOT (!)
## true = false
## false = true
