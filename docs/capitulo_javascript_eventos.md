# Eventos

Los eventos permiten ejecutar acciones cuando sucede un determinado evento o se realiza una determinada acción sobre un elemento HTML de nuestra página Web. La forma de definirlos es similar a los atributos HTML (`evento="acción"`), donde la acción hará referencia a una función o método en lenguaje JavaScript:

```html
<div onclick="CODIGO-JAVASCRIPT"></div>
```

Algunos de los eventos que podemos utilizar son:

* **onload**: se activa cuando el navegador termina de cargar todos los elementos de la página.

* **onunload**: se activa al cerrar una página.

* **onclick**: cuando se presiona el botón del ratón sobre un elemento.

* **ondblclick**: se activa al hacer doble clic sobre un elemento.

* **onmousedown**: se activa al presionar el botón del ratón (mientras que está presionado).

* **onmouseup**: cuando el botón del ratón es liberado.

* **onmouseover**: se dispara cuando el cursor del ratón pasa sobre un elemento.

* **onmousemove**: cuando se mueve el cursor del ratón mientras está sobre un elemento.

* **onmouseout**: se activa cuando el cursor del ratón sale fuera de un elemento (sobre el que estaba).

* **onfocus**: ocurre cuando un elemento recibe el enfoque (el cursor de escritura), ya sea con el puntero o con mediante la tecla tabulador.

* **onblur**: se dispara cuando un elemento pierde el enfoque (ya sea por hacer clic fuera o por presionar la tecla tabulador).

* **onkeypress**: ocurre cuando se presiona una tecla (dentro de un elemento, por ejemplo un campo de escritura).

* **onkeydown**: se dispara cuando una tecla es presionada (dentro de un elemento)

* **onkeyup**: cuando una tecla es soltada.

* **onsubmit**: se activa cuando un formulario es enviado.

* **onreset**: ocurre cuando un formulario es reseteado.

* **onselect**: cuando el usuario selecciona un texto en un campo de texto.

* **onchange**: ocurre cuando un control pierde el enfoque y su valor ha sido modificado desde que recibió el enfoque.


Ejemplos de uso:

```html
<!-- Dos eventos en una misma etiqueta... -->
<div onclick="alert('Has hecho click');" onmouseover="alert('Acabas de pasar por encima');">
    Puedes pinchar sobre este elemento o simplemente pasar el ratón por encima
</div>

<!-- Comprobar que la página se ha cargado... -->
<body onload="alert('La página se ha cargado completamente');">
    ...
</body>

<!-- Tambień se pueden llamar a funciones desde los eventos... -->
<script type="text/javascript">
   function saveText() {
      // acciones JavaScript
   }
</script>

<textarea id="myarea" cols="80" rows="15" onkeyup="saveText()"></textarea>
```


## Eventos y la variable _this_

JavaScript define una variable especial llamada _this_ que se crea automáticamente y que se emplea en algunas técnicas avanzadas de programación. En los eventos, se puede utilizar la variable _this_ para referirse al elemento que ha provocado el evento.

Esta variable es muy útil para ejemplos como el siguiente: queremos que al pasar por encima de un `<div>` el color del borde cambie, y al salir del contenedor restablezca el color inicial. Si no usamos la variable _this_ el código sería el siguiente:

```html
<div id="contenidos" style="width:150px; height:60px; border:thin solid silver"
onmouseover="document.getElementById('contenidos').style.borderColor='black';"
onmouseout="document.getElementById('contenidos').style.borderColor='silver';">
    Sección de contenidos...
</div>
```

Sin embargo, usando la variable _this_ quedaría mucho más claro:

```html
<div id="contenidos" style="width:150px; height:60px; border:thin solid silver"
onmouseover="this.style.borderColor='black';"
onmouseout="this.style.borderColor='silver';">
    Sección de contenidos...
</div>
```

Si quisieramos llamar a una función externa, también es posible usar la variable _this_ para pasarle como parámetro el elemento sobre el cual se quiere actuar, por ejemplo:

```html
<script>
function setColor(element, color) {
    element.style.borderColor = color;
}
</script>

<div id="contenidos" style="width:150px; height:60px; border:thin solid silver"
onmouseover="setColor(this,'black');" onmouseout="setColor(this,'silver');">
    Sección de contenidos...
</div>
```

