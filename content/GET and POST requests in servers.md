+++
date = '2025-09-09T18:00:24+03:00'
title = 'GET and POST requests in servers'
categories = [ "javascript" ]
+++

## GET requests

GET is the simplest way to ask data from a server.  
The request is visible in the URL, so it’s not private.  
It’s best for reading data, not sending secrets.

- Used to read information
- Parameters go in the URL
- Not secure for passwords

## POST requests

POST is used to send data to the server.  
The data is hidden in the body of the request.  
It’s good for forms, passwords, or any private info.

- Used to send information
- Data goes inside the body
- Safer for sensitive data

### Example: POST request

```
fetch('https://api.example.com/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({ name: 'Anna', age: 25 })
})
  .then(response => response.json())
  .then(result => {
    console.log('User created:', result);
  })
  .catch(error => console.error('Error:', error));
```

### Example: GET request
```
fetch('https://api.example.com/users?name=Eva')
  .then(response => response.json())
  .then(data => {
    console.log('User found:', data);
  })
  .catch(error => console.error('Error:', error));
```

Here GET looks for a user named Eva, and POST creates a new user named Anna.

Key Points ^-^

- GET is for reading data, visible in the URL  
- POST is for sending data, hidden in the body  
- GET is simple but not secure for secrets  
- POST is better for passwords and private info  
- Together they are the most common HTTP methods  