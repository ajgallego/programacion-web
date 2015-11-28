

# Como incluir JavaScript en nuestra página Web

La integración de JavaScript y XHTML es muy flexible, ya que existen al menos tres formas para incluir código JavaScript en las páginas web.

## Incluir desde un archivo externo

Las instrucciones JavaScript se pueden incluir en un archivo externo de tipo JavaScript que los documentos XHTML enlazan mediante la etiqueta `<script>`.

```html
<script type="text/javascript" src="/js/codigo.js"></script>
```

Se pueden crear todos los archivos JavaScript que sean necesarios y cada documento XHTML puede enlazar tantos archivos JavaScript como necesite. La principal ventaja de enlazar un archivo JavaScript externo es que se simplifica el código de la página, que se puede reutilizar el mismo código JavaScript en todas las páginas del sitio web y que cualquier modificación realizada en el archivo JavaScript se ve reflejada inmediatamente en todas las páginas que lo enlazan.

## Incluir en el mismo documento HTML

El código JavaScript se encierra entre etiquetas `<script>` y se incluye en cualquier parte del documento:

```html
<script type="text/javascript">
    alert("Hola mundo!");
</script>
```

Aunque es correcto incluir cualquier bloque de código en cualquier zona de la página, se recomienda definir el código JavaScript dentro de la cabecera del documento (sección `<head>`) o al final de la página (antes de la etiqueta de cierre `</body>`. Con esta segunda opción se consigue mejorar el tiempo de carga de la página, ya que primero se mostrará todo el contenido de la web y por último se cargarán los javascript.


## Incluir en los elementos HTML

Consiste en incluir trozos de JavaScript dentro del código HTML de la página, por ejemplo:

```html
<p onclick="alert('Un mensaje de prueba')">Un párrafo de texto.</p>
```

El principal inconveniente de este método es que ensucia innecesariamente el código HTML de la página y complica el mantenimiento del código JavaScript.



