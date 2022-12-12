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
