+++
date = '2025-09-09T18:20:24+03:00'
title = 'JSON - JavaScript Object Notation'
categories = [ "javascript" ]
+++

JSON means JavaScript Object Notation.  
It’s a simple text format for storing and sharing data.  

```
{
  "name": "Eva",
  "age": 27,
  "isStudent": false,
  "skills": ["HTML", "CSS", "JavaScript"],
}

```


It looks like JavaScript objects, but it is always just a string.  
Most APIs use JSON to send information between server and client.  
For example, when your app talks to a backend, the backend usually answers with JSON.


Important rules:

- Always use **double quotes** for keys and strings.
    
- Supported types: `string`, `number`, `boolean`, `null`, `array`, `object`.
    
- It is just text that can be parsed back into an object.


```
// JavaScript object
const user = {
  name: "Eva",
  age: 27,
  skills: ["HTML", "CSS", "JS"]
};

// Convert object to JSON string
const jsonString = JSON.stringify(user);
console.log(jsonString);
// {"name":"Eva","age":27,"skills":["HTML","CSS","JS"]}

// Parse JSON string back to object
const parsedUser = JSON.parse(jsonString);
console.log(parsedUser.name); // Eva
```


This code shows how to work with JSON in JavaScript.
First, we take an object and convert it into a JSON string with `JSON.stringify()`.  
Then, we parse the string back into an object with `JSON.parse()`.