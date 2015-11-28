# Símbolos HTML

Los caracteres especiales como signo de puntuación, letras con tilde o diéresis, o símbolos del lenguaje; se deben convertir en entidades HTML para que se muestren correctamente en un navegador. La siguiente es una lista de caracteres españoles junto con algunos símbolos especiales y su correspondiente entidad HTML:

| Caracter          | Código     || Caracter       | Código     |
| ----------------- | ---------- | -- | ---------- | ---------- |
| á                 | `&aacute;` | | Á             | `&Aacute;` |
| é                 | `&eacute;` | | É             | `&Eacute;` |
| í                 | `&iacute;` | | Í             | `&Iacute;` |
| ó                 | `&oacute;` | | Ó             | `&Oacute;` |
| ú                 | `&uacute;` | | Ú             | `&Uacute;` |
| ü                 | `&uuml;  ` | | Ü             | `&Uuml;  ` |
| ñ                 | `&ntilde;` | | Ñ             | `&Ntilde;` |
| espacio en blanco | `&nbsp;`   | | €             | `&euro;`   |
| `<` (Menor que)   | `&lt;`     ||`>` (Mayor que) | `&gt;`     |
| &                 | `&amp;`    | | º (grados)    | `&deg;`    |


Recordad que para escribir letras acentuadas u otros símbolos y que el navegador los muestre correctamente símplemente tenemos que añadir la cabecera `meta` con la codificación: 

```html
<meta charset="utf-8"/>
```

Sin embargo hay determinados caracteres que si queremos escribirlos nos veremos obligados a escribir el código del símbolo. Por ejemplo, HTML solamente muestra o renderiza un espacio en el navegador aunque nosotros escribamos muchos espacios. Si por alguna razón queremos dar varios espacios tendremos que escibir el símbolo "`&nbsp;`". O si por ejemplo queremos poner los símbolos de mayor (`>`) o menor (`<`) y no correr el riesgo de que se confunda con el inicio o cierre de una etiqueta HTML, también tendremos que escribir el código correspondiente.

Para obtener una lista mucho más completa de símbolos podemos buscar en Google: "_HTML symbols_" o visitar la siguiente dirección http://www.ascii.cl/htmlcodes.htm.
