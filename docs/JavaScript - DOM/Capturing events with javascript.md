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
