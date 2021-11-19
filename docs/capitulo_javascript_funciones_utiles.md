# Funciones útiles de JavaScript

JavaScript incorpora una serie de herramientas y utilidades para el manejo de las variables.


## Funciones útiles para mostrar resultados

* La función "`alert(texto);`" nos permite mostrar un valor o cadena en una ventana emergente.
* La función "`console.log(texto);`" nos permite mostrar un valor o cadena en la consola del sistema. Esta función se suele utilizar para depuración.


## Funciones útiles para cadenas de texto

* Longitud de una cadena: se obtiene a partir de su propiedad "`.length`"
* Concatenación de cadenas: operador "`+`"
* Convertir en mayúsculas: `toUpperCase()`
* Convertir en minúsculas: `toLowerCase()`
* Obtener un carácter de la cadena: `charAt(posicion)`

Ejemplos:

```javascript
var mensaje = "Hola Mundo";
var numeroLetras = mensaje.length; // numeroLetras = 10
var concatenacion = "¡" + mensaje + "!";
var mayusculas = mensaje.toUpperCase();
var letra = mensaje.charAt(0); // letra = H
```


## Funciones útiles para arrays

* Longitud del array:  se obtiene a partir de su propiedad "`.length`"
* Añadir un elemento al final del array: "`push(valor)`"

Ejemplos:

```javascript
var array = [1, 2, 3];
var numeroElementos = array.length; // numeroElementos = 3
array.push(4);  // contenido del array = [1, 2, 3, 4]
```

## Funciones útiles para números

* Comprobar posibles valores numéricos no definidos: "`isNaN(valor)`"
* Comprobar si el valor es finito: "`isFinite(valor)`"
* Formatear / redondear números decimales: "`.toFixed(digitos)`"

Ejemplos:

```javascript
var valor1 = 3.14159265358979323846;
var valor2 = 0;

if( isNaN(valor1/valor2) || !isFinite(result) )
    alert("La división no está definida para los números indicados");

var valor3 = valor1.toFixed(2); // 3.14
```
