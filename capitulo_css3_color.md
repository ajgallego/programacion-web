# Color

En CSS3 se han incorporado nuevas formas para definir los colores:

* **rgba( red, green, blue, opacity );** - Color RGBA. El valor de opacidad debe de estar entre 0 y 1, siendo 0 totalmente transparente. Por ejemplo, podemos usarlo de la forma:

```css
background-color: rgba(255, 115, 135, 0.5);
color: rgba(255, 115, 135, 0.5);
```

* **hsl( hue, saturation, lightness );** - Modelo de color HSL.
* **hsla(hue, saturation, lightness, alpha);** - Modelo de color HSLA.
* **cmyk(cyan, magenta, yellow, black);** - Modelo de color CMYK.
* **opacity: 0.5;** - También podemos indicar el valor de transparencia u opacidad por separado, debiendo de estar este valor entre 0 y 1, siendo 0 totalmente transparente y 1 totalmente opaco. Para dar también soporte a Internet Explorer usaremos: "_filter:alpha(opacity=50);_".

