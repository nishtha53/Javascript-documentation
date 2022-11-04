---
sidebar_position : 8
---

## Event methods

**1) onclick event**

- when the mouse clicks on an element (touchscreen devices generate it on a tap).

Example:

```html
<input type="button" onclick="countRabbits()" value="Count rabbits!">

<script>
  function countRabbits() {
    for(let i=1; i<=3; i++) {
      alert("Rabbit number " + i);
    }
  }
</script>
```

**2) addEventListener**

- Instead of onClick we can also use addEventListener and it takes two paramenters one is which event want to trigger and second is function.

```js
elem.addEventListener( "click" , () => alert('Thanks!'));
```

**3) Submit Event**

- when the visitor submits a `<form>`

**Example**

```html
 <form method="get">
          <label>Your name:
              <input type="text" name="name">
          </label>
          <input type="submit" value="send">
</form>

<script>
var myForm = document.querySelector("form");

myForm.addEventListener("submit", function(e){
    e.preventDefault();

    var formData = document.querySelector('input').value;
    document.write(formData);
});
</script>

// with the help of submit event date will be submite basically used for get formData.
```

**4) Mouseover / Mouseout**

-  when the mouse cursor comes over / leaves an element.

**Example**

```html
<!doctype html>
<html>

<head>
  <meta charset="UTF-8">
  <link rel="stylesheet" href="style.css">
</head>

<body>

  <div id="parent">parent
    <div id="child">child</div>
  </div>
  <textarea id="text"></textarea>
  <input onclick="clearText()" value="Clear" type="button">

  <script src="script.js"></script>

</body>

</html>
```

```js
let parent = document.getElementById('parent');
parent.onmouseover = parent.onmouseout = parent.onmousemove = handler;

function handler(event) {
  let type = event.type;
  while (type.length < 11) type += ' ';

  log(type + " target=" + event.target.id)
  return false;
}


function clearText() {
  text.value = "";
  lastMessage = "";
}

let lastMessageTime = 0;
let lastMessage = "";
let repeatCounter = 1;

function log(message) {
  if (lastMessageTime == 0) lastMessageTime = new Date();

  let time = new Date();

  if (time - lastMessageTime > 500) {
    message = '------------------------------\n' + message;
  }

  if (message === lastMessage) {
    repeatCounter++;
    if (repeatCounter == 2) {
      text.value = text.value.trim() + ' x 2\n';
    } else {
      text.value = text.value.slice(0, text.value.lastIndexOf('x') + 1) + repeatCounter + "\n";
    }

  } else {
    repeatCounter = 1;
    text.value += message + "\n";
  }

  text.scrollTop = text.scrollHeight;

  lastMessageTime = time;
  lastMessage = message;
}
```

**5) Scroll Event**

- The scroll event allows reacting to a page or element scrolling. There are quite a few good things we can do here.

For instance:
- Show/hide additional controls or information depending on where in the document the user is.
     
- Load more data when the user scrolls down till the end of the page.

**Example**

```html
<!----html ----->

<h1>capturing scroll events</h1>
<div></div>
```

```css
/*   css   */

div{
  width: 50px;
  height: 5000px;
  background-color: red;
}
```

```js
// javascript

var pageTop;
window.addEventListener("scroll", function(){
  pageTop = window.pageYOffset;
  console.log(pageTop);
});
```


**6) Window resize Event**

- window resize event is used to resize and know the size in height and width.

**Example**

```html

<h1>Window resize event</h1>

<script>
window.addEventListener("resize", function(){
   console.log(`size of window width is ${window.innerWidth}`);
   console.log(`size of window height is ${window.innerHeight}`);
})
</script>
```


**7) Keyboard: keydown and keyup**

- Keyboard events should be used when we want to handle keyboard actions (virtual keyboard also counts). For instance, to react on arrow keys Up and Down or hotkeys (including combinations of keys).

**Example**

```html
<p>Press key on your keyboard</p>
<script>
document.addEventListener("keydown", function(){
  alert("A key was presses!");
})
</script>

// once any key is pressed alert will show.
```


## Event object

- To properly handle an event we’d want to know more about what’s happened. Not just a “click” or a “keydown”, but what were the pointer coordinates? Which key was pressed? And so on.

- When an event happens, the browser creates an event object, puts details into it and passes it as an argument to the handler.

```html
<input type="button" value="Click me" id="elem">

<script>
  elem.onclick = function(event) {
    // show event type, element and coordinates of the click
    alert(event.type + " at " + event.currentTarget);
    alert("Coordinates: " + event.clientX + ":" + event.clientY);
  };
</script>
```




## Prevent Default Behaviour

- You can use the event object in combniation with preventDefault() method to keep the browser from doing its default behaviour.

```html
<a href="https://google.com">Link to google</a>

<script>
var link = document.querySelector("a");

link.addEventListener("click", function(){
    event.preventDefault();
    alert("Sorry, no google for you");
});
</script>

// it won't redirect to google but give alert message as said in code.
```


