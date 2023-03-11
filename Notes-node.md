# Node.js Notes - Codevolution

Playlist Link : </br>
<https://www.youtube.com/watch?v=LAUi8pPlcUM&list=PLC3y8-rFHvwh8shCMHFA5kWxD9PaPwxaY>

</br>

---

## Node.js

- JS runtime environment

## Modules

```javascript
// Module wrapper

/* Modules execute as iife patterns*/

(function (exports, require, module, __filename, __dirname) {
  // some code
})();
```

</br>

---

## Watch mode

```javascript
// Automatic update

in terminal -> node --watch fileName
```

</br>

---

## Built-in Modules

```javascript
// 1) Events module

const EventEmitter = require("node:events"); // node: is used to specify that it is a built-in module (optional)

const emitter = new EventEmitter();

// Event listener on 'order-pizza' event
emitter.on("order-pizza", (size, topping) => {
  console.log(`Order recieved, baking ${size} pizza with ${topping}`);
});

// Fire the 'order-pizza' event
emitter.emit("order-pizza", "large", "mushrooms");
```

```javascript
Character Encoding
- Character encoding dictates how to represent a number in a character set as binary data before it can be stored in a computer

- It dictates how many bits to use to represent the number

- Example of a character encoding system is UTF-8
- UTF-8 states that characters should be encoded in bytes (8 bits)

- Eight 1s or Os should be used to represent the code of any character in binary
4 =>100=> 00000100
V=> 86 => 01010110
```

</br>

---

# Node.js Notes - Pluralsight

Playlist Link : </br>
<https://app.pluralsight.com/library/courses/nodejs-getting-started/table-of-contents>

</br>

---

## Node Modules

```javascript
console.log(arguments);
// in browser it will print undefined but in node every file is wrapped in a function so arguments here have a value (exports, module, require, __filename, __dirname)

// hidden wrapping function
(function (exports, module, require, __filename, __dirname) {
  // code in the node file
  console.log(arguments);

  // by default the wrapping function returns module.exports
  return module.exports;
})(module.exports); // iife
```

</br>

---
