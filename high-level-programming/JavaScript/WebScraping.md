# Java Script - Web Scraping

## Working with JSON

- JavaScript Object Notation (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax
- JSON is a string whose format very much resembles JavaScript object literal format. You can include the same basic data types inside JSON as you can in a standard JavaScript object
- JSON is purely a string with a specified data format — it contains only properties, no methods.

### Working through a JSON example

```JavaScript
async function populate() {

  const requestURL = 'https://mdn.github.io/learning-area/javascript/oojs/json/superheroes.json';
  const request = new Request(requestURL);

  const response = await fetch(request);
  const superHeroes = await response.json();

  populateHeader(superHeroes);
  populateHeroes(superHeroes);

}
```

- To obtain the JSON, we use an API called `Fetch`. This API allows us to make network requests to retrieve resources from a server via JavaScript

#### Populating the header

- Now that we've retrieved the JSON data and converted it into a JavaScript object, let's make use of it by writing the two functions we referenced above

```JavaScript
function populateHeader(obj) {
  const header = document.querySelector('header');
  const myH1 = document.createElement('h1');
  myH1.textContent = obj.squadName;
  header.appendChild(myH1);

  const myPara = document.createElement('p');
  myPara.textContent = `Hometown: ${obj.homeTown} // Formed: ${obj.formed}`;
  header.appendChild(myPara);
}
```

### Converting between objects and text

- sometimes we receive a raw JSON string, and we need to convert it to an object ourselves. And when we want to send a JavaScript object across the network, we need to convert it to JSON (a string) before sending
- a built-in JSON object is available in browsers, which contains the following two methods
  - `parse()`: Accepts a JSON string as a parameter, and returns the corresponding JavaScript object
  - `stringify()`: Accepts an object as a parameter, and returns the equivalent JSON string


## The workflow of accessing the attributes of a simply-created JSON object

- created a simple JSON object

```json
{
  "likes": [
    "Reliability",
    "Order",
    "Error checks"
  ],
  "age": 34,
  "name": "TCP"
}
```
- access the whole body of the JSON object

```JavaScript
const request = require('request');
const url = 'http://jsonbin.io/b/591a64459208345676e6a1ed';
request (url, function (error, response, body) {
 if (error) {
  console.log(error);
 } else {
  console.log(JSON.parse(body));
 }
});
```

- To access the respective attributes, say the “name”, you simply add that attribute to the code accordingly.
  - `console.log(JSON.parse(body).name);`
- To access the respective an element in the array of “likes” attribute, say the first element [which is of course the 0th element], you simply add that attribute and the element you are trying to grab
  - `console.log(JSON.parse(body).likes[0])`

## What is Axios module?

- Axios is a promise-based HTTP Client for node.js and the browser
- Features
  - Make XMLHttpRequests from the browser
  - Make http requests from node.js
  - Supports the Promise API
  - Intercept request and response
  - Transform request and response data
  - Cancel requests
  - Automatic transforms for JSON data