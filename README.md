#### Variables
Variable declaration: var, const, let.
Variables declared with const keyword can't be reassigned, while let and var can.
```js
  const person = "Aris";
  person = "John"; // Will raise an error, person can't be reassigned

  let person = "Aris";
  person = "John";
  console.log(person); // "John", reassignment is allowed with let
```

#### Data types
```js
  var work; //Undefined
  var love = true; //Boolean
  var name = "Aris"; //Strings
  var age = 20; //Number
  var skill = ["HTML", "CSS", "Javascript"]; //Arrays
  var myInfo = {
    fistName: "Aris",
    lastName: "Galay"
  }; //Objects
```

#### Arithmetic Operator
| Operator |  Description   |
| -------- | :------------: |
| +        |    Additon     |
| -        |  Subtraction   |
|  *       | Multiplication |
| **       | Exponentiation |
| /        |    Division    |
| %        |     Modolu     |
| ++       |   Increment    |
| --       |   Decrement    |

#### Assignment Operator
```js
  var x = 5,y = 10, z;
  z = x + y; //Simple assignment
  z += x; //Add and assignment
  z -= x; //Subtract and assignment
  z *= x; //Multiply and assignment
  z /= x; //Divide and assignment
  z %= x; //Modolu and assignment
```

#### Comparison Operator
Given that x = 5 , the table below explains the comparison operators:
| Operator |        Description               | Comparing | Returns |
| -------- | :------------------------------: | :-------: | :-----: |
| ==       |          Equal to                |  x == 8   |  false  |
| ===      | Equal value and Equal type       |  x === 5  |  true   |
| !=       |          not equal               |  x != 8   |  true   |
| !==      | Not equal value or not equal type|  x !== 5  |  false  |
| >        |        Greater Than              |  x >  8   |  false  |
| <        |        Less    Than              |  x <  8   |  true   |
| >=       |    Greater Than or Equal to      |  x >=  8  |  false  |
| <=       |    Less Than or Equal to         |  x <=  8  |  true   |

#### Logical Operator
Given that x = 6 and y = 3, the table below explains the logical operators: 
| Operator | Description | Comparing            | Returns |
| -------- | :---------: | :------------------: | :-----: |
| &&       |     and     | (x < 10 && y > 1)    |  true   |
| ||       |     or      | (x == 5 || y == 5)   |  false  |
| !        |     no      | !(x == y)            |  true   |

#### Conditional (Ternary) Operator
variablename = (condition) ? value1:value2 
```js
  var voteable = (age < 18) ? "Too young":"Old enough";
```

#### Function
```js
   function functionName() {
   console.log("Hello World");
  }
  functionName(); //Calling a function

  //Passing Values to Function
 function testFun(param1, param2) {
   console.log(param1, param2);
 }
 testFun("Hello", "World"); //Adding value & calling the function
```

#### If, If Else Statement
```js
 if (condition is true) {
   statement is executed
 }

 //chaining if else
 if (condition1) {
   statement1
 } else if (condition2) {
   statement2
 } else if (condition3) {
   statement3
 . . .
 } else {
   statementN
 } 
```

#### Switch Statement
case "a": , case 1:
```js
//case values are tested with strict equality (===).
 switch(num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
 ...
  case valueN:
    statementN;
    break;
 }

//Multiple Identical Options
 switch(val) {
  case 1:
  case 2:
  case 3:
    result = "1, 2, or 3";
    break;
  case 4:
    result = "4 alone";
}
```
#### Loops
*  for — The most common way to create a loop in JavaScript
*  while — Sets up conditions under which aloop executes
*  do while — Similar to the while loop but it executes at least once and performs a check at the end to s
*  if the condition is met to execute again
*  break —Used to stop and exit the cycle at certain conditions
*  continue — Skip parts of the cycle if certain conditions are met
```js
  //For Loop
  for (i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
  }
  //While Loop
  while (i < 10) {
  text += "The number is " + i;
  i++;
  }
  //Do While Loop
  do {
  text += "The number is " + i;
  i++;
  }
  while (i < 10); 
```
#### Array Methods
```js
var fruit = ["Banana", "Apple", "Pear"];
```
*  concat() — Join several arrays into one
*  indexOf() — Returns the first position at which a given element appears in an array
*  join() — Combine elements of an array into a single string and return the string
*  lastIndexOf() — Gives the last position at which a given element appears in an array
*  pop() — Removes the last element of an array
*  push() — Add a new element at the end
*  reverse() — Sort elements in a descending order
*  shift() — Remove the first element of an array
*  slice() — Pulls a copy of a portion of an array into a new array
*  sort() — Sorts elements alphabetically
*  splice() — Adds elements in a specified way and position
*  toString() — Converts elements to strings
*  unshift() —Adds a new element to the beginning
*  valueOf() — Returns the primitive value of the specified object
#### Array Sort

#### Array Iteration

#### String Methods
```js 
var person = "John Doe";
```
*  charAt() — Returns a character at a specified position inside a string
*  charCodeAt() — Gives you the unicode of a character at that position
*  concat() — Concatenates (joins) two or more strings into one
*  fromCharCode() — Returns a string created from the specified sequence of UTF-16 code units
*  indexOf() — Provides the position of the first occurrence of a specified text within a string
*  lastIndexOf() — Same as indexOf() but with the last occurrence, searching backward
*  match() — Retrieves the matches of a string against a search pattern
*  replace() — Find and replace specified text in a string
*  search() — Executes a search for a matching text and returns its position
*  slice() — Extracts a section of a string and returns it as a new string
*  split() — Splits a string object into an array of strings at a specified position
*  substr() —  Similar to slice() but extracts a substring depending on a specified number of characters
*  substring() — Also similar to slice() but can’t accept negative indices
*  toLowerCase() — Convert strings to lower case
*  toUpperCase() — Convert strings to upper case
*  valueOf() — Returns the primitive value (that has no properties or methods) of a string object

#### Global Functions
Global functions are functions built into every browser capable of running JavaScript.
*  decodeURI() — Decodes a Uniform Resource Identifier (URI) created by encodeURI or similar
*  decodeURIComponent() — Decodes a URI component
*  encodeURI() — Encodes a URI into UTF-8
*  encodeURIComponent() — Same but for URI components
*  eval() — Evaluates JavaScript code represented as a string
*  isFinite() — Determines whether a passed value is a finite number
*  isNaN() — Determines whether a value is NaN or not
*  Number() —- Returns a number converted from its argument
*  parseFloat() — Parses an argument and returns a floating point number
*  parseInt() — Parses its argument and returns an integer

#### Number Methods
Number Properties
*  MAX_VALUE — The maximum numeric value representable in JavaScript
*  MIN_VALUE — Smallest positive numeric value representable in JavaScript
*  NaN — The “Not-a-Number” value
*  NEGATIVE_INFINITY — The negative Infinity value
*  POSITIVE_INFINITY — Positive Infinity value
Number Methods
*  toExponential() — Returns the string with a rounded number written as exponential notation
*  toFixed() — Returns the string of a number with a specified number of decimals
*  toPrecision() — String of a number written with a specified length
*  toString() — Returns a number as a string
*  valueOf() — Returns a number as a number
Math Properties
*  E — Euler’s number
*  LN2 — The natural logarithm of 2
*  LN10 — Natural logarithm of 10
*  LOG2E — Base 2 logarithm of E
*  LOG10E — Base 10 logarithm of E
*  PI — The number PI
*  SQRT1_2 — Square root of 1/2
*  SQRT2 — The square root of 2
Math Methods
*  abs(x) — Returns the absolute (positive) value of x
*  acos(x) — The arccosine of x, in radians
*  asin(x) — Arcsine of x, in radians
*  atan(x) — The arctangent of x as a numeric value
*  atan2(y,x) — Arctangent of the quotient of its arguments
*  ceil(x) — Value of x rounded up to its nearest integer
*  cos(x) — The cosine of x (x is in radians)
*  exp(x) — Value of Ex
*  floor(x) — The value of x rounded down to its nearest integer
*  log(x) — The natural logarithm (base E) of x
*  max(x,y,z,...,n) — Returns the number with the highest value
*  min(x,y,z,...,n) — Same for the number with the lowest value
*  pow(x,y) — X to the power of y
*  random() — Returns a random number between 0 and 1
*  round(x) — The value of x rounded to its nearest integer
*  sin(x) — The sine of x (x is in radians)
*  sqrt(x) — Square root of x
*  tan(x) — The tangent of an angle

[Javascript Cheatsheet](https://websitesetup.org/javascript-cheat-sheet/)