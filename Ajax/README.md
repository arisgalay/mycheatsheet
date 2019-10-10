### Asynchronous JavaScript and XML
* Async Flow Control
 * Callback
 * Promises
 * Generator
```js
//Ajax Request
window.onload = function(){ //this function fire when the window load

    var http = new XMLHttpRequest();
    
    http.onreadystatechange = function(){
     //check the ready state.  console.log(http);
     if(http.readyState == 4 && http.status == 200){
    //do something. JSON.parse(http.response);
     }
    };
    http.open("GET", "data.json", true );
    http.send();

    //jQuery Method
    $.get("data.json", function(data){
        
    });
};
```
ReadyState
0 - request not initialized
1 - request has been set up
2 - request has been sent
3 - request is in process
4 - request is complete
### jQuery $.ajax();
```js
 window.onload = function(){
//callback 
     function errorHandler(jqXHR, textStatus,error){
         console.log(error);
     }

     $.ajax({
         type : "GET",
         url  : "data/data1.json",
         success : cdData2,
         error : errorHandler
        });

    function cdData2(data){
         console.log(data);
             
         $.ajax({
         type : "GET",
         url  : "data/data2.json",
         success : cbData3,
         error : errorHandler
        });
        }
        
    function cbData3(data){
        console.log(data);

        $.ajax({
         type : "GET",
         url  : "data/data3.json",
         success : function(data){
             console.log(data);
         },
         error : errorHandler
         });
         }

 };
```