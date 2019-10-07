### Variables
Variable declaration: var, const, let.
Variables declared with const keyword can't be reassigned, while let and var can.
```js
  const person = "Aris";
  person = "John"; // Will raise an error, person can't be reassigned

  let person = "Aris";
  person = "John";
  console.log(person); // "John", reassignment is allowed with let
```

### Data types
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

### Arithmetic Operator
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

### Assignment Operator
```js
  var x = 5,y = 10, z;
  z = x + y; //Simple assignment
  z += x; //Add and assignment
  z -= x; //Subtract and assignment
  z *= x; //Multiply and assignment
  z /= x; //Divide and assignment
  z %= x; //Modolu and assignment
```

### Comparison Operator
Given that x = 5 , the table below explains the comparison operators:

| Operator |        Description                | Comparing | Returns |
| -------- | :-------------------------------: | :-------: | :-----: |
| ==       |          Equal to                 |  x == 8   |  false  |
| ===      | Equal value and Equal type        |  x === 5  |  true   |
| !=       |          not equal                |  x != 8   |  true   |
| !==      | Not equal value or not equal type |  x !== 5  |  false  |
| >        |        Greater Than               |  x >  8   |  false  |
| <        |        Less    Than               |  x <  8   |  true   |
| >=       |    Greater Than or Equal to       |  x >=  8  |  false  |
| <=       |    Less Than or Equal to          |  x <=  8  |  true   |

### Logical Operator
Given that x = 6 and y = 3, the table below explains the logical operators: 

| Operator |   Description  |   Comparing        |    Returns   |
| -------- | :------------: | :----------------: | :----------: |
| &&       |     and        | (x < 10 && y > 1)  |  true        |
| ll       |     or         | (x == 5 ll y == 5) |  false       |
| !        |     no         | !(x == y)          |  true        |

### Conditional (Ternary) Operator
variablename = (condition) ? value1:value2 
```js
  var voteable = (age < 18) ? "Too young":"Old enough";
```

### Function
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

### If, If Else Statement
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

### Switch Statement
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
### Loops
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

### Global Functions
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

### Number Methods

### Math Methods
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
*  toString() — Returns a number as a string
*  valueOf() — Returns a number as a number

[Javascript Cheatsheet](https://websitesetup.org/javascript-cheat-sheet/)