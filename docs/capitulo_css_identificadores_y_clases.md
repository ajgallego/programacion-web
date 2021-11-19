# Identificadores y Clases

A veces tenemos varias etiquetas del mismo tipo pero queremos aplicar diferentes estilos según donde estén. Para esto usamos los identificadores y las clases.

La principal diferencia entre ellos es que los identificadores tienen que ser **únicos en todo el documento HTML** mientras que las clases pueden repetirse todas las veces que queramos. La otra diferencia es la forma de definirlos y de utilizarlos: En HTML para indicar el identificador de una etiqueta usaremos el atributo "`id`", mientras que para indicar la clase usaremos "`class`":

```html
<div id="capitulo2">
   <p>...</p>
   <p class="parrafogris">....</p>
   <p>...</p>
   <p class="parrafogris">....</p>
   <p>...</p>
   <p class="parrafogris">....</p>
</div>
```

En este ejemplo se asigna el identificador "capitulo2" a la etiqueta `<div>` inicial. Esta etiqueta sería una sección **única** en todo el documento sobre la cual podemos aplicar un estilo concreto. El estilo de la clase "parrafogris" se aplicaría sobre las etiquetas "`p`" indicadas, y como se puede ver si ha aplicado varias veces. 

Otra diferencia entre identificadores y clases es la forma de definir sus estilos CSS en la hoja de estilos. Para indicar un identificador escribiremos su nombre precedido por una almohadilla "`#`", y para referenciar una clase usaremos como prefijo el punto ".", por ejemplo: 

```css
#identificador {
    /* estilos CSS */
}
.clase {
    /* estilos CSS */
}
```

Por ejemplo, para indicar los estilos del ejemplo anterior, escribiríamos el siguiente código: 

```css
#capitulo2 {
    /* estilos CSS */
}
.parrafogris {
    /* estilos CSS */
}
```

> Es importante diferenciar cuando tenemos que usar la almohadilla "`#`" y el punto ".", los cuales solo los pondremos en la hoja de estilos y **no** en el código HTML. Esto es un error común y haría que los estilos no funcionasen. Es decir, si escribimos `<div id="#capitulo2">` (con "`#`") o escribimos `<p class=".parrafogris">` (con ".") sería un **error** y no funcionaría. 


> Los identificadores se suelen usar menos que las clases y solo para elementos específicos que se quieren diferenciar. Normalmente se aplican sobre etiquetas "neutras" como `<div>` o `<span>` para marcar partes de un documento y después indicar sus estilos (como por ejemplo identificar la cabecera, un logotipo, el menú principal, etc.).



## Definición de varios estilos a la vez

Igual que hemos visto antes, podemos definir estilos a la vez para varios identificadores y clases: 

```css
#capitulo1, #capitulo2, #capitulo3 {
    /* estilos CSS */
}
.parrafogris, .parraforojo, .parrafoverde {
    /* estilos CSS */
}
```

Podemos mezclar identificadores, con clases y con etiquetas sin problema: 


```css
#capitulo1, .parrafogris, h1 {
    /* estilos CSS */
}
```


## Anidación de estilos

Podemos aplicar estilos a identificadores y clases solo cuando cuando estén dentro de otros: 

```css
#capitulo1 #cabecera {
    /* estilo a aplicar a #cabecera solo cuando esté dentro de #capitulo1 */
}
.parrafogris .resaltado {
    /* estilo a aplicar a .resaltado solo cuando esté dentro de .parrafogris */
}
```

Igual que antes también podemos combinar identificadores, con clases y con etiquetas sin problema:

```css
#cabecera h1 {
    /* estilos a aplicar a h1 solo cuando esté dentro de la sección #cabecera */
}
.parrafogris span {
    /* estilos a aplicar a la etiqueta span solo cuando esté dentro de .parrafogris */
}
```

Si queremos podemos crear más niveles de profundidad, por ejemplo: 

```css
#cabecera p .resaltado {
    /* estilos a aplicar a ".resaltado" solo cuando esté dentro 
    de una etiqueta "p" que a su vez esté dentro de la sección #cabecera */
}
```



## Filtrar etiquetas con estilos

También podemos aplicar estilos filtrando por etiquetas que tenga una determinada clase, por ejemplo: 

```css
etiqueta1.clase1 {
   /* estilos CSS */
}
```

En este caso sólo se aplicaría el estilo a las etiquetas "etiqueta1" que se marque que son de la clase "clase1", por ejemplo: `<etiqueta1 class="clase1">...</etiqueta1>`. Si intentáramos aplicar esta clase a una etiqueta diferente no funcionaría.

Por ejemplo, el estilo: 

```css
h1.resaltado {
   /* estilos CSS */
}
```

Solo se aplicaría a las cabeceras `h1` que tengan aplicada la clase `.resaltado` de la forma: `<h1 class="resaltado">...</h1>`

