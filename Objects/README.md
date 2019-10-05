### Objects
```js
 //Create an Object
 var Person = {
     firstName: "Aris",
     lastName: "Galay",
     age: 20,
     work: "none",
     grind: function(){
         console.log("Code Code Code...");
     },
     fullName: function(){
         console.log(`My Fullname is ${this.firstName} ${this.lastName}`);
     }
 }; 

console.log(Person.firstName);  //Call an Object property
console.log(Person.fullName()); //Call an Object  function
```
### Constructor Functions
```js
 var Person = function(firstName,lastName,myAge){
     this.firstName = firstName;
     this.lastName = lastName;
     this.myAge = myAge;
     this.fullName = function(){
         console.log(`My Fullname is ${this.firstName} ${this.lastName}`);
     }
 }

 var user1 = new Person("Aris","Galay",20); //inserting value to constructor functionss
 user1.fullName(); //call
```

### Date Object
```js
 

```