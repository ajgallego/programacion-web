# Audio

El nuevo elemento audio permite insertar archivos sonoros en diferentes formatos, incluyendo mp3 y ogg. Además provee de una interfaz de control sobre la reproducción del mismo con una API en JavaScript sin necesidad de plugins de ningún tipo (como Flash). Añadir un reproductor de audio en HTML5 es muy simple:

```html
<audio src="archivo.mp3" controls>
   <p>Tu navegador no soporta el elemento audio</p>
</audio>
```

En Firefox obtendríamos un resultado similar a:

![](images/web_intro/html5_sound.jpg)

El texto que se encuentra entre las etiquetas audio solo es tenido en cuenta por navegadores que no soporten la nueva etiqueta. El atributo "controls" indica al navegador que muestre los controles de reproducción. En caso de no activarlo no se visualizaría nada, pero podríamos controlar la reproducción mediante funciones JavaScript, de la forma:


```html
<audio id="player" src="archivo.mp3"></audio>
<button onclick="document.getElementById(’player’).play();">Reproducir</button>
<button onclick="document.getElementById(’player’).pause();">Pausa</button>
<button onclick="document.getElementById(’player’).volume += 0.1;">Subir Volumen</button>
<button onclick="document.getElementById(’player’).volume -= 0.1;">Bajar Volumen</button>
```

También podemos usar los atributos "autoplay" y "loop" para que se auto-reproduzca y para que se cree un bucle de reproducción infinito:

```html
<audio src="archivo.mp3" autoplay loop></audio>
```

El formato de audio a utilizar vendrá impuesto por el navegador usado y no por el estándar:


| Códec      | IE>=9 | Firefox | Chrome | Safari | Opera |
| --         | --    | --      | --     | --     | --    |
| Ogg Vorbis | no    | sí      | sí     | no     | sí    |
| WAV PCM    | no    | sí      | sí     | sí     | sí    |
| MP3        | sí    | no      | sí     | sí     | sí    |
| AAC        | sí    | no      | sí     | sí     | sí    |
| Speex      | no    | no      | sí     | no     | no    |


Como puede verse, combinando Vorbis y MP3 podremos ofrecer audio a todos los navegadores mayoritarios. Existe una forma de definir más de un archivo de audio para la etiqueta audio, en lugar de usar el atributo "src", utilizaremos la etiqueta "source" para poder definir múltiples archivos. Estas etiquetas se irán leyendo de arriba a abajo hasta que el navegador encuentre un formato soportado. De esta manera podremos complacer las necesidades de todos los usuarios sin discriminar a ningún navegador.


```html
<audio controls>
   <source src="archivo.ogg" type="audio/ogg" />
   <source src="archivo.mp3" type="audio/mpeg" />
   <object type="application/x-shockwave-flash" data="player.swf?soundFile=archivo.mp3">
      <param name="movie" value="player.swf?soundFile=archivo.mp3" />
      <a href="archivo.mp3">Descarga el archivo de audio</a>
   </object>
</audio>
```

En este ejemplo hemos añadido además una tercera línea con un reproductor Flash por si no fuesen soportados ninguno de los formatos anteriores, y un link directo de descarga para aquellos que tampoco soporten Flash. Así estaremos ofreciendo nuestro contenido a todos los navegadores y dispositivos manteniendo unas buenas prácticas en cuanto a accesibilidad del contenido se refiere.

