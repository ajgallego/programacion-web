# Estructura básica de una Web

Un documento HTML comienza con la etiqueta `<html>` y termina con `</html>`. Dentro del documento (entre las etiquetas de principio y fin de html) hay dos zonas bien diferenciadas: el encabezamiento, delimitado por `<head>` y `</head>`, que sirve para incluir definiciones iniciales válidas para todo el documento; y el cuerpo, delimitado por `<body>` y `</body>`, donde reside la información del documento.

Las etiquetas básicas o mínimas son:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
   <title>Ejemplo</title>
</head>
<body>
   ¡Hola mundo!
</body>
</html>
```

La primera línea es el DOCTYPE, o el tipo de documento que viene a continuación. En este caso se usa el estándar de HTML 4.01 (el último estándar adoptado en 1999, ya que HTML5 a fecha de 2011 sigue siendo un borrador). La siguiente etiqueta, `<html>`, define el inicio del documento HTML, e indica que lo que viene a continuación debe ser interpretado como código HTML. Como podemos ver en la última línea, se cierra la etiqueta `</html>`.

Dentro de estas etiquetas `<html> ... </html>` encontramos las dos secciones mencionadas: 

* Encabezamiento (`head`): Esta sección inicial contiene todos los elementos _no visuales_ de nuestra web, como por ejemplo los metadatos descriptivos (autor, palabras clave, descripción del contenido, etc.), los estilos a utilizar en los elementos visuales del cuerpo, el título que aparecerá en la barra superior del navegador (como en el ejemplo superior), y otra serie de elementos que se estudiarán más en detalle en la siguiente sección.

* Cuerpo (`body`): Aquí hemos de incluir todos los contenidos _visuales_ de nuestra web, todos los textos, imágenes, enlaces, etc. En el ejemplo de arriba lo único que se incluye es el texto "¡Hola mundo!" por lo que al abrir esta web nos aparecerá una página web que incluirá únicamente ese texto. 


En los siguientes apartados se describirán más en detalle los elementos que podemos utilizar dentro del encabezamiento o del cuerpo de una web. En primer lugar se estudiarán los elementos de la cabecera y a continuación todas las etiquetas HTML que se suelen utilizar para la construcción de una web. 