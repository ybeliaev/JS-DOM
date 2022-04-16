# JS DOM
## ✨✨Attributes✨✨
```js
<body>
  <div id="elem" about="Elephant"></div>
  <a id="a" href="#hello">link</a>
  <script>
    elem.getAttribute('About') // 'Elephant', reading

    elem.setAttribute('Test', 123); // writing

    elem.outerHTML;  // <div id="elem" about="Elephant" test="123"></div>
    
    elem.attributes // [id, about, test]
    //NamedNodeMap {0: id, 1: about, 2: test, id: id, about: about, test: test, length: 3}
    // id.name = 'id', id.value = 'elem'

    a.getAttribute('href'); // #hello
    a.href // full URL in the form http://.../...#hello
  </script>
</body>
```
### 💡 InnerHTML vs OuterHTML
![InnerHTML vs OuterHTML](./src/difference-between-innerhtml-and-outerhtml.png)

### Получение элемента с  атрибутом
```js
<div data-widget-name="menu">Choose the genre</div>
```
> `let elem = document.querySelector('[data-widget-name]');`
### Attributes starting with “data-”
> They are available in the dataset property.
```js
<body data-about="Elephants">
<script>
  document.body.dataset.about; // Elephants
</script>
```
## ✨✨Node manipulation✨✨

```js
// 1. Create <div> element
let div = document.createElement('div');

// 2. Set its class to "alert"
div.className = "alert";

// 3. Fill it with the content
div.innerHTML = "<strong>Hi there!</strong> You've read an important message.";

// 4. Adding an element
document.body.append(div);

// 5. Removal node
setTimeout(() => div.remove(), 1000);
```
### cloneNode
>The call `elem.cloneNode(true)` creates a “deep” clone of the element – with all attributes and subelements. 
>If we call `elem.cloneNode(false)`, then the clone is made without child elements.
```js
<body>
    <div class="alert" id="div">
    <strong>Hi there!</strong> You've read an important message.
    </div>

    <script>
    // clone the message
    let div2 = div.cloneNode(true);
     // change the clone 
    div2.querySelector('strong').innerHTML = 'Bye there!';
    // show the clone after the existing div
    div.after(div2); 
    </script>
</body>
```
## ✨✨Node create, styled and classes✨✨
* createElement
* `let elem = document.createElement('div');`
*  className
* `elem.className = "notification";`   
* classList   
* `elem.classList.add(className);`
* style
* `elem.style.top = top + 'px';`
* innerHTML
* `elem.innerHTML = html;`
* append
* `document.body.append(elem);`
* remove
* `setTimeout(() => div.remove(), 1500);`
  
## ✨✨Size and scrolling✨✨