# Pseudo-clases

Una *pseudo-clase* permite tener en cuenta diferentes condiciones o eventos al definir una propiedad para una etiqueta HTML, por ejemplo si un enlace ha sido visitado o si el cursor del ratón está sobre un elemento. Algunas de las pseudo-clases que podemos utilizar son:

* _a:link_ - enlace que no ha sido explorado por el usuario.
* _a:visited_ - se refiere a los enlaces ya visitados.
* _a:active_ - enlace seleccionado con el ratón.
* _a:hover_ - enlace con el puntero del ratón encima, pero no seleccionado.
* _a:focus_ - enlace con el foco del sistema. También puede ser usado para un input.
* _p:first-letter_ - primera letra de un párrafo.
* _p:first-line_ - primera línea de un párrafo.

Utilizando estos elementos podemos configurar por ejemplo:

```css
a { color: black; }
a:hover { color: blue; }
a:visited { color: darkgreen; }
p:first-letter {color: green; font-size: x-large;}
```

En este ejemplo se aplica el color azul al texto de los enlaces solo cuando el ratón esté encima. Es decir, el texto del enlace tendrá por defecto el color negro, pero cuando el cursor del ratón pase por encima el color cambiará a azul. Además también se asigna el color del texto verde oscuro a los enlaces ya visitados, por lo que el usuario podrá ver marcados de este color los enlaces que ya ha pulsado anteriormente. Por último también se indica que la primera letra de los párrafos tenga el color verde y un tamaño más grade.

Las *pseudo-clases* no se pueden incluir en el estilo en línea de un elemento, por lo tanto las tendremos que definir bien en la hoja de estilos externa o en la sección *style* de la cabecera, por ejemplo: 

```html
<html>
<head>
    <style type="text/css">
        a {
            background-color: white;
        }
        a:hover {
            background-color: blue;
        }
    </style>
</head>
...
```