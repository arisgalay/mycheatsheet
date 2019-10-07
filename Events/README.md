### Events
```js
 var title = document.getElementById("title");
 
 //Anonymouse function
 title.onclick = function(){
     alert("do whatever here");
 };
```
### Forms
```js
 var myForm = document.forms.myForm; // grab form
 myForm.name.value; //check if field has value

 myForm.onsubmit = function(){
     if(myForm.name.value == ""){
         //error message
     }
 };
```