# JS DOM
## ✨✨Attributes✨✨
```js
<body>
  <div id="elem" about="Elephant"></div>

  <script>
    elem.getAttribute('About') // 'Elephant', reading

    elem.setAttribute('Test', 123); // (2), writing

    elem.outerHTML;  // <div id="elem" about="Elephant" test="123"></div>
    
    elem.attributes // [id, about, test]
    //NamedNodeMap {0: id, 1: about, 2: test, id: id, about: about, test: test, length: 3}
    // id.name = 'id', id.value = 'elem'
  </script>
</body>
```
### 💡 InnerHTML vs OuterHTML
![InnerHTML vs OuterHTML](./src/difference-between-innerhtml-and-outerhtml.png)
