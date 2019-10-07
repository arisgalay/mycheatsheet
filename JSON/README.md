### JSON Javascript Object Notation
* JSON is a format for storing and transporting data.
* JavaScript Objects can be converted into JSON, and JSON can be converted back into JavaScript Objects.
This way we can work with the data as JavaScript objects, with no complicated parsing or translations.
```js
 // a JavaScript object...:
 var myObj = { "name":"John", "age":31, "city":"New York" };

 // ...converted into JSON:
 var myJSON = JSON.stringify(myObj);

 // send JSON:
 window.location = "demo_json.php?x=" + myJSON;
```

### Methods
* parse() - Parses a JSON string and returns a JavaScript object
* stringify() - Convert a JavaScript object to a JSON string