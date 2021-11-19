# Tablas

Las tablas se definen básicamente mediante tres etiquetas:

* `<table></table>`: define una tabla.
* `<tr></tr>`: fila de una tabla, debe de estar dentro de las etiquetas de una tabla.
* `<td></td>`: celda de una tabla, debe estar dentro de una fila.

Ejemplo de una tabla:

```html
<table>
   <tr>
      <td>Fila 1 izquierda</td>
      <td>Fila 1 derecha</td>
   </tr>
   <tr>
      <td>Fila 2 izquierda</td>
      <td>Fila 2 derecha</td>
   </tr>
</table>
```

Con lo que obtendríamos un resultado similar al siguiente:

<table>
   <tr>
      <td>Fila 1 izquierda</td>
      <td>Fila 1 derecha</td>
   </tr>
   <tr>
      <td>Fila 2 izquierda</td>
      <td>Fila 2 derecha</td>
   </tr>
</table>

Además también podemos utilizar la etiqueta `<th>` en lugar de `<td>` para indicar una celda de "cabecera", de esta forma el contenido será resaltado en negrita y en un tamaño ligeramente superior al normal. Por ejemplo, para crear una tabla con dos elementos de cabecera y dos celdas normales:

```html
<table>
   <tr>
      <th>Cabecera 1</th>
      <th>Cabecera 2</th>
   </tr>
   <tr>
      <td>Celda 1</td>
      <td>Celda 2</td>
   </tr>
</table>
```

En la etiqueta de apertura `<table>` podemos utilizar los siguientes atributos:

* `border="num"`: Ancho del borde de la tabla en puntos. Si indicamos border="0" tendremos una tabla cuyas divisiones no serán visibles, esta propiedad se suele utilizar para distribuir los elementos en una página Web.

* `cellspacing="num"`: Espacio en puntos que separa las celdas que están dentro de la tabla.

* `cellpadding="num"`: Espacio en puntos que separa el borde de cada celda y el contenido de esta.

* `width="num"`: Indica la anchura de la tabla en puntos o en porcentaje en función del ancho de la ventana. Si no se indica este parámetro, el ancho dependerá de los contenidos de las celdas.

* `height="num"`: Indica la altura de la tabla en puntos o en porcentaje en función del alto de la ventana. Si no se indica este parámetro, la altura dependerá de los contenidos de las celdas.
Este atributo también se puede utilizar en las etiquetas `<tr>` para indicar la altura de cada fila de forma individual.


En las etiquetas de apertura de celda (`<td>` o `<th>`) podemos utilizar los siguientes atributos:

* `align="pos"`: Indica como se debe alinear el contenido de la celda, a la izquierda (left), a la derecha (right), centrado (center) o justificado (justify).

* `valign="pos"`: Indica la alineación vertical del contenido de la celda, en la parte superior (top), en la inferior (bottom), o en el centro (middle).

* `rowspan="num"`: Indica el número de filas que ocupará la celda. Por defecto ocupa una sola fila. Este atributo se utiliza para crear celdas "multifila", es decir, una celda que por ejemplo ocupe 3 filas. Tendremos que tener en cuenta que esa celda no se deberá de definir en las siguientes 2 filas (para esas filas se definirá una celda menos).

* `colspan="num"`: Indica el número de columnas que ocupará la celda. Por defecto ocupa una sola columna. Este atributo se utiliza para crear celdas "multicolumna", es decir, una celda que por ejemplo ocupe 3 columnas. Tendremos que tener en cuenta que en esa fila tendremos que definir 2 celdas menos.

* `width="num"`: Indica la anchura de la columna en puntos o en porcentaje en función del ancho de la ventana. Si no se indica este parámetro, el ancho dependerá del tamaño de los contenidos.


