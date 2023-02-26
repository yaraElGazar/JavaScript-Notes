# JavaScript Notes - Elzero

Playlist Link : </br>
<https://www.youtube.com/watch?v=GM6dQBmc-Xg&list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv>

Code & Notes : </br>
<https://elzero.org/category/courses/javascript-bootcamp/>

Assignments : </br>
<https://elzero.org/category/assignments/javascript-bootcamp-assignments/>

</br>

---

## What can JS do?

1. Dynamically update content
2. Manipulate HTML & CSS
3. Animate images and content
4. Manipulate and validate Data
5. Control Multimedia
6. Games
7. Mobile Apps

</br>

---

## Where to put the \<script> tag ?

We have 2 ways </br>

1. In the \<head>
2. In the \<body>
   </br>

_It dapends on the order of executing the code_
</br>
If you are using elements that are availbale after the page is loaded you should put the \<script> tag last thing in the \<body> otherwise if you want to include it in the head you should use the onload event.
</br>

```javascript
main.js

window.onload = function () {

    YOUR CODE
}

```

</br>

---

## Console

```javascript
console.log();
console.error("Error");
console.table([1, 2, 3]);

// Styling console messages
console.log(
  "Hello from %cJS %cFiLe",
  "color: red; font-size: 40px",
  "color: blue; font-size: 40px"
);

// JS will be red and File will be blue

// %c is called Directive, it specifies the words that will take the style
```

</br>

---

## Web API

_console is a part of web API_
</br>
What is **Web API** ?
</br>
API stands for Application Programming Interface.

A Web API is an application programming interface for the Web.

A Browser API can extend the functionality of a web browser.

A Server API can extend the functionality of a web server.

</br>

---

## Variables

1.

```js
// HTML
<div id="hello"> Hello world! </div>;

// JS
hello.innerHTML = "Hello updated!";

/*When you use an id, a global variable is created with the same name*/
```

2.

```js
/* When you use var for variable declaration the variable is added to the window object => Causes variable scope drama */

var x = 10;
console.log(window.x); //10
```

</br>

---

## Template Literals

```js
/* Can be used to write HTML elements in an efficient way */

let title = "Elzero";
let desc = "Elzero Web School";

let markup = `
  <div class="card">
    <div class="child">
      <h2>${title}</h2>
      <p>${desc}</p>
    </div>
  </div>
`;

document.write(markup);
```

</br>

---

## Unary operators

```js
/* Can be used to convert strings or any type of data to numbers */

console.log(+100); // 100
console.log(+"100"); // 100
console.log(+"-100"); // -100
console.log(+"Osama"); // NaN
console.log(+"15.5"); // 15.5
console.log(+0xff); // 255
console.log(+null); // 0
console.log(+false); // 0
console.log(+true); // 1

// Another way to convert strings to numbers is the Number() constructor

console.log(Number("100")); // 100
```

</br>

---

## Number

```js
/*Numbers in JS are stored as double precision*/

/*Syntactic sugar -> using '_' to display numbers in a more descriptive way for the developers*/

cosole.log("1_000_000"); // 1000000

/*Number methods*/
// Two dots (one for float and the other for the method) to call the method or paranthesis

// 1) .toString()
console.log((100).toString()); // 100

// 2) .toFixed() -> returns a string
console.log((100.555556).toFixed(2)); // 100.56

// 3) parseInt()/ parseFloat()
console.log(parseInt("100")); // 100
console.log(parseInt("x 100")); // NaN
console.log(parseInt("100 x")); // 100
console.log(parseInt("100.5")); // 100
console.log(parseFloat("100.5")); // 100.5

// 4) Number.isIntger()
console.log(Number.isInteger("100")); // false
console.log(Number.isInteger(100.5)); // false
console.log(Number.isInteger(100)); // true

// 5) Number.isNaN() -> true only if JS returns NaN
console.log(Number.isNaN("Osama")); // false
console.log(Number.isNaN("Osama" / 20)); // false
```

## Nullish Coalescing Operator And Logical Or

```js
/* Default values if the variable is falsey */
let price; // undefined
console.log(`The Price is ${price || 200}`);

/* Default values if the variable is null or undefined (Nullish Coalescing)*/
console.log(`The Price is ${price ?? 200}`); // only prints 200 if price is undefined or null
```

## this keyword

```js
document.getElementById("btn").onclick = function () {
  console.log(this);
};

// When the button is clicked, this will refer to the button with the id btn and will print it to the console (can be used if multiple buttons exist and you want to know which one has been clicked)
```

## simulate the events

```js
let btn = document.getElementById("btn");

btn.addEventListener("click", function () {
  console.log("clicked");
});

setTimout(function () {
  btn.click(); // simulate the click event
}, 1000);

/* After one second the button is automatically clicked and the event is fired*/
```
