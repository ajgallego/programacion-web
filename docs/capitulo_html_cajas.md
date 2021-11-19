# Cajas (etiqueta `<div>`)

La etiqueta `<div></div>` permite crear cajas contenedoras de otros elementos. Esta etiqueta no muestra (por defecto) ningún estilo ni formato visual, sino que es utilizada únicamente para organizar la disposición de los elementos en la página. Es muy sencillo indicar su posición de forma absoluta o relativa en la página y crear divisiones del espacio para distribuir los elementos. 

Estas cajas pueden contener cualquier tipo de elemento (texto, imágenes, etc.) u otras etiquetas `<div>` para crear subdivisiones. 

A continuación se incluye un pequeño ejemplo de su uso: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
    <title>Ejemplo de uso de la etiqueta DIV</title>
    <meta charset="utf-8">
</head>
<body>
   <div>Menu superior</div>
   
   <div>
        <h1>Contenido central</h1>
        
        <div>
            Artículo 1 
        </div>
        
        <div>
            Artículo 2
        </div>
   </div>
   
   <div>Pie de página</div>
</body>
</html>
```

Como se puede ver se ha utilizado una etiqueta `<div>` para crear una sección que contendrá el menú superior, otra para el contenido central y otra para el pie de página. La sección con el contenido central se divide a su vez en otras dos secciones o cajas que contendrán los artículos. 

Si guardamos este código de ejemplo en un archivo y lo abrimos veremos que esta etiqueta no muestra ningún formato ni estilo, solamente nos aparecerán los textos que hemos puesto. Para poder completar este código e indicar la posición y estilos nos hará falta utilizar CSS. En la sección de "[Introducción a CSS](capitulo_css.html) `>` [Capas](capitulo_css_capas.html)" se explica más a fondo el uso de esta etiqueta y como la podemos utilizar para alinear los contenidos o crear secciones con estilos definidos. 


> Para alinear el contenido de una página se recomienda el uso de la etiqueta `<div>` junto con CSS. No es recomentable el uso de la etiqueta `<table>` para crear alineaciones. 






