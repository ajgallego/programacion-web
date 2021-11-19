# DOM

El _Document Object Model_ o DOM ('Modelo de Objetos del Documento' o 'Modelo en Objetos para la Representación de Documentos') es esencialmente una interfaz que proporciona un conjunto estándar de objetos para representar documentos HTML y XML, aportando una interfaz estándar para acceder a ellos y manipularlos. A través del DOM se pueden acceder y modificar el contenido, estructura y estilo de los documentos HTML y XML, y es para lo que se diseñó principalmente.

DOM transforma todos los documentos XHTML en un conjunto de elementos llamados nodos, que están interconectados y que representan los contenidos de las páginas web y las relaciones entre ellos. Por su aspecto, la unión de todos los nodos se llama "árbol de nodos".

Por ejemplo, la siguiente página HTML:

```html
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
    <title>Página sencilla</title>
</head>
<body>
    <p>Esta página es <strong>muy sencilla</strong></p>
</body>
</html>
```

Se transformaría en el siguiente árbol de nodos:

![Ejemplo DOM](images/web_js/dom_example.jpg "Ejemplo DOM")


Una vez construido automáticamente el árbol completo de nodos DOM, ya es posible utilizar las funciones DOM para acceder de forma directa a cualquier nodo del árbol. Como acceder a un nodo del árbol es equivalente a acceder a "un trozo" de la página, por lo que es posible manipular de forma sencilla la página: acceder al valor de un elemento, establecer el valor de un elemento, mover un elemento de la página, crear y añadir nuevos elementos, etc.

DOM proporciona dos métodos alternativos para acceder a un nodo específico: acceso a través de sus nodos padre y acceso directo.

Las funciones que proporciona DOM para acceder a un nodo a través de sus nodos padre consisten en acceder al nodo raíz de la página y después a sus nodos hijos y a los nodos hijos de esos hijos y así sucesivamente hasta el último nodo de la rama terminada por el nodo buscado.

Sin embargo, cuando se quiere acceder a un nodo específico, es mucho más rápido acceder directamente a ese nodo y no llegar a él descendiendo a través de todos sus nodos padre.



## Acceso a nodos del árbol DOM

### getElementsByTagName()

Obtiene todos los elementos de la página HTML cuya etiqueta sea igual que el parámetro que se le pasa a la función, por ejemplo:

```javascript
var parrafos = document.getElementsByTagName("p");
```

El valor que se indica delante del nombre de la función (en este caso _document_, que sería la raíz del árbol DOM) es el nodo a partir del cual se realiza la búsqueda de los elementos. En este caso, como se quieren obtener
todos los párrafos de la página, se utiliza el valor _document_ como punto de partida de la búsqueda.

El valor que devuelve la función es un array con todos los nodos que cumplen la condición de que su etiqueta coincide con el parámetro proporcionado. El valor devuelto es un array de nodos del DOM, no un array de cadenas de texto o un array de objetos normales.

De este modo, se puede obtener el primer párrafo de la página de la siguiente manera:

```javascript
var primerParrafo = parrafos[0];
```

De la misma forma, se podrían recorrer todos los párrafos de la página con el siguiente código:

```javascript
for(var i=0; i<parrafos.length; i++) {
    var parrafo = parrafos[i];
}
```

La función `getElementsByTagName()` se puede aplicar de forma recursiva sobre cada uno de los nodos devueltos por la función. En el siguiente ejemplo, se obtienen todos los enlaces del primer párrafo de la página:

```javascript
var parrafos = document.getElementsByTagName("p");
var primerParrafo = parrafos[0];
var enlaces = primerParrafo.getElementsByTagName("a");
```


### getElementsByName()

Esta función es similar a la anterior, pero en este caso se buscan los
elementos cuyo atributo `name` sea igual al parámetro proporcionado. En el siguiente ejemplo, se obtiene directamente el único párrafo con el nombre indicado:

```javascript
var parrafoEspecial = document.getElementsByName("especial");
<p name="prueba">...</p>
<p name="especial">...</p>
<p>...</p>
```

Internet Explorer 6.0 no implementa de forma correcta esta función, ya que sólo la tiene en cuenta para los elementos de tipo `<input>` y `<img>`. Además, también tiene en consideración los elementos cuyo atributo id sea igual al parámetro de la función.


### getElementById()

Esta es la función más utilizada cuando se desarrollan aplicaciones web
dinámicas ya que permite acceder directamente a un nodo y poder leer o
modificar sus propiedades.

La función `getElementById()` devuelve el elemento HTML cuyo atributo `id` coincide con el parámetro indicado en la función. Como el atributo `id` debe ser único en toda la página, la función devuelve únicamente el nodo deseado.

```javascript
var cabecera = document.getElementById("cabecera");
<div id="cabecera">
<a href="/" id="logo">...</a>
</div>
```

Internet Explorer 6.0 también interpreta incorrectamente esta función, ya que devuelve también aquellos elementos cuyo atributo name coincida con el parámetro proporcionado a la función.


## Creación y eliminación de nodos

Con JavaScript también se pueden añadir y eliminar elementos dinámicamente del árbol DOM. Para esto se utilizan las funciones `createElement(etiqueta)`, `createTextNode(text)`, `appendChild(child)` y `removeChild(child)`.

Dado que su uso se queda fuera de los contenidos de este curso, si se desea obtener más información se puede consultar la web:

* http://www.w3schools.com/jsref/met_document_createelement.asp
* http://www.w3schools.com/jsref/met_document_createtextnode.asp
* http://www.w3schools.com/jsref/met_node_appendchild.asp
* http://www.w3schools.com/dom/met_element_removechild.asp


## Acceso a atributos de un nodo

Una vez que se ha accedido a un nodo, el siguiente paso natural consiste en acceder y/o modificar sus atributos y propiedades. Mediante DOM, es posible acceder de forma sencilla a todos los atributos y todas las propiedades CSS de cualquier elemento de la página.

Los atributos de los elementos de la página se transforman automáticamente en propiedades de los nodos. Para acceder a su valor, simplemente se indica el nombre del atributo detrás del nombre del nodo.

El siguiente ejemplo obtiene de forma directa la dirección a la que enlaza el enlace:

```javascript
// HTML
<a id="enlace" href="http://www.ua.es">Universidad de Alicante</a>
<img id="imagen" style="margin:0; border:0;" src="logo.png" />
<p id="parrafo" style="font-weight: bold;" class="destacado">Texto</p>

// JavaScript
var enlace = document.getElementById("enlace");
var imagen = document.getElementById("imagen");
var parrafo = document.getElementById("parrafo");

console.log(enlace.id);       // muestra "enlace"
console.log(enlace.href);     // muestra "http://www.ua.es"
console.log(enlace.innerHTML);// muestra "Universidad de Alicante"

console.log(imagen.id);       // muestra "imagen"
console.log(imagen.src);      // muestra "logo.png"
console.log(imagen.style.margin); // muestra "0px"
console.log(imagen.style.border); // muestra "0px none"

console.log(parrafo.id);               // muestra "parrafo"
console.log(parrafo.innerHTML);        // muestra "Texto"
console.log(parrafo.style.fontWeight); // muestra "bold"
console.log(parrafo.className);        // muestra "destacado"
```

Es importante destacar que si el nombre de una propiedad o estilo es compuesto, como "font-weight", que tiene un guión "-" en el medio, para acceder dicho guión se elimina y además se escribe en mayúsculas la primera letra se la siguiente palabra, por ejemplo:

* _font-weight_ se transforma en _fontWeight_
* _line-height_ se transforma en _lineHeight_
* _border-top-style_ se transforma en _borderTopStyle_
* _list-style-image_ se transforma en _listStyleImage_

También es importante destacar que como la palabra `class` está reservada por JavaScript, no es posible utilizarla para acceder al atributo `class` del elemento XHTML. En su lugar, DOM utiliza el nombre `className` para acceder.


