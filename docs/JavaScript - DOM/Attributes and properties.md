---
sidebar_position : 4
---

## Html  attributes

- In HTML, tags may have attributes. When the browser parses the HTML to create DOM objects for tags, it recognizes standard attributes and creates DOM properties from them.

- So when an element has id or another standard attribute, the corresponding property gets created. But that doesn’t happen if the attribute is non-standard.

**All attributes are accessible by using the following methods:**

1) elem.hasAttribute(name) – checks for existence.

2) elem.getAttribute(name) – gets the value.

3) elem.setAttribute(name, value) – sets the value.

4) elem.removeAttribute(name) – removes the attribute.

**Example of `getAttribute` and `setAttribute`**

 ```html
 <body>
  <div id="elem" about="Elephant"></div>

  <script>
    alert( elem.getAttribute('About') ); // (1) 'Elephant', reading

    elem.setAttribute('Test', 123); // (2), writing

    alert( elem.outerHTML ); // (3), see if the attribute is in HTML (yes)

    for (let attr of elem.attributes) { // (4) list all
      alert( `${attr.name} = ${attr.value}` );
    }
  </script>
</body>
```

