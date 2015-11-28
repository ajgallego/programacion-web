# Vídeo

La nueva especificación de HTML5 soporta la inclusión de vídeo empotrado en las páginas web de forma nativa. El elemento _video_ no especifica el formato del mismo sino que el uso de uno u otro vendrá impuesto por el fabricante del navegador:

| Códec      | IE>=9 | Firefox | Chrome | Safari | Opera |
| --         | --    | --      | --     | --     | --    |
| Ogg Theora | no    | sí      | sí     | no     | sí    |
| H.264      | sí    | no      | no     | sí     | no    |
| VP8        | no    | sí      | sí     | no     | sí    |

El elemento _video_ dispone de los atributos "_autoplay_", "_loop_" y "_preload_", para activar la auto-reproducción, para indicar que se reproduzca en bucle y para activar/desactivar la precarga del vídeo. Asimismo puedes utilizar los controles que te ofrece el navegador de forma nativa utilizando el atributo _controls_ o bien puedes ofrecer tus propios controles en JavaScript. Dado que el vídeo ocupa un espacio, también podremos definir sus dimensiones con los atributos "_width_" y "_height_". E incluso podemos indicar una imagen para que se muestre antes de la reproducción mediante el atributo "poster":


```html
<video src="archivo.mp4" controls width="360" height="240" poster="poster.jpg"> </video>
```

Con lo que obtendríamos un resultado similar a:

![](images/web_intro/html5_video.jpg)

Para dar soporte a todos los navegadores, podemos especificar diferentes archivos en diferentes formatos. Además podemos usar el mismo truco que usábamos con el elemento audio para seguir dando soporte al _plugin_ de Flash a través de la etiqueta _object_, e incluso incluir un link de descarga:


```html
<video controls width="360" height="240" poster="poster.jpg">
   <source src="archivo.ogv" type="video/ogg" />
   <source src="archivo.mp4" type="video/mp4" />
   <object type="application/x-shockwave-flash" width="360" height="240"
					data="player.swf?file=archivo.mp4">
      <param name="movie" value="player.swf?file=archivo.mp4" />
      <a href="archivo.mp4">Descarga la película</a>
   </object>
</video>
```

