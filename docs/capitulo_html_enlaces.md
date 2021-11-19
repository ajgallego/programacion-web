# Enlaces

Los enlaces permiten vincular partes del documento con otros documentos o con otras partes del mismo documento. Por ejemplo, que al pulsar con el ratón sobre un texto o sobre una imagen se nos redirija a una nueva Web con un contenido diferente.

Para crear un enlace se utiliza la etiqueta `<a href=""></a>` cuyo atributo href establece la dirección URL a la que apunta el enlace. Por ejemplo, un enlace a la Wikipedia sería de la forma:

```html
<a href="http://es.wikipedia.org">Wikipedia</a>
```

Para crear un enlace a una sección de nuestra propia web únicamente nos hará falta escribir el nombre del fichero HTML, por ejemplo: 

```html
<a href="pagina2.html">Pulsa aquí</a>
```


## Ejemplo 

En este ejemplo vamos a crear un enlace desde la página principal de nuestro sitio web (almacenada en el fichero `index.html`) a una página secundaria con un artículo (que estaría en el fichero `articulo1.html`). Además, en la página secundaria añadiremos también un enlace para volver a la página principal. 

El contenido de la página principal (fichero `index.html`) sería el siguiente: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
    <title>Ejemplo</title>
    <meta charset="utf-8">
</head>
<body>
   <h1>Web de ejemplo</h1>
   <p>Pulsa en <a href="articulo1.html">este enlace</a> 
      para consultar nuestro primer artículo.</p>
</body>
</html>
```

El contenido de la página secundaria (fichero `articulo1.html`) sería el siguiente: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
    <title>Ejemplo</title>
    <meta charset="utf-8">
</head>
<body>
   <h1>Artículo 1</h1>
   <p>Texto de ejemplo del artículo 1.</p>
   <p>Pulsa en <a href="index.html">este enlace</a> para volver a la página principal.</p>
</body>
</html>
```



## Enlaces sobre otros elementos

También se pueden crear enlaces sobre otros elementos, como por ejemplo imágenes. Para esto simplemente tenemos que escribir la/s etiqueta/s de dicho elemento dentro del enlace:

```html
<a href="dirección_URL"><img src="imagen.jpg"/></a>
```


## Abrir una nueva ventana (o pestaña del navegador)

La etiqueta de enlace `<a>` también permite el atributo `target="_blank"`, mediante el cual indicamos que el enlace se tiene que abrir en una nueva ventana o en una pestaña nueva del navegador. Esta opción se suele utilizar a menudo para los enlaces externos para que no se cierre la web actual. 

Por ejemplo, para añadir un enlace a una web externa que se abra en otra ventana para que el usuario consulte más información escribiríamos el siguiente código: 

```html
<a href="https://es.wikipedia.org/wiki/Polinomio" target="_blank">
    Para más información pulsa aquí
</a>
```


## Dirección base

La dirección principal de la web no es necesario escribirla ya que se añadirá automáticamente. Por ejemplo, si nuestra web es "http://www.webejemplo.es" y en el enlace escribímos únicamente `<a href="pagina2.html">Pulsa aquí</a>`, al pulsar nos redirigirá a la web "http://www.webejemplo.es/pagina2.html". 

Hay que tener **cuidado** cuando colocamos las páginas dentro de carpetas. Por ejemplo, si creamos una carpeta para meter todas las páginas con artículos y escribimos un enlace de la forma: `<a href="articulos/articulo1.html">Ir al artículo 1</a>`, esto nos redirigirá a la dirección "http://www.webejemplo.es/articulos/articulo1.html". El **problema** está en los enlaces que coloquemos dentro de una página que esté en una subcarpeta. Por ejemplo, si en la página "articulo1.html" (que está en la carpeta "articulos") añadimos un enlace para volver al índice de la forma: `<a href="index.html">Volver</a>`, este enlace en realidad nos llevaría a la dirección "http://www.webejemplo.es/**articulos/index.html**". Es decir, buscaría la página "index.html" dentro de la carpeta actual.

Para solucionar este problema y hacer referencia a la raíz de nuestro sitio web, se suele anteponer **siempre** la barra "/" a todas las direcciones. Por ejemplo, en el caso del enlace erróneo anterior tendríamos que escribir: `<a href="/index.html">Volver</a>`. Pero esta barra es recomendable escribirla siempre, en todas las direcciones, para evitar errores. 



