# Funciones

Una función es un conjunto de instrucciones que se agrupan para realizar una tarea concreta y que se pueden reutilizar fácilmente. Las funciones en JavaScript se definen mediante la palabra reservada `function`, seguida del nombre de la función. Su definición formal es la siguiente:

```javascript
function nombre_funcion() {
    ...
}
```

El nombre de la función se utiliza para llamar a esa función cuando sea necesario. A continuación se incluye un ejemplo de función y su llamada:

```javascript
<script>
function calculaSuma() {
    var valor1 = 3;
    var valor2 = 7;
    var resultado = valor1 + valor2;
    alert( "El resultado es " + resultado );
}
calculaSuma();  // llamada a la función "calculaSuma"
</script>
```

Igual que en otros lenguajes, a las funciones se le pueden pasar valores o _argumentos_ de entrada y pueden devolver un valor como resultado:

```javascript
function calculaSuma(valor1, valor2) {
    var resultado = valor1 + valor2;
    return resultado;
}
var resultado = calculaSuma(10, 4);  // llamada a la función "calculaSuma"
alert( resultado );
```

Es importante saber que:
* Se puede utilizar un número ilimitado de argumentos.
* El número de argumentos que se pasa a una función debería ser el mismo que el número de argumentos que ha indicado la función. No obstante, JavaScript no muestra ningún error si se pasan más o menos argumentos de los necesarios. En caso de que un argumento no esté definido tendrá el valor "undefined".



## Ámbito de las variables

Con respecto al ámbito de las variables tenemos que tener en cuenta las siguientes consideraciones:

* Si una variable se define con `var` dentro de una función el ámbito de dicha variable será local.
* Si una variable se define fuera de una función su ámbito será global, y por lo tanto serán accesibles desde dentro de las funciones.
* Si una variable se define dentro de una función pero sin usar la palabra reservada `var` el ámbito de dicha variable será global.

Ejemplos:

```javascript
var global1 = "Variable Global 1";

function mostrarMensaje() {
    var local1 = "Variable local 1";
    global2 = "Variable Global 2";
    console.log( global1 );  // mostrará "Variable Global 1"
}
mostrarMensaje();
console.log(local1);  // error, no existe la variable "local1"
console.log(global2); // mostrará "Variable Global 2"
```

