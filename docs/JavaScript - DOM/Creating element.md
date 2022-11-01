---
sidebar_position : 5
---

## To create DOM nodes, there are two methods:

**1) `document.createElement(tag)`**

- Creates a new element node with the given tag:

  => `let div = document.createElement('div');`

**2) `document.createTextNode(text)`**

- Creates a new text node with the given text:

  => `let textNode = ocument.createTextNode('Here I am');`


### How to insert elements?

- Insert elements with  `document.body.append(div)`.


## Example:

```html
<body>
        <div>
                    <p>This is first para </p>
        </div>

        <script>
                var mytag = document.createElement('p');
                var myText = document.createTextNode("Second para");

                mytag.appendChild(myText);

                var myDiv = document.querySelector('div');
                myDiv.appendChild(mytag);
        </script>
</body>


//output

This is first para
Second para
```



