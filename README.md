# JS DOM
## ✨✨Attributes✨✨
```js
<body>
  <div id="elem" about="Elephant"></div>
  <a id="a" href="#hello">link</a>
  <script>
    elem.getAttribute('About') // 'Elephant', reading

    elem.setAttribute('Test', 123); // (2), writing

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