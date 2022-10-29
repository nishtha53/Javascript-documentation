## Selecting and manipulating elements Methods:

**1) getElementById()** 

- The document method, getElementById() will go into your document and look for specific element.

- It will check in html the ID which you have given is proper or not.

```html
<div id="elem">
  <div id="elem-content">Element</div>
</div>

<script>
  // get the element
  let elem = document.getElementById('elem');

  // make its background red
  elem.style.background = 'red';
</script>
```