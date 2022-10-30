---
Sidebar_position : 3
---

## Node type property and display content

**1) "nodeType Property"**

- The nodeType property provides one more, “old-fashioned” way to get the “type” of a DOM node.

=>It has a numeric value:

1) elem.nodeType == 1 for element nodes

2) elem.nodeType == 3 for text nodes

3) elem.nodeType == 9 for the document object

**Example**

```html
<body>
  <script>
  let elem = document.body;

  alert(elem.nodeType); // 1 => element

  alert(elem.firstChild.nodeType); // 3 => text

  alert( document.nodeType ); // 9
  </script>
</body>
```

**2) Tag: nodeName and tagName**

Given a DOM node, we can read its tag name from nodeName or tagName properties:

**Is there any difference between tagName and nodeName?**

The difference is reflected in their names, but is indeed a bit subtle.

=>The tagName property exists only for Element nodes.

=> The nodeName is defined for any Node:
     -  for elements it means the same as tagName.
     -  for other node types (text, comment, etc.) it has a string with the node type.

=> In other words, tagName is only supported by element nodes (as it originates from Element class), while nodeName can say something about other node types.


**3) innerHtml - contents**

- The innerHTML property allows to get the HTML inside the element as a string.

- We can also modify it. So it’s one of the most powerful ways to change the page.

```html
<body>
  <p>A paragraph</p>
  <div id="div">A div</div>

  <script>
    var myDiv = document.querySelector("#div");
    myDiv.innerHTML = 'The new BODY!'; // replace it
  </script>

</body>

//output
A paragraph
The new BODY!
```

**4) textContent**

- The textContent provides access to the text inside the element: only text, minus all `<tags>`.


**Example:**

```html
<body>
  <p>A paragraph</p>
  <div id="div">A div</div>

  <script>
    var myDiv = document.querySelector("#div");
    var p = document.querySelector("p");
    myDiv.innerHTML = 'The new BODY!'; // replace it
    p.textContent = "New text added"
  </script>
</body>

//output
New text added
The new BODY!
```

