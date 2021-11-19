# Geolocalización

La geolocalización es la forma de obtener tu posición en el mundo y si quieres, compartir esta información. Existen muchas maneras de descubrir donde te encuentras, por tu dirección IP, la conexión de red inalámbrica, la torre de telefonía móvil por la que se conecta tu móvil, o usando directamente el posicionador GPS.

HTML5 incorpora una nueva funcionalidad para facilitar esta tarea, que dependerá de que el navegador le de soporte. Está disponible a partir de las versiones de Opera 10.6, Firefox 3.5, Chrome 5, Safari 5 e Internet Explorer 9.

Para obtener la localización simplemente tienes que utilizar el objeto `navigator` de JavaScript. Inicialmente es recomendable comprobar si está disponible la localización y de ser así ya podemos utilizar el método `getCurrentPosition` de la forma: 

```javascript
if (navigator.geolocation)
{
   navigator.geolocation.getCurrentPosition(showPosition);
}

function showPosition( position )
{
      var lat = position.coords.latitude;
      var lng = position.coords.longitude;

      alert( "Latitud: " + lat + ", longitud: " + lng );
}
```

