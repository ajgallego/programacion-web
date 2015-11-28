# Eventos

En esta sección de describe un concepto un poco más avanzado: los eventos. Un evento, como su nombre indica, es cuando sucede una determinada acción sobre un elemento. HTML permite escuchar estos eventos y asociarles un comportamiento o acción que se realizará cuando suceda dicho evento. La forma de definirlos es similar a los atributos (`evento="ACCION"`), la acción hará referencia a una función o método en lenguaje JavaScript. Algunos de los eventos que podemos utilizar son:

* **onload**: se activa cuando el navegador termina de cargar todos los elementos de la página.

* **onclick**: cuando se presiona el botón del ratón sobre un elemento.

* **onmouseover**: se dispara cuando el cursor del ratón pasa sobre un elemento.

* **onmousemove**: cuando se mueve el cursor del ratón mientras está sobre un elemento.

* **onmouseout**: se activa cuando el cursor del ratón sale fuera de un elemento (sobre el que estaba).

* **onfocus**: ocurre cuando un elemento recibe el enfoque (el cursor de escritura), ya sea con el puntero o con mediante la tecla tabulador.

* **onkeypress**: ocurre cuando se presiona una tecla (dentro de un elemento, por ejemplo un campo de escritura).

* **onkeydown**: se dispara cuando una tecla es presionada (dentro de un elemento)

* **onkeyup**: cuando una tecla es soltada.

* **onsubmit**: se activa cuando un formulario es enviado.

* **onreset**: ocurre cuando un formulario es reseteado.

* **onchange**: ocurre cuando un control pierde el enfoque y su valor ha sido modificado desde que recibió el enfoque.

* etc. (Ver sección [eventos](capitulo_javascript_eventos.html) en el capítulo de JavaScript)


Por ejemplo, podemos enlazar el evento "`onkeyup`" de un `textarea` con una función de JavaScript de la forma:

```html
<script type="text/javascript">
   function saveText() {
      // acciones JavaScript
   }
</script>

<textarea id="myarea" cols="80" rows="15" onkeyup="saveText()"></textarea>
```

Los eventos se verán más en detalle en el capítulo correspondiente de la sección dedicada a Javascript (Ver sección [eventos](capitulo_javascript_eventos.html)). De momento, solo es importante que aprendráis que se puede asociar código JavaScript a determinados eventos o acciones que se producen en los campos HTML de una página Web. 



