# JavaScript Utility Functions – Unit Testing with Jest

This project demonstrates how to write and test simple JavaScript utility functions using [Jest](https://jestjs.io/). It includes:

- `concat`: A function that adds a new property `id_name` to each object in an array.
- `addition`: A function that returns the sum of two numbers.

---

##  Project Structure



---

## Functions Overview

### 🔹 concat()

This function returns a mapper that appends a new key `id_name` to each object, formatted as `"id - name"`.

#### Example:

```js
const data = [
  { id: 1, name: "Pedro" },
  { id: 2, name: "John" },
  { id: 3, name: "Vitor" }
];

const updatedData = data.map(concat());

/*
[
  { id: 1, name: "Pedro", id_name: "1 - Pedro" },
  { id: 2, name: "John", id_name: "2 - John" },
  { id: 3, name: "Vitor", id_name: "3 - Vitor" }
]
*/
```


 ## Test Scenarios
The run.test.js file includes tests written with Jest for both functions:

### concat Test
GIVEN an array with an object: { id: 10, name: "Lucky" }

WHEN the function is called

THEN the result should include: id_name: "10 - Lucky"

### addition Test
GIVEN two numbers: 10 and 20

WHEN the function is called

THEN it should return 30

## Technologies Used
JavaScript (Node.js)

```js

function concat() {
    return (obj) => {
        obj.id_name = obj.id + " - " + obj.name;
        return obj;
    }
}

function addition(n1, n2) {
    return n1 + n2;
}

module.exports = {
    concat,
    addition
}
```





