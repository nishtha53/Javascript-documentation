---
sidebar_position : 6
---

## How to remove element from DOM

- If you want to remove any element from html need to use  `removeChild()` but you can only call it on the parentNode of the element you want to remove.


### Example:

```html
<body>
        <div>
            <p>This is first para </p>
            <p>Second para</p>
        </div>

        <script>
            var myDiv = document.querySelector('div');
            myDiv.removeChild(myDiv.children[1]);
        </script>
</body>
```

- The modern approach to removing an element is the remove() method. Just call this method on the element you want to remove from the DOM

### Example

```html
<body>
        <div>
            <p id ="one">This is first para </p>
            <p>Second para</p>
        </div>

        <script>
            var myDiv = document.querySelector('div');
            var oneP = document.querySelector("#one");
            oneP.remove();
        </script>
</body>

// it will remove first para from html.
```
