# Modelo de caja básico

Se han añadido nuevas propiedades para la disposición de elementos dentro de una caja:

* **overflow: visible | hidden | scroll | auto;** - permite indicar que ocurrirá si el contenido excede el área de un elemento, acepta cuatro posibles valores:
  * _visible_: No se recorta el contenido, la parte que quede fuera será visible. Es el valor por defecto.
  * _hidden_: El contenido que sobresalga será ocultado y tampoco se mostrará la barra de scroll.
  * _scroll_: El contenido se recorta y el navegador muestra la barra de scroll para ver el resto del contenido.
  * _auto_: Si el contenido se recorta el navegador mostrará una barra para ver el resto del contenido.
* **overflow-x**: igual que overflow pero indicaremos solo la propiedad en horizontal.
* **overflow-y**: igual que overflow pero solo para vertical.
* **resize: none | horizontal | vertical | both;** - habilita la posibilidad de redimensionar "manualmente" una caja. Puede tomar los valores: none, horizontal (permitir redimensionar solo en horizontal), vertical (solo en vertical), o both (redimensionar ambas dimensiones). Se recomienda además añadir la propiedad "overflow: hidden" para ocultar los elementos al redimensionar. Por ejemplo:

```css
resize:both;
overflow:auto;
```

