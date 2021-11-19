# Transformaciones

La propiedad "**transform**" nos permite aplicar transformaciones 2D o 3D a un elemento. Por ejemplo nos permite rotar, escalar, mover, etc. el elemento indicado. Esta propiedad todavía no es soportada por todos los navegadores, por lo que tendremos que añadir los prefijos "-ms-", "webkit-", "-moz-" y "-o-" para dar un mayor soporte. Algunas de las funciones de transformación que podemos utilizar son:

* **none:** Indica que no se tiene que aplicar ninguna transformación.
* **translate(x,y): ** Define una traslación 2D.
* **translateX(x):** Traslación en la coordenada X.
* **translateY(y):** Traslación en la coordenada Y.
* **scale(x,y):** Define una transformación de escalado 2D, deberemos de indicar valores entre 0.1 y 2.
* **scaleX(x):** Escalado en la coordenada X, deberemos de indicar valores entre 0.1 y 2.
* **scaleY(y):** Escalado en la coordenada Y, deberemos de indicar valores entre 0.1 y 2.
* **rotate(angle):** Aplica una rotación, el ángulo debe ser indicado en grados (ejem: "30deg").
* **skew(x-angle,y-angle):** Define una transformación 2D de sesgo (o torsión), indicada en grados (deg).
* **skewX(angle):** Define una transformación de sesgo sobre la coordenada X (indicada en grados).
* **skewY(angle):** Define una transformación de sesgo sobre la coordenada Y (indicada en grados).

Además también podemos indicar varias transformaciones en una misma línea, de la forma:

```css
#myDIV {
   -moz-transform: scale(1.2) rotate(9deg) translate(5px, 2px) skew(5deg, 5deg);
   -webkit-transform: scale(1.2) rotate(9deg) translate(5px, 2px) skew(5deg, 5deg);
   -o-transform: scale(1.2) rotate(9deg) translate(5px, 2px) skew(5deg, 5deg);
   -ms-transform: scale(1.2) rotate(9deg) translate(5px, 2px) skew(5deg, 5deg);
   transform: scale(1.2) rotate(9deg) translate(5px, 2px) skew(5deg, 5deg);
}
```

Hay muchos más tipos de transformaciones, aunque algunas de ellos no son funcionales todavía (sobre todo las funciones 3D), para más información consulta: "<a href="http://www.w3schools.com/cssref/css3_pr_transform.asp">http://www.w3schools.com/cssref/css3_pr_transform.asp</a>".

