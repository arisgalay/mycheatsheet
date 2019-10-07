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
