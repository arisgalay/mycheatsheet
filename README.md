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
| \*       | Multiplication |
| \*\*     | Exponentiation |
| /        |    Division    |
| %        |     Modolu     |
| ++       |   Increment    |
| --       |   Decrement    |

#### Assignment Operator

```js
var x = 5,
  y = 10,
  z;
z = x + y; //Simple assignment
z += x; //Add and assignment
z -= x; //Subtract and assignment
z *= x; //Multiply and assignment
z /= x; //Divide and assignment
z %= x; //Modolu and assignment
```

#### Comparison and Logical Operator

Given that x = 5 , the table below explains the comparison operators:
| Operator|Description|Comparing|Returns|
| ------- |:---------:|:---------:|:---------:|
| == | Equal to |x == 8 |false |
| === | Equal value and Equal type |x === 5|true|
| == | Equal to |x == 8 |false |
| == | Equal to |x == 8 |false |
| == | Equal to |x == 8 |false |
