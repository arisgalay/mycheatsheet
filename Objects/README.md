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
 //Create an Date object
 var currentDate = new Date(); // store the current date in the variable.
 var selectDate = new Date(); 
 /* YYYY,MM,DD,HR,Min,Secs
    Month = 0 - 11, january to decemeber 
    Hour = 0 - 23
    Minutes = 0 - 59
    Seconds = 0 - 59
 */

 var birthday = new Date(1999, 1, 6, 11, 30, 30);
 
 console.log(birthday.getMonth()); //Get month of the date (0 - 11)
 console.log(birthday.getFullYear()); //Get the full year (YYYY)
 console.log(birthday.getDate()); //Get the date of the month (0 - 31)
 console.log(birthday.getDay()); //Get the day of the week (0 - 6)
 console.log(birthday.getHours()); //Get the hour of the date (0 - 23)
 console.log(birthday.getTime()); //Get the number of milliseconds since the 1st jan 1970
```
### DOM - Document Object Model
* Use the dom when we interact to webpages. ADD content to a html document,DELETE content from a html document,CHANGE content to an html document.
```js
 //Traversing the DOM
 document.getElementByClassName("class"); //selecting class
 document.getElementsByTagName("h1").innerHTML = "Title"; //selecting html tags & changing content
 var try = document.getElementById("idName"); //selecting ID  

 try.getAttribute("href"); //get the value of attribute
 try.setAttribute("attrName", "value"); //set attribute with value or change attr value
 try.className = "newValue"; //select class and update new value
 try.style.left = "20px"; // updating css style

 //Changing Content using DOM Properties
 innerHTML = "<p>ey</p>"; //change the html tags & content
 textContent = "Changes"; //change the content
```

### Create new element using DOM
```js
 var newLi = document.createElement("li"); //created new li tag
 var newA = document.createElement("a"); //created new a tag

 var menu = documenet.getElementById("main").getElementsByTagName("ul")[0]; //selecting dom and grab element
 menu.appendChild(newLi);
 newLi.appendChild(newA);
 newA.innerHTML = "Content";

 menu.insertBefore(newLi, menu.getElementsByTagName("li")[0]); //insert at the top
```

### Removing elements from the DOM;
```js
 var parent = document.getElementById("main").getElementsByTagName("ul")[0]; //get the parent
 var child = parent.getElementsByTagName("li")[0]; //get the tag you want to remove

 var removed = parent.removeChild(child); //remove

```