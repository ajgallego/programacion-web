# Capas

Normalmente la posición de los elementos de una página es **relativa**, es decir, depende de los demás elementos de la página. Por ejemplo, un párrafo estará más abajo si antes de él hay más párrafos o elementos. Debido a esto, normalmente cuando se quería colocar elementos en un sitio concreto, se recurría al uso de tablas (invisibles, solo para estructurar).

Con CSS podemos colocar los elementos en posición **absoluta**, es decir, indicando el tamaño y coordenadas exactas en las que queremos que se coloque. Para organizar la disposición en una Web con CSS se suele usar el elemento `<div>`. Además se le suele dar un identificador único a cada uno, mediante el cual, desde la hoja de estilo, podemos configurar su disposición. También podemos colocar estos elementos con posición relativa a otro elemento que lo contenga, por ejemplo, un `<div>` dentro de otro.

Es común en el diseño Web crear contenedores `<div>` generales en una posición absoluta o centrados en la página, con un tamaño definido, los cuales se utilizarán para contener y disponer el resto de elementos de nuestra Web. Estos otros elementos se pueden alinear de forma sencilla con una alineación "relativa" a sus contenedores. Por ejemplo un contenedor para la cabecera que contenga un par de contenedores para la disposición de logotipo y el texto de cabecera.


## Distribución

Para indicar el tipo de distribución o disposición de un elemento lo hacemos mediante el atributo "**position: valor**". El cual puede tomar los valores:

* _absolute_: La posición del elemento no depende de ninguna otra etiqueta. Esta posición se calcula desde la esquina superior izquierda de la página.
* _fixed_: Al igual que el anterior la posición es absoluta, pero el elemento se queda fijo en el sitio al hacer "scroll".
* _relative_: Posición relativa a su elemento contenedor. Es la propiedad predeterminada.
* _static_: Al igual que el anterior la posición es relativa, pero no podemos redimensionar (por ejemplo) el objeto.


## Posición

Para indicar la posición concreta de una capa utilizamos los atributos: _top_, _bottom_, _left_ y _right_, de la forma:

```css
top: <posición>;
left: <posición>;
```

Normalmente sólo se utilizan un par de ellos, como _top_ y _left_, o _botton_ y _right_. La posición se especifica mediante unidades de CSS, como por ejemplo en "px", aunque también admite porcentajes.

Un ejemplo de la definición de una capa sería:


```css
#micapa {
   position: absolute;
   top: 200px;
   left: 150px;
   width: 175px;
   height: 175px;
   border: solid 1px blue;
   text-align: center;
   color: gray;
}
```


En nuestro documento HTML tendremos un elemento definido de la forma: `<div id="micapa"> ... </div>`, dentro del cual colocaremos texto u otros elementos.


> La posición absoluta la podemos definir respecto a la ventana del navegador o de forma relativa a un elemento contenedor. En este segundo caso tenemos que indicar que la posición del elemento contenedor es relativa (o de otra forma no funcionará).


## Orden

A veces tenemos varias capas, unas por encima de otras, y queremos especificar un orden, para poder controlar las ocultaciones entre capas. Para esto usamos el z-index, de la forma:

```css
z-index: <índice>;
```

Las capas con un índice de Z-index mayor aparecerán por encima de las capas con un z-index menor.

