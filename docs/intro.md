---
sidebar_position: 1
---

# Introduction to JavaScript

<h3>Let's understand what is JavaScript?</h3>

- JavaScript is a scripting or programming language that allows you to implement complex features on web pages.

- JavaScript is HIGH-LEVEL Object- oriented programming, Multi-Paradigm programming language.

## Getting Started with Hello World

Hello world is very basic program to start with: 

```javascript
console.log("Hello World!");
```


## How many ways JavaScript can be added in browser??

<h3>Using Script tag in HTML</h3>

- In html file you can use `<script></script>` tag and under that write Javascript code.

=> Let's see an example:

```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>
<h2>Demo JavaScript in Head</h2>

<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```


<h3>Individual .js file</h3>

- JavaScript can be added with `<script> </script>` tag.
- Javascript should be linked at last of line as code works line by line and first html css will be loaded and then script will be loaded.
- src attribute is used for giving source of file i.e what is file name and which location.

=> Suppose file is named as index.html:

```html
<!-- Html File -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript file added</title>
</head>
<body>
      <p> JavaScript Loaded </p>

      <script src="./app.js"></script>
</body>
</html>
```

JavaScript File is: 
```javascript
// app.js file
document.write("Hello I am Nishtha!!");
```

Output
```
It will print: 
    JavaScript Loaded
    Hello I am Nishtha!!
```


