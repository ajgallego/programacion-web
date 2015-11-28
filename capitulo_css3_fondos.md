# Fondos

CSS3 también ha introducido nuevas propiedades para definir el estilo de las imágenes de fondo:

* **background-origin: border-box | padding-box | content-box** - permite definir el origen de coordenadas sobre el que se va a colocar la imagen de fondo. Acepta tres posible valores: "border-box" para que el fondo empiece desde el mismo borde del elemento, "padding-box" para que la imagen de fondo se coloque a partir del espaciado de padding, y por último "content-box" para que la imagen de fondo se coloque donde empieza el contenido del elemento, sin tener en cuenta el borde ni el padding.

* **background-clip: border-box | padding-box | content-box** - define el área sobre la que se extiende la imagen de fondo, puede tomar tres valores: "border-box" se extiende por toda el área dentro de la zona definida a partir del borde, "padding-box" se extiende a partir del espaciado de padding y "content-box" el fondo se extiende solo dentro del área de contenido.

* **background-size**: Permite indicar el tamaño de la imagen de fondo. Acepta diferentes atributos:

  * background-size: 200px; // especifica ancho y alto a la vez
  * background-size: 200px 100px; // 200px de ancho y 100px de alto
  * background-size: auto 200px; // ajustar la anchura automáticamente
  * background-size: 50% 25%; // También podemos indicar el tamaño con porcentajes
  * background-size: contain; // Escalar la imagen al tamaño máximo posible (conservando las proporciones originales) para que quepa dentro del área asignada.
  * background-size: cover; // Escalar la imagen para que cubra completamente el área asignada (conservando las proporciones originales).
  * Capas con múltiples imágenes de fondo: Con la propiedad **background** ahora podemos indicar varias imágenes de fondo, simplemente separándolas con comas. Para cada propiedad background debemos definir cuatro valores: imagen de fondo, posición vertical, posición horizontal, modo de repetición (repeat, repeat-x, repeat-y, no-repeat). Ejemplo:

```css
background: url(imagen1.png) 10px center no-repeat,
            url(imagen2.png) 0 center repeat-x;
```

Dado que estas propiedades no son soportadas todavía en todos los navegadores, deberemos de definirlas también añadiendo los prefijos "-webkit-" y "-moz-" para dar un mayor soporte.

