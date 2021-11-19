# Estructuras de control de flujo
Las estructuras de control permiten modificar el flujo de ejecución de las instrucciones de un programa.


## Estructura if
Se emplea para tomar decisiones en función de una condición. Su definición
formal es:

```javascript
if(condicion) {
    ...
}
```

Si la condición se cumple (es decir, si su valor es true ) se ejecutan todas las instrucciones que se encuentran dentro de `{...}`. Si la condición no se cumple (es decir, si su valor es false ) no se ejecuta ninguna instrucción contenida en `{...}` y el programa continúa ejecutando el resto de instrucciones del script.

La condición se evaluará de forma booleana y por lo tanto podemos utilizar cualquiera de los operadores que hemos visto para ello: !, &&, ||, >, <, ==, etc.

Esta estructura permite añadir una sección `else` que se ejecutará en caso de que no se cumpla la condición anterior e incluso concatenar varias sentencias `if` para realizar varias comprobaciones. A continuación se incluyen algunos ejemplos:

```javascript
var nombre = "";
if(nombre == "") {
    alert("Aún no nos has dicho tu nombre");
}
else {
    alert("Hemos guardado tu nombre");
}

// If ... else if anidado
var valor = 3;
if( valor == 1 )
    alert( "La variable vale 1" );
else if( valor == 2 )
    alert( "La variable vale 2" );
else if( valor == 3 )
    alert( "La variable vale 3" );
else
    alert( "La variable tiene otro valor" );
```


## Estructura switch
La estructura `switch` se utiliza para agilizar la toma de decisiones múltiples, trabaja de la misma manera que lo harían sucesivos `if`, `if else` anidados en el que según el valor de una variable entraría en uno de los casos definidos o en el caso por defecto:

```javascript
switch (variable) {     // La variable puede ser cualquier tipo de dato
    case "ok":
        // si variable == "ok"
        break;
    case 1:
        // si variable == "1"
        break;
    default:
        // Si no es igual a ninguno de los casos anteriores
        break;
}
´´´

El ejemplo anterior sería igual a hacer:

```javascript
if( variable == "ok" ) {
    // si variable == "ok"
}
else if( variable == 1 ) {
    // si variable == "1"
}
else {
    // Si no es igual a ninguno de los casos anteriores
}
```



## Estructura for
Esta estructura permite realizar una serie de repeticiones (también llamado bucle) mientras se cumpla una condición:

```javascript
for(inicializacion; condicion; actualizacion) {
    ...
}
```

Donde:
* La "inicialización" es la zona en la que se establece los valores iniciales de las variables que controlan la repetición.
* La "condición" es el único elemento que decide si continua o se detiene la repetición.
* La "actualización" es el nuevo valor que se asigna después de cada repetición a las variables que controlan la repetición.

Ejemplo de uso con un array:

```javascript
var dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"];
for(var i=0; i<7; i++) {
    alert(dias[i]);
}
```

## Estructura while
Es similar a `for`, repetirá el contenido del bucle mientras se cumpla la condición inicial:

```javascript
while (condicion) {
    ...
}
```

## Estructura do...while
Esta estructura es similar al bucle tipo `while` pero evalua la condición al final del bucle, con lo que se asegura que al menos se ejecutará una iteración:

```javascript
do {
    ...
} while (condicion);
```


## Estructura for...in
Este tipo de bucle, derivado de la estructura tipo `for`, permite iterar entre los elementos de un array o de un objeto (no tratados en esta introducción) de una forma muy sencilla:

```javascript
var dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"];

for(i in dias) {
    alert(dias[i]);
}
```
