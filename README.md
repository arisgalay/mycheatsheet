### jQuery
```js
 var demo = $("#demo"); //getElementById , class , tags
 demo.css({color: red}); //add CSS

 /* Filter */
 $("header nav li:first").css({border: "2px solid black"});
 //first,last - get the child of selected element tag
 //first:child , last:child - get the first element tag or last element tag
 //li:even , li:odd - even 0 based
 //section:not('#contact') - style all section except section with #contact
//input[type='button'] - attribute filter
```
### Traversing DOM
```js
 $("header nav").next().css({border: "2px solid blue"}); //get the next element tag
 $("header nav").prev().css({border: "2px solid blue"}); //get the previous element tag
 $("#banner").parent().css({border: "2px solid red"}); //get the parent element tag
 $("#nav-link").children().css({border: "2px solid pink"}); //get the all child element like li
 //find class
 $("#contact").find(".facebook").css({border: "2px solid green"});
 $("#footer").closest(".container").css({border: "2px solid green"});
```
### Adding Content
```js
 var addCode = "<p>Add Now</p>"
 $("#demo div").append(addCode); //adds content to the bottom of the element
 $("#demo div").prepend(addCode); //adds content to the top of the element
 $("#demo div p").before(addCode); //adds content before element
 $("#demo div p").after(addCode); //adds content after element
 html();
 text();
```
### Wrap and Unwrap elements
```js
 wrap(); //wraps all matches element individually
 unwrap(); //unwrap all matches element
 wrapAll(); //wrap all elements combined with 1 single element
```
### Removing Content
```js
 .empty(); //empties the innerhtml inside elements
 .remove(); //removes element completely

```
### Changing Attributes
```js
 removeAttr("type"); //remove attributes completly
 attr("alt","this is an alternative"); //set or read attributes
```
### Controlling CSS
```js
css({
    "width" : "250px",
    "border": "2px solid black"
});
//Removing Class
$("header .container").removeClass("container");
//Add Class
$("header > div").addClass("container");
//Toggle Class
var btn = $("#form a");
btn[0].onclick = function(){
    $("#main-content").toggleClass("open");
    return false;
};
```
### Binding & Unbinding Events
```js
 var myLis = $("header li");
 myLis.on("click", function(){
     $(this).css({"background-color" : "pink"});
     myLis.off("click");
 });
```

* Document Ready
```js
 $(document).on("ready", function(){
     //method 1
 });
 $(document).ready(function(){
     //method 2
 });
 
 $(function(){
    //method 3
 });
```
* Window onload
```js
 $(window).on("load", function(){
     //method 1
 });
 
 $(window).load(function(){
     //method 2
 });
```
### Animations
```js
 $("#btn").on("click", function(){
     $(this).animate({"width" : "300px", "height" : "100px"}, 2000 , "linear", function(){
         console.log("do something");   
     });
 });
 //Animation method
fadeOut(2000);
fadeIn(500);
hide(1000);
show(1000);
toggle(1000);
```
* Sliding Elements
```js
 slideUp(200);
 slideDown(2000,function(){
     //callback
 });
 slideToggle();
```
### Plugins
```js
 ResponsiveSlideJs
 
```