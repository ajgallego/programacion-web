# Nuevos selectores de atributos

En primer lugar encontramos 3 nuevos selectores de atributos:

* **elemento[atributo^="valor"]**: Selecciona los elementos con ese atributo y que su valor comienza por la cadena de texto indicada en "valor".
* **elemento[atributo$="valor"]**: Selecciona los elementos con ese atributo y que su valor termina por la cadena de texto indicada en "valor".
* **elemento[atributo*="valor"]**: Selecciona los elementos con ese atributo y que su valor contiene la cadena de texto indicada en "valor".

Por ejemplo:

```css
// Selecciona todos los enlaces que apunten a una dirección de correo:
a[href^="mailto:"]{...}

// Selecciona todos los enlaces que apuntan a páginas .php
a[href$=".php"]{...}

// Selecciona todos los enlaces que lleven a una página que contenga la palabra ejemplo:
a[href*="ejemplo"]{...}
```

También incorpora nuevas formas de seleccionar etiquetas adyacentes:

* **h1 + h2{...}**: Etiquetas inmediatamente adyacentes.
* **h1 ~ h2{...}**: Selector general de hermanos. Válido cuando `<h2>` se encuentre después de `<h1>`, pero puede haber otras etiquetas de por medio.

Ejemplo:

```html
<h1>Título</h1>
<h2>Subtítulo adyacente</h2>

<h1>Título</h1>
<p> párrafo de separación</p>
<h2>Subtítulo con selector general de hermanos</h2>
```

También podemos indicar atributos específicos de una etiqueta, con:

* **etiqueta1[atributo1="valor1"]**: seleccionaría todas las etiquetas "etiqueta1" que contengan un atributo llamado "atributo1" cuyo valor sea igual a "valor1". Por ejemplo, si queremos indicar un estilo para todas las etiquetas input que sean de tipo texto:


```css
input[type="text"] {
   background: #eee;
}
```


