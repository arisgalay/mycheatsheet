### DOM - Document Object Model
* querySelector() - Returns the first element that matches a specified CSS selector(s) in the document
* querySelectorAll() - Returns a static NodeList containing all elements that matches a specified CSS selector(s) in the document
```js
//querySelectorAll - return a collection of elements li
 const sample = document.querySelector("#demo"); //Grab the element , $("#demo")
 document.querySelector("#shopList li:nth-child(2) .name"); //id li[1] class
```

### Methods
* getElementById() - Returns the element that has the ID attribute with the specified value
```js
 <p id="demo"> </p>
 var text = document.getElementById("demo");
```
* getElementsByClassName() - Returns a NodeList containing all elements with the specified class name
```js
 <h1 class="title"> </h1>
 <p class="title"> </p>
 var title = document.getElementsByClassName("title");

//call classname in array
Array.from(title).forEach(function(item){
    document.write(item);
})
```

### DOM properties
* textContent - Sets or returns the textual content of a node and its descendants
* innerHTML - Sets or returns the content of an element

### Node
every single element in the page is a node
```js
 const banner = document.querySelector("#page-banner");

 console.log(banner.nodeType); //return element node type
 console.log(banner.nodeName); //return element tag name
 console.log(banner.hasChildNode()); //check if element has child 

 const cloneBanner = banner.cloneNode(true); //clone entire nodes. else only parent
```
### DOM Traversal
```js
 console.log(banner.parentNode); //return element parent
 console.log(banner.childNode); //return elements of child
 console.log(banner.children); //return elements of child *
 console.log(banner.parentElement.parentElement); //return element parent *
 console.log(banner.nextElementSibling); //get the next element sibling *
 console.log(banner.previousElementSibling); //get the previous element sibling *

 shopList.previousElementSibling.querySelector("p").innerHTML += "heloo";
```

### DOM Events
```js
 var btn = document.querySelector("#btn");
 btn.addEventListener('click', function(e){
     e.target; //find the target element
 });


 var removeBtn = document.querySelectorAll("removeBtn .delete");
 //array nodeList
 removeBtn.forEach(function(btn){
    btn.addEventListener('click', function(e){
        const li = e.target.parentElement; //grab the all li
        li.parentNode.removeChild(li); //grab the parent of li which is ul. then remove the child 
      });
 });

 //create preventdefault behaviour
 const myForm = document.querySelector("#myForm .btnSubmit");

 myForm.addEventListener('submit', function(e){
     e.preventDefault();
 });
```
### Event Bubbling
```js
 const list = document.querySelector("#parent ul");
 list.addEventListener('click',function(e){
     if(e.target.className == "delete"){
         const li = e.target.parentElement; //grab the target element
         li.parentNode.removeChild(li); //grab the parent element ul and remove child li or
         list.removeChild(li); // exactly the same as above example.
     }
 })

```
### Intearcting with forms
```js
 //Getting forms
 document.forms[0]; //arrayIndex
 document.forms["myForm"]; //idName

 const myForm = document.forms["myForm"];
 myForm.addEventListener("submit", function(e){
     e.preventDefault();
     const value = myForm.querySelector('input[type="text"]').value;
     //Create element
    const li = document.createElement("li");
    const bookName = document.createElement("span");
    const deleteBtn = document.createElement("span");
    //Add content
    bookName.textContent = value; 
    deleteBtn.textContent = "delete";
    //Add Classes
    bookName.classList.add("name");
    deleteBtn.classList.add("delete");
    // append to document
    li.appendChild(bookName);
    li.appendChild(deleteBtn);
 });
```
### Attributes
```js
 const list = document.querySelector("li");
 list.getAttribute("class"); //check if list have class attributes
 list.setAttribute("class", "newClass"); //add new attributes in class
 list.hasAttribute("href"); //check if has href attributes
 list.removeAttribute("class"); //remove class attributes
```
### Checkbox Events
```js
 const hideBox = document.querySelector("#hide"); //grab the checkbox
 hideBox.addEventListener("change", function(e){
     if(hideBox.checked){
         list.style.display = "none";
     }else{
         list.style.display = "block";
     }
 });
```
