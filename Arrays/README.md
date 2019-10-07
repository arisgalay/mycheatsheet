### Array Object
```js
 var fruit = ["Banana", "Apple", "Pear"];  //Create an Array Object
 fruit[2] = "Orange"; //Changing array element value
 fruit[fruit.length] = "Lemon";    // adds a new element (Lemon) to fruits
 console.log(fruit); //Access the full array
 var first = fruit[0];  //Access the elememts of an array
 var last = fruit[fruit.length - 1]; //Accessing the last element of an array

 /*Looping an Array*/
 for(i = 0;i < fruit.length;i++){
     console.log(fruit[i]);
 }
 //ForEach
```
### Array Properties
* length - The length property returns the number of elements
```js
 var cars = ["Toyota","Mitsubishi","Chevorlet"];
 var x = cars.length;
```
* constructor - The constructor property returns an array's constructor function
```js
 var cars = ["Toyota","Mitsubishi","Chevorlet"];
 console.log(cars.constructor);
 //Array - function Array() { [native code] }
 //Number - function Number() { [native code] }
 //String - function String() { [native code] }
```
* prototype - The prototype constructor allows you to add new properties and methods to the Array() object.
```js
 //Make a new array method that transforms array values into upper case:
 Array.prototype.myUcase = function() {
  for (i = 0; i < this.length; i++) {
    this[i] = this[i].toUpperCase();
  }
 };
 //Make an array, then call the myUcase method:
 // Note: Prototype is a global object constructor which is available for all JavaScript objects.
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.myUcase();
```
### Array Methods
*  concat() — Join several arrays into one
```js
 var hege = ["Cecilie", "Lone"];
 var stale = ["Emil", "Tobias", "Linus"];
 var children = hege.concat(stale);
```
*  indexOf() — Returns the first position at which a given element appears in an array
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 var a = fruits.indexOf("Apple");
```
*  join() — Combine elements of an array into a single string and return the string
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 var energy = fruits.join();
```
*  lastIndexOf() — Gives the last position at which a given element appears in an array
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 var a = fruits.lastIndexOf("Apple");
```
*  pop() — Removes the last element of an array
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.pop();
```
*  push() — Add a new element at the end
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.push("Lemon");
```
*  reverse() — Sort elements in a descending order
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.reverse();
```
*  shift() — Remove the first element of an array
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.shift();
```
*  slice() — Pulls a copy of a portion of an array into a new array
```js
 //extract the second and the third elements from the array.
 var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
 var citrus = fruits.slice(1, 3);
```
*  sort() — Sorts elements alphabetically
```js
 //Sort in Alphabetical Order
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.sort();
 //Sort an array alphabetically, and then reverse the order of the sorted items (descending):
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.sort();
 fruits.reverse();

 //Sort number Ascending
 var points = [40, 100, 1, 5, 25, 10];
 points.sort(function(a, b){return a-b});
 //sort number Descending
 var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});
``` 
*  splice() — Adds elements in a specified way and position
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.splice(2, 0, "Lemon", "Kiwi");
```
*  toString() — Converts elements to strings
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.toString();
```
*  unshift() —Adds a new element to the beginning
```js
 var fruits = ["Banana", "Orange", "Apple", "Mango"];
 fruits.unshift("Lemon","Pineapple");
```
*  filter() - method creates an array filled with all array elements that pass a test (provided as a function).
```js
 var ages = [32, 33, 16, 40];

 function checkAdult(age) {
   return age >= 18;
 }

 function myFunction() {
   document.getElementById("demo").innerHTML = ages.filter(checkAdult);
 } 
```
* find() - method returns the value of the first element in an array that pass a test (provided as a function).
```js
 var ages = [3, 10, 18, 20];

 function checkAdult(age) {
   return age >= 18;
 }

 function myFunction() {
   document.getElementById("demo").innerHTML = ages.find(checkAdult);
 }
```
*  findIndex() - Returns the index of the first element in an array that pass a test
```js
 var ages = [3, 10, 18, 20];

 function checkAdult(age) {
   return age >= 18;
 }

 function myFunction() {
   document.getElementById("demo").innerHTML = ages.findIndex(checkAdult);
 }
```
*  map() - Creates a new array with the result of calling a function for each array element
```js
 var numbers = [4, 9, 16, 25];

 function myFunction() {
   x = document.getElementById("demo")
   x.innerHTML = numbers.map(Math.sqrt);
 }
```
*  reduce() - Reduce the values of an array to a single value (going left-to-right)
```js
 //Get the sum of the numbers in the array
 var numbers = [65, 44, 12, 4];

 function getSum(total, num) {
   return total + num;
 }

 function myFunction(item) {
   document.getElementById("demo").innerHTML = numbers.reduce(getSum);
 }
```
*  reduceRight() - Reduce the values of an array to a single value (going right-to-left)
```js
 //Get the sum of the numbers in the array
 var numbers = [65, 44, 12, 4];
 function getSum(total, num) {
   return total + num;
 }

 function myFunction(item) {
   document.getElementById("demo").innerHTML = numbers.reduceRight(getSum);
 }
```
*  forEach() - Calls a function for each array element
*  valueOf() — Returns the primitive value of the specified object

### Array Iteration

### Code of Conduct
```js
 var points = new Array();     // Bad
 var points = [];              // Good 
 
 var points = new Array(40, 100, 1, 5, 25, 10); // Bad
 var points = [40, 100, 1, 5, 25, 10];          // Good

 Array.isArray(points);   // Recognize an array, returns true
```