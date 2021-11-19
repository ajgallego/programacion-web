# Operadores

Los operadores permiten manipular el valor de las variables, realizar operaciones matemáticas con sus valores y comparar diferentes variables. De esta forma, los operadores permiten a los programas realizar cálculos complejos y tomar decisiones lógicas en función de comparaciones y otros tipos de condiciones.

## Asignación
Este operador se utiliza para guardar un valor específico en una variable.

```javascript
var numero1 = 3;
var numero2 = 4;
var numero3 = numero1 + numero2;
```

## Incremento y decremento
Estos dos operadores solamente son válidos para las variables numéricas y se utilizan para incrementar (++) o decrementar (--) en una unidad el valor de una variable.

```javascript
var numero = 5;
++numero;   // Pre-incremento
numero++;   // Post-incremento
--numero;   // Pre-decremento
numero--;   // Post-decremento
```

Si el operador se utiliza como prefijo el decremento o incremento se realiza antes de la operación, si por el contrario se utiliza como sufijo se realizará después, por ejemplo:

```javascript
var numero1 = 5;
var resultado = 2 + numero1++;
// resultado = 7

var numero1 = 5;
var resultado = 2 + ++numero1;
// resultado = 8
```

## Operadores lógicos
El resultado de cualquier operación que utilice operadores lógicos siempre es un valor lógico o booleano.

* **Negación**: Se utiliza para obtener el valor contrario al valor de la variable: `var negacion = !valor_booleano;`

* **And**: El operador se indica mediante el símbolo `&&` y su resultado solamente es _true_ si los dos operandos son _true_: `var resultado = valor1 && valor2;`

* **Or**: El operador se indica mediante el símbolo || y su resultado es _true_ si alguno de los dos operandos es _true_: `var resultado = valor1 || valor2;`



## Operadores matemáticos
Los operadores definidos son: suma ( + ), resta ( - ), multiplicación ( * ), división ( / ) y módulo ( % ). A continuación se incluyen algunos ejemplos:

```javascript
var numero1 = 10;
var numero2 = 5;
var resultado = numero1 / numero2;  // resultado 2
resultado = 3 + numero1;   // resultado 13
resultado = numero2 – 4;   // resultado 1
resultado = numero1 * numero2; // resultado 10
resultado = numero1 % numero2; // resultado 0
```

Los operadores matemáticos también se pueden combinar con el operador de asignación para abreviar su notación:

```javascript
var numero1 = 5;
numero1 += 3; // numero1 = numero1 + 3 = 8
numero1 -= 1; // numero1 = numero1 - 1 = 4
numero1 *= 2; // numero1 = numero1 * 2 = 10
numero1 /= 5; // numero1 = numero1 / 5 = 1
numero1 %= 4; // numero1 = numero1 % 4 = 1
```

## Operadores relacionales o de comparación
Los operadores relacionales definidos por JavaScript son idénticos a los que definen las matemáticas: mayor que ( > ), menor que ( < ), mayor o igual ( >= ), menor o igual ( <= ), igual que ( == ) y distinto de ( != ). El resultado de todos estos operadores siempre es un valor booleano:

```javascript
var numero1 = 3;
var numero2 = 5;
resultado = numero1 > numero2; // resultado = false
resultado = numero1 < numero2; // resultado = true

numero1 = 5;
numero2 = 5;
resultado = numero1 >= numero2; // resultado = true
resultado = numero1 <= numero2; // resultado = true
resultado = numero1 == numero2; // resultado = true
resultado = numero1 != numero2; // resultado = false
```

