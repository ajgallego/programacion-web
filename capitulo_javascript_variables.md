# Variables

Las variables en JavaScript se crean mediante la palabra reservada `var`, que solamente es necesario utilizarla la primera vez (al declarar la variable), de la forma:

```javascript
var numero1 = 2;
var numero2 = 3;
var resultado = numero1 + numero2;
```

En javascript no es necesario declarar las variables con `var`, y en este caso lo que hace es crear una variable global a la que asigna el valor correspondiente. Por esta razón se recomienda declarar siempre las variables y llevar cuidado con esta característica.

El nombre de la variable solo puede estar formado por letas, números, el símbolo de dólar "$" y el guión bajo "_", además la primera letra del nombre no puede ser un número. A continuación se incluyen algunos ejemplos de nombres válidos e incorrectos:

```javascript
// Ejemplos correctos
var $numero1;
var _$letra;
var $$$otroNumero;
var $_a__$4;

// Ejemplos incorrectos
var 1numero;  // Empieza por un número
var numero;1_12.3;  // Contiene los carácteres ";" y "."
```


## Tipos de variables

Dado que todas las variables se crean de la misma forma (mediante la palabra reservada `var`), el tipo de la variable vendrá definido según el valor que se le asigne o almacene en ella. A continuación se detallan los diferentes tipos de variables posibles:


### Variables numéricas

Si a una variable se le asigna un entero o un valor decimal dicha variable se convertirá a tipo numérico, por ejemplo:

```javascript
var num1 = 16;
var num2 = 3.1415;
```

### Variables tipo cadenas de texto

Se utilizan para almacenar caracteres, palabras y/o frases de texto. Para asignar el valor a la variable, se encierra el valor entre comillas dobles o simples, para delimitar su comienzo y su final, por ejemplo:

```javascript
var mensaje = "Bienvenido a nuestro sitio web";
var nombreProducto = 'Producto ABC';
var letraSeleccionada = 'c';
var texto1_1 = "Una frase con 'comillas simples' dentro";
var texto1_2 = 'Una frase con \'comillas simples\' dentro';
var texto2_1 = 'Una frase con "comillas dobles" dentro';
var texto2_2 = "Una frase con \"comillas dobles\" dentro";
```

### Booleanos

Una variable de tipo boolean almacena un tipo especial de valor que solamente puede tomar dos valores: true (verdadero) o false (falso). Por ejemplo:

```javascript
var clienteRegistrado = false;
var ivaIncluido = true;
```



### Arrays

Para definir un array, se utilizan los caracteres `[` y `]` para delimitar su comienzo y su final y se utiliza el carácter `,` (coma) para separar sus elementos:

```javascript
var nombre_array = [valor1, valor2, ..., valorN];
```

Un nuevo array se puede declarar asignado valores iniciales (como en el ejemplo anterior), o vacío haciendo `var array1 = new Array();` o también `var array2 = [];` y después asignarle valores:

```javascript
var array1 = new Array();
array1[0] = "hola";
array1[1] = "mundo";

var saludo = array1[0];  // Obtener el valor de un elemento del array
```

Las posiciones o índices del array empiezan en 0 y terminan en el tamaño del array menos uno.


### Tipo de una variable

En JavaScript se puede comprobar el tipo de una variable mediante el operador `typeof`, por ejemplo:

```javascript
typeof "John"                // string
typeof 3.14                  // number
typeof false                 // boolean
typeof [1,2,3,4]             // object
```

JavaScript define los siguientes tipos primitivos de variables: _undefined, null, boolean, number, string_ y _object_. Los dos primeros (equivalentes) se utilizan para identificar cuando se accede a una variable que está sin definir. Los tipos _boolean, number_ y _string_ ya los hemos visto en las secciones anteriores, pero hay que destacar que el tipo _object_ se utiliza para definir tanto a los arrays como a los objectos (los cuales no se tratarán en este manual de iniciación).

