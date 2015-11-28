# Mark

HTML5 también introduce un conjunto nuevo de elementos _inline_, solo que ya no se llaman elementos inline sino _text-level semantics_ o semántica a nivel de texto. Uno de ellos es la etiqueta mark. Cuando realizamos una búsqueda en ciertos sitios, los elementos encontrados en la página aparecen remarcados para facilitar su localización. Hasta ahora el estilo se aplicaba con etiquetas `<span>`, pero esta solución no es semántica. Es ahí donde entra en escena la nueva etiqueta `<mark>`:


```html
<h1>Resultados de la búsqueda de la palabra ’anillo’</h1>
<ol>
   <li>El señor de los <mark>anillo</mark>s...</li>
   <li>el cliente compró este <mark>anillo</mark></li>
</ol>
```

Si queremos podemos redefinir el estilo de esta nueva etiqueta de la misma forma que lo hacíamos con las etiquetas de HTML, por ejemplo, para cambiar el color de fondo a rojo:


```css
mark { background-color: red; }
```
