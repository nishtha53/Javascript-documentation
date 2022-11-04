---
sidebar_position : 8
---

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


