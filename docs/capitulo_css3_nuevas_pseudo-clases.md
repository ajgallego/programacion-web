# Nuevas pseudo-clases

Una pseudo-clase es un estado o uso predefinido de un elemento al que se le puede aplicar un estilo independientemente del estilo aplicado al de su estado por defecto. En CSS3 se han añadido muchas nuevas pseudo-clases para facilitar a los programadores el uso de algunos estilos avanzados en el diseño de páginas Web. Las nuevas pseudo-clases son:

* **:nth-child(n)** - Fija el aspecto de una ocurrencia específica del elemento nodo hijo especificado. Por ejemplo, el tercer elemento nodo hijo de una lista sería "li:nth-child(3)". Además se pueden usar pequeñas expresiones como parámetro para por ejemplo seleccionar todos los elementos impares: "nth-child(2n+1)" los pares "nth-child(2n)", etc. Los elementos impares y pares también se pueden seleccionar usando "nth-child(odd)" y "nth-child(even)"

* **:nth-last-child(n)** - igual que ":nth-child(n)"** **pero empezando a contar desde el final.

* **:nth-of-type(n)** - Fija la apariencia de una ocurrencia específica del elemento con el tipo de selector especificado en un elemento padre. Por ejemplo la segunda lista no ordenada sería ul:nth-of-type(2). También permite los mismos parámetros que ":nth-child(#)".

* **:nth-last-of-type(n)** - igual que ":nth-of-type(n)" pero empezando a contar desde el final.

* **:first-child** - Fija el aspecto del primer elemento de un tipo de selector solo si es el primer nodo hijo de su elemento padre, por ejemplo la primera etiqueta `<li>` de una lista `<ol>`.

* **:last-child** - Ultimo elemento de una lista de elementos de un tipo dado.

* **:first-of-type** - Selecciona el primer elemento de un tipo concreto dentro de la lista de hijos.

* **:last-of-type** - Selecciona el último elemento de un tipo.

* **:only-child** - Selecciona el elemento si es el único elemento hijo.

* **:only-of-type** - Selecciona el elemento si es el único elemento hijo de ese tipo.

* **:empty** - Selecciona los elementos que no tienen hijos (incluyendo nodos de texto).

* **:enabled** - Selecciona los elementos de la interfaz que tengan el estado "enable".

* **:disabled** - Selecciona los elementos de la interfaz que tengan un estado "disabled".

* **:not(s)** - Selecciona los elementos que no coincidan con el selector especificado.

* **:lang(language)** - nos permite especificar estilos que dependen del idioma especificado por la propiedad language (en, sp, etc.)


Ejemplos de uso:

```css
tr:nth-child(even) {
   background: silver;
}
tr:nth-child(odd) {
   background: white;
}
p:lang(en) {
   color: gray;
   font-style: italic;
}
```


## Pseudo-clases para formularios

Además también se han añadido nuevas pseudo-clases que podemos usar en los formularios para aplicar un formato según el estado de un campo. Estas propiedades van en concordancia con los nuevos campos introducidos en HTML5 (ver la sección de formularios de HTML5). estas son:

* **:valid** - campo válido (dependerá del tipo de campo).
* **:invalid** - campo inválido (dependerá del tipo de campo).
* **:required** - campo requerido (marcado con el atributo "required").
* **:optional** - campo opcional (campo no marcado con el atributo "required").
* **:checked** - elemento marcado (o checked, válido para radio button o checkbox).
* **:in-range** - valor dentro del rango indicado (para campos numéricos o de rango).
* **:out-of-range** - valor fuera de rango (para campos numéricos o de rango).
* **:read-only** - campo de solo lectura.
* **:read-write** - campo de lectura / escritura.


Algunos ejemplos de uso:

```html
<head>
   <style>
      #form1 input:valid { background:lightgreen; }
      #form1 input:invalid  { border-color:red; }
      #form1 specialInput input:valid { background:green; }
   </style>
</head>
<body>
   <form id="form1" name="form1" method="post" action="formaction.php">
      <p>Nombre:
       <input type="text" name="nombre" id="nombre" required/>
      <p/>
      <p>Usuario:
         <specialInput>
         <input type="text" name="usuario" id="usuario" required/>
         </specialInput>
      <p/>
   </form>
</body>
```

En este ejemplo cabe destacar la etiqueta "specialInput", que no es ninguna etiqueta existente, sino una nueva etiqueta que hemos creado para aplicar un formato especial.

Además podemos aplicar estas pseudo-clases en cadena y hacer cosas como:

```css
input:focus:required:invalid {
   background: pink url(ico_validation.png) 379px 3px no-repeat;
}
input:required:valid {
   background-color: #fff; background-position: 379px -61px;
}
```

Dado que Internet Explorer 6-8 no soporta la mayoría de pseudo-clases se han desarrollado algunas librerías de JavaScript que realizan las mismas funciones para estos navegadores, como "select[ivizr]" que podréis descargar de su página oficial "<a href="http://selectivizr.com/">http://selectivizr.com/</a>".


