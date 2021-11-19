# Definición de estilos para etiquetas HTML

Si lo que queremos es dar formato o redefinir una etiqueta HTML existente, usaríamos la sintaxis:

```css
etiqueta {
   estilo CSS 1;
   estilo CSS 2;
   ...
}
```

En "etiqueta" pondríamos el nombre de la etiqueta (por ejemplo "`h1`", "`p`", etc. pero sin los signos `< >`) y los estilos que definirían esa etiqueta irían encerrados entre las llaves "`{...}`". Por ejemplo: 

```css
h1 {
   estilo CSS 1;
   estilo CSS 2;
   ...
}
```


## Comentarios

En las hojas de estilo también se pueden escribir comentarios usando los símbolos: `/* texto del comentario */`. Pero es importante usar esta notación y no ninguna otra, ya que es la única soportada. A continuación se incluye un ejemplo con comentarios: 

```css
/* Definimos el estilo de la cabecera principal */
h1 {
   estilo CSS 1; /* Cambiamos el estilo de su... */
   
   /* También cambiamos este otro estilo porque... */
   estilo CSS 2;
}
```



## Definición de varios estilos a la vez

También podemos redefinir varias etiquetas a la vez que compartirán los mismos estilos, separándolas por comas, de la forma:

```css
etiqueta1, etiqueta2, etiqueta3 {
   /* estilos CSS */
}
```

> En esta sección y la siguiente nos centraremos las cabeceras de los estilos y dejaremos los estilos CSS que podemos utilizar para la sección "estilos CSS básicos" y siguientes. Por este motivo escribiremos `/* estilos CSS */` en el lugar donde irán los estilos que definirá la etiqueta. 


Imaginad por ejemplo que queréis cambiar el color de todas las cabeceras, lo podéis hacer a la vez escribiendo: 

```css
h1, h2, h3, h4, h5, h6 {
   /* estilos CSS */
}
```


## Estilos anidados

Otra opción interesante es definir el estilo de etiquetas "dentro" de otras etiquetas. Para esto tenemos que escribir primero la etiqueta contendora, seguida de un espacio y por último la etiqueta a definir. En este caso el estilo CSS solo se aplicará cuando la _etiqueta definida_ se encuentre dentro de la _etiqueta contenedora_: 

```css
contenedor etiqueta {
   /* estilos CSS */
}
```

Por ejemplo, una etiqueta `<span>` dentro de una sección `<p>`:

```css
p span {
   /* estilos CSS */
}
```

Este estilo solo se aplicaría cuando se encuentre la etiqueta `<span>` dentro de una sección `<p>` de la forma: 

```html
<p> 
    Párrafo de ejemplo donde 
    <span>el estilo solo se aplicará sobre este texto</span> 
    y no sobre el resto del texto. 
</p>
```

Esta opción es muy útil pues nos permitirá definir diferentes estilos para la misma etiqueta dependiendo de donde se encuentre. 

