# Elementos de la cabecera

La sección de cabecera `<head> ... </head>` se utiliza para describir el tipo de contenido y aspecto visual que tendrá la web. Es importante destacar que todo el contenido de la sección de cabecera **no** se muestra directamente al usuario, sino que es únicamente información descriptiva y metadatos. Por ejemplo, nos permitirá indicar metadatos que son muy útiles para la indexación de la web en buscadores, como el tipo de contenido, palabras clave o el autor, o indicar los estilos con los cuales se mostrarán los elementos visuales, entre otra información. 

Algunas de las principales etiquetas que podemos utilizar dentro de la cabecera son:

* `<title></title>`: define el título de la página. Por lo general el título aparece en la barra de título encima de la ventana.

* `<link/>`: para vincular el sitio con hojas de estilo externas (ver la sección de CSS para más información):
```html
<link rel="stylesheet" href="style.css" type="text/css"/>
```
El atributo `rel` es requerido y describe el tipo de documento enlazado (en este caso una hoja de estilo). El atributo `type` es simplemente indicativo del tipo de hoja de estilo enlazada (en este caso CSS).


* `<style></style>`: se utiliza para añadir definición de estilo en línea. No es necesario colocarlo si se va a utilizar una hoja de estilo externa usando la etiqueta `<link/>` (que es lo más habitual y recomendable). El uso correcto sería de la forma:
```html
<html>
<head>
   ...
   <style type="text/css">
      Estilos CSS
   </style>
</head>
<body></body>
</html>
```
Para más información ver la sección CSS del manual.


* `<meta/>`: para indicar metadatos como la descripción de la web, los keywords, o el autor:
```html
<meta name="description" content="Descripción de la web" />
<meta name="keywords" content="key1,key2,key3" />
<meta name="author" content="Nombre del autor" />
```
Una etiqueta "meta" **muy útil** es la de la codificación, que nos permitirá escribir texto con acentos y se se vea bien (sin símbolos extraños) en todos los navegadores: 
```html
<meta charset="utf-8"/>
```


* `<script></script>`: permite incluir un script en la Web. El código se puede escribir directamente entre las etiquetas de `<script>` o cargar desde un fichero externo utilizando el atributo `src="url del script"` para indicar la dirección del fichero. Se recomienda incluir el tipo MIME en el atributo `type`, que en el caso de código JavaScript sería `text/javascript`. A continuación se incluyen algunos ejemplos de uso:
```html 
<script src="fichero.js" type="text/javascript"></script>
<script type="text/javascript">
    Código de un script integrado en la página
</script>
``` 
Cuando usamos el atributo `src` el contenido de estas etiquetas está vacío (no encierra nada), esto es porque lo carga directamente desde el fichero indicado. En el capítulo sobre JavaScript podréis encontrar mucha más información sobre como utilizar estas etiquetas. 



A continuación se incluye un código de ejemplo en el que se ha ampliado la estructura HTML básica de una web que vimos en la sección anterior para añadir algunas de estas etiquetas: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
    <title>Ejemplo</title>
    
    <meta charset="utf-8"/>
    <meta name="description" content="Descripción de la web" />
    <meta name="keywords" content="key1,key2,key3" />
    <meta name="author" content="Nombre del autor" />
    
    <link rel="stylesheet" href="style.css" type="text/css"/>
    
    <script src="javascript.js" type="text/javascript"></script>
</head>
<body>
   ¡Hola mundo!
</body>
</html>
```






