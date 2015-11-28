# Detectar funcionalidades de HTML5

_Modernizr_ es una librería de JavaScript con licencia MIT de código abierto que detecta si son compatibles elementos de HTML5 y CSS3. Podemos descargar la librería desde "<a href="http://www.modernizr.com/">http://www.modernizr.com/</a>". Para utilizarla solo hay que incluir en el `<head>` de tu página de la forma:


```html
<head>
   <script src="modernizr.min.js"></script>
</head>
```

_Modernizr_ se ejecuta automáticamente, no es necesario llamar a ninguna función. Cuando se ejecuta, se crea una objeto global llamado _Modernizr_, que contiene un _set_ de propiedades _Boleanas_ para cada elemento que detecta. Por ejemplo si su navegador soporta elementos _canvas_, la propiedad de la librería "_Modernizr.canvas_" será “_true_”. Si tu navegador no soporta los elementos _canvas_, la propiedad será “_false_”, de la forma:


```javascript
if (Modernizr.canvas) {
   // sí que hay soporte
} else {
   // no hay soporte para canvas
}
```

Para comprobar elementos de un formulario también podemos crearnos dos simples funciones que validan el soporte para diferentes tipos de inputs y atributos:



## Comprobar si un *input* es soportado

Con la siguiente función podemos comprobar si un navegador soporta o no los nuevos tipos de inputs:

```javascript
function inputSupports(tipo) {
   var input = document.createElement(’input’);
   input.setAttribute(’type’, tipo);
   if (input.type == ’text’) {
      return false;
   } else {
      return true;
   }
}
```

Por lo que podemos usarlo de la siguiente forma:

```javascript
if (!inputSupports(’range’)) {
   // Input tipo range no soportado
}
```



## Comprobar si un atributo es soportado

Para comprobar si hay soporte para un atributo

```javascript
function attrSupports(el, attr) {
   var telement = document.createElement(el);
   if (attr in telement) {
      return true;
   } else {
      return false;
   }
}
```


Por lo que podemos usarlo para comprobar, por ejemplo, los atributos autofocus, placeholder o required:

```javascript
if (!attrSupports(’input’, ’autofocus’)) {
   document.getElementById(’search_string’).focus();
}
if (!attrSupports(’input’, ’placeholder’)) {
   // Atributo placeholder no soportado
}
if (!attrSupports(‘input’, ‘required’)) {
   // Atributo required no soportado
}
```

