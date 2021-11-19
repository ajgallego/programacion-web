# Adjuntar una hoja de estilo

La información de estilo puede ser adjuntada de tres formas diferentes:

* **Hoja de estilo externa**: es una hoja de estilo que está almacenada en un archivo diferente al archivo HTML (por ejemplo llamado "estilo.css"). Esta es la manera de programar más potente y la que deberemos de utilizar por defecto, ya que separa completamente las reglas de estilo de la página HTML y además nos permite usar dicha hoja de estilo en todas las páginas HTML que queramos. La hoja de estilo debe de ser enlazada con el código HTML de la forma:

```html
<html>
<head>
   <link rel="stylesheet" type="text/css" href="estilo.css"/>
   ...
</head>
...
```

* **Hoja de estilo interna**: es una hoja de estilo que está incrustada dentro del documento HTML. En general, el motivo para usar una hoja de estilo interna, es cuando se quiere diferenciar con algún estilo uno de los ficheros HTML de nuestra Web. Este código debe de estar incluido en la sección de cabecera `<head>` y entre las etiquetas `<style>`. La forma de incluir el código sería de la forma:

```html
<html>
<head>
   <style type="text/css">
      H1 { color:blue; text-align:center }
   </style>
</head>
...
```

* **Estilo en línea (inline):** es un método para insertar los estilos CSS directamente dentro de una etiqueta HTML. Esta opción la usaremos **únicamente** cuando queramos aplicar un estilo sobre una única etiqueta o un único elemento. En cualquier otro caso usaremos alguna de las opciones anteriores, ya que si por ejemplo aplicamos un mismo estilo a muchas etiquetas usando esta opción y después queremos cambiar algo de ese estilo tendríamos que cambiarlo en todas las etiquetas, mientras que si tenemos una hoja de estilo centralizada con un único cambio será suficiente. 
Para incluir un estilo en línea o _inline_ se usa el atributo `style` de la forma:

```html
<h1 style="color:blue; text-align:center">...</h1>
```
