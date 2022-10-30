---
sidebar_position : 2
---



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

**2) getElementsByTagName()** 

- The document method, getElementByTagName() will give you all the elements with a particular tag name in a collection.

```html
<h1> Dom with tagname</h1>
<p>Learning DOM</p>
<p>Nice to learn dom</p>

<script>
        var myPara = document.getElementsByTagName('p');
        console.log(myPara);
</script>
```

**3) getElementsByClassName()** 

- The document method, getElementsByClassName() is similar to the one getElementsByTagName.It will get all elements that match a particular class.

```html
<h1> Dom with tagname</h1>
<p class="special">Learning DOM</p>
<p class="special">Nice to learn dom</p>

<script>
        var myPara = document.getElementsByClassName('special');
        console.log(myPara);

        for(i=0;i<myPara.length;i++)
        {
            myPara[i].style.color = "red";
        }
</script>
```

**4) querySelector()** 

- The document method querySelector() will return the first match of a query.

```html
<div id = "special">
   <p class="special">Here is some text</p>
</div>

<script>
    var myText = document.querySelector("#special");
    myText.style.color = "yellow";
</script>
```

=> In querySelector, if Id is given need to select element with `#`

=> In querySelector, if class is given need to select element with `.`

=> In querySelector, if tag name is given need to select element with `write tag name`


**5) querySelectorAll()** 

- The document method querySelectorAll() will get all elements that match a certain selector. It returns nodelist of elements that have same classname.

```html
<div class="special">
  <p> one para </p>
  <p> second para </p>
</div>

<script>
        var myText = document.querySelectorAll(".special");
        for(var i=0;i<myText.length;i++)
        {
            myText[i].style.color = "red"
        }
</script>
```
