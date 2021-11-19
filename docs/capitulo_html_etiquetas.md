# Sintaxis del lenguaje

Las etiquetas HTML deben de ir encerradas entre corchetes angulares `<>`, y pueden ser de dos tipos:

* Se abren y se cierran, como por ejemplo: `<b>negrita</b>` o `<p>texto</p>`.

* Se abren y cierran en la misma etiqueta, como: `<br/>` o `<hr/>`.

En caso de que no cerremos una etiqueta que deba ser cerrada se producirá un error en la estructura del documento y probablemente también genere errores en la visualización.

Hay etiquetas que además pueden contener atributos, en este caso los atributos se deben de colocar en la etiqueta de inicio, de la forma:

```html
<etiqueta atributo1="valor1" atributo2="valor2">...</etiqueta>
```

O para las etiquetas de solo apertura:

```html
<etiqueta atributo1="valor1" atributo2="valor2"/>
```

Por ejemplo: 

```html
<img src="imagen.jpg" alt="Imagen de cabecera"/>
```