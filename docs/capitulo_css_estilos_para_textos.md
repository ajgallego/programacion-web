## Estilos para textos

En esta sección se describen los principales estilos CSS que podemos utilizar para cambiar la apariencia de los textos de una Web. Para cada uno de ellos se indica el nombre del atributo, los posibles valores que le podemos asignar, algunos ejemplos y una explicación de uso. 


* **color:** valor RGB o nombre de color<br/>
*Ejemplos*: color: #009900; color: red;<br/>
Sirve para indicar el color del texto. Lo admiten casi todas las etiquetas de HTML. No todos los nombres de colores son admitidos en el estándar, es aconsejable entonces utilizar el valor RGB. Algunos de los principales nombres de colores son: white, black, gray, blue, red, green o yellow, para más nombres podemos consultar la dirección "<a href="http://www.w3schools.com/cssref/css_colornames.asp">http://www.w3schools.com/cssref/css_colornames.asp</a>".

* **font-size:** xx-small|x-small|small|medium|large|x-large|xx-large|Unidades CSS<br/>
*Ejemplos*: font-size: 12pt; font-size: x-large; <br/>
Sirve para indicar el tamaño de las fuentes de manera más rígida y con mayor exactitud.

* **font-family:** serif | sans-serif | cursive | fantasy | monospace | Etc. <br/>
*Ejemplos*: font-family: arial,helvetica; font-family: fantasy; <br/>
Con este atributo indicamos la familia de tipografía del texto. Los primeros valores son genéricos (serif, sans-serif, etc.), es decir, los navegadores las comprenden y utilizan las fuentes que el usuario tenga en su sistema.<br/>
También se pueden definir con tipografías normales. Si el nombre de una fuente tiene espacios se utilizan comillas para que se entienda bien.

* **font-weight:** normal | bold | bolder | lighter | 100 | 200 | 300 | ... | 900 <br/>
*Ejemplos*: font-weight: bold; font-weight: 200; <br/>
Sirve para definir la anchura de los caracteres, o dicho de otra manera, para poner negrita con total libertad. <br/>
Normal y 400 son el mismo valor, así como bold y 700.

* **font-style:** normal | italic | oblique <br/>
*Ejemplos*: font-style: normal; font-style: italic; <br/>
Es el estilo de la fuente, que puede ser normal, itálica u oblicua. El estilo "oblique" es similar al "italic".

* **text-decoration:** none | underline | overline | line-through <br/>
*Ejemplos*: text-decoration: none; text-decoration: underline; <br/>
Establece la decoración de un texto, si está subrayado, sobre-rayado o tachado.

* **text-transform:** capitalize | uppercase | lowercase | none <br/>
*Ejemplos*: text-transform: none; text-transform: capitalize; <br/>
Nos permite transformar el texto, para que tenga la primera letra en mayúsculas de todas las palabras, o todo en mayúsculas o minúsculas.




### Ejemplos

Por ejemplo, para definir un párrafo en negrita, cursiva y además cambiar el color podemos definir estos estilos _inline_ en el atributo `style` del propio párrafo: 

```html
<p style="font-weight:bold; font-style:italic; color:red">
    Texto en negrita, cursiva y en color rojo.
</p>
```

Si quisieramos cambiar solamente el estilo de una o varias palabras dentro de un párrafo podemos utilizar la etiqueta `<span>` y asignarle dichos estilos en su atributo `style`: 

```html
<p>
    Este párrafo contiene una 
    <span style="font-weight:bold">sección en negrita</span>.
</p>
```

La definición de estilos dentro de la etiqueta `style` se suele hacer cuando dicho estilo solo se va a aplicar de forma puntual. Pero si por el contrario queremos definir un estilo que lo vamos a aplicar varias veces en un sitio Web lo más aconsejable es declarar una clase en una hoja de estilos externa o interna. Por ejemplo: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
    <title>Ejemplo</title>
    <meta charset="utf-8"/>
    <style type="text/css">
        h1 {
            color: blue;
        }
        p {
            color: black;
            font-size: 12pt;
        }
        .parrafo-aviso {
            font-weight:bold; 
            font-style:italic; 
            color:red;
        }
        .nota {
            text-align: right;
            font-size: 10pt;
            color: gray;
        }
    </style>
</head>
<body>
    <h1>Artículo 1</h1>
    <p>
        Párrafo normal al que se le aplica el color negro y un tamaño de 12pt.
    </p>
    <p class="parrafo-aviso">
        Texto de aviso destacado en color rojo, cursiva y negrita.
    </p>
    <p class="nota">
        Nota alineada a la derecha, en color gris y con tamaño de letra 10pt.
    </p>
</body>
</html>
```




