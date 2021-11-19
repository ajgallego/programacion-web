# Formularios

Los formularios permiten solicitar información al visitante de una página Web. Están compuestos por campos de diferente tipo, cuya información se enviará a una dirección URL (indicada en el código) al pulsar el botón de envío.

La declaración de formulario queda recogida por las etiquetas `<form></form>`, las cuales deben encerrar la definición de todos los campos del formulario. En la etiqueta de apertura `<form>` tenemos que indicar los atributos básicos:

* `action=""`: Entre comillas se indica la acción a realizar al enviar el formulario. En general se indicará el nombre de un fichero alojado en el servidor, el cual se encargará de procesar la información. Aunque también se le puede indicar una dirección de correo para que envíe directamente todo el contenido, de la forma: `mailto:direccion_de_correo`.

* `method=""` (`post` o `get`): Indica el método de transferencia de las variables. El método "`post`" envía los datos de forma no visible, mientras que el método "`get`" los adjunta a la URL a la que se redirige.

* `enctype= ""`: Especifica el tipo de codificación de la información enviada. Con `method="get"` no se realiza codificación, solo se cambian caracteres especiales como el espacio, por lo que no es necesario indicar `enctype`. Cuando el valor del atributo "`method`" es "`post`", podemos utilizar los siguientes valores:

    * `application/x-www-form-urlencoded`: Es el valor predeterminado. Codifica todos los caracteres antes de enviarlos.

    * `multipart/form-data`: Es requerido al enviar archivos mediante un formulario. No codifica la información.

    * `text/plain`: No codifica la información, solo cambia los espacios por el símbolo "+".
    
Por ejemplo, una posible cabecera de un formlario sería: 

```html
<form action="http://www.miweb.com/procesarformulario" method="POST">

    <!-- Como no indicamos el enctype se utilizará la condificación por defecto -->

    <!-- Campos del formulario -->
    <!-- Campos del formulario -->
    <!-- Campos del formulario -->

</form>
```



## Tipos de campos básicos

Para añadir campos al formulario se utiliza la etiqueta `<input/>`, esta etiqueta debe de tener siempre dos atributos:

* `name=""`: Indica el nombre que se asigna a un determinado campo. Este nombre no aparece visible en la Web, pues se utiliza para poder distinguir cada campo al enviar la información al servidor o por correo. Es como si fuera el nombre de la variable a la que se asigna el valor del campo.

* `type=""`: Indica el tipo de campo a utilizar. Puede ser de muchos tipos: text, password, checkbox, radio, file, hidden, submit, reset.


A continuación se describen más detalladamente los diferentes tipos de campos `<input/>` según su valor `type`:

* `type="text"`: campo de tipo texto de una línea. Sus atributos son:
    * `maxlenght=""`: Seguido de un valor que limitará el número máximo de caracteres.
    * `size=""`: Seguido de un valor que limitará el número de caracteres a mostrar en pantalla. A diferencia de maxlenght este atributo no limita la longitud del texto que se puede introducir, sino que modifica el tamaño visible del campo.
    * `value=""`: Indica el valor inicial del campo.
    A continuación se incluye un ejemplo de uso:
```html
<input name="usuario" type="text" maxlenght="24"/>
```

* `type="password"`: Este campo funciona exactamente igual que el de tipo "text", pero ocultará el texto introducido cambiando las letras por asteriscos o puntos. Sus atributos son los mismos que para "text".

* `type="checkbox"`: Este campo mostrará una casilla cuadrada que nos permitirá marcar opciones de una lista (podremos marcar varias opciones a la vez). Para indicar que varias casillas pertenecen al mismo grupo se les debe de dar el mismo nombre para el atributo "name". El texto que queramos que aparezca a continuación de la casilla del "checkbox" se tendrá que escribir después de cerrar la etiqueta `<input/>`. Sus atributos son:
    * `value=""`: Define el valor que será enviado si la casilla está marcada.
    * `checked`: Este atributo es opcional, y hace que la casilla aparezca marcada por defecto. No necesita indicarle ningún valor.
    Ejemplo:
```html
<input type="checkbox" name="option1" value="leche"/> Leche<br/>
<input type="checkbox" name="option1" value="pan" checked/> Pan<br/>
<input type="checkbox" name="option1" value="queso"/> Queso<br/>
```


* `type="radio"`: El campo se elegirá marcando de entre varias opciones una casilla circular. Al marcar una casilla el resto de casillas de ese grupo de desmarcarán automáticamente. Para indicar que varias casillas pertenecen al mismo grupo se les debe de dar el mismo nombre para el atributo "name" (ver ejemplo). Además debemos de indicar:
    * `value=""`: Define el valor que será enviado si la casilla está marcada.
    * `checked`: Este atributo es opcional, y hace que la casilla aparezca marcada por defecto. Solo se podrá usar para una casilla. No necesita indicarle ningún valor.
      Ejemplo:
```html
<input type="radio" name="group1" value="leche"/> Leche<br/>
<input type="radio" name="group1" value="pan" checked/> Pan<br/>
<input type="radio" name="group1" value="queso"/> Queso<br/>
```


* `type="file"`: El atributo file permite al usuario subir archivos. Necesitaremos un programa que gestione estos archivos en el servidor mediante un lenguaje diferente al HTML. El único atributo opcional que podemos utilizar es `size=""` mediante el cual podremos indicar la anchura visual de este campo. Ejemplo:
```html
<input type="file" name="datafile" size="40"/>
```

* `type="hidden"`: Este valor no puede ser modificado, pues permanece oculto. Se suele utilizar para enviar al método encargado de procesar el formulario algún dato adicional necesario para su procesamiento. Para indicar el valor de este campo utilizamos el atributo: `value = "valor"`.

* `type="submit"`: Representa el botón de "Enviar". Al pulsar este botón la información de todos los campos se enviará realizando la acción indicada en `<form>`. Mediante el atributo:
    * `value="texto"`: podemos indicar el texto que aparecerá en el botón.

* `type="reset"`: Al pulsar este botón se borra el contenido de todos los campos del formulario. Mediante el atributo:
    * `value="texto"`: podemos indicar el texto que aparecerá en el botón.



## Etiquetas

Las etiquetas se utilizan para poner un texto o descripción de los campos de un formulario. Se escriben usando la etiqueta HTML `<label>` y tienen un único atributo "`for`" que se utiliza para indicar el nombre (atributo `name`) del campo asociado. Por ejemplo: 

```html
<label for="campo1">Etiqueta</label>
<input name="campo1" type="text"/>
```




## Campos de Selección

Mediante la etiqueta `<select></select>` podemos crear listas de opciones, que nos permitirán seleccionar entre una o varias de ellas. Sus atributos son:

* `name=""`: Nombre del campo.
* `size=""`: Número de opciones visibles a la vez. Si no se indica nada o se le asigna un valor de uno se presentará como un menú desplegable. En el caso de valores mayores que uno aparecerá como una lista con una barra de desplazamiento.
* `multiple`: Permite seleccionar mas de un valor a la vez para el campo.

Las diferentes opciones de la lista se indicarán mediante la etiqueta `<option></option>`. El nombre que se visualizará debe de indicarse dentro de estas etiquetas. Mediante el atributo `value=""` podemos indicar el valor que se enviará con el formulario. También podemos utilizar el atributo `selected` para indicar la opción seleccionada por defecto. Si no lo especificamos, siempre aparecerá como seleccionado el primer elemento de la lista.

```html
<select name="Colores" multiple>
   <option value="r">Rojo</option>
   <option value="g">Verde</option>
   <option value="b">Azul</option>
</select>
<select name="Colores" SIZE="1">
   <option value="r">Rojo</option>
   <option value="g" selected>Verde</option>
   <option value="b">Azul</option>
</select>
```


## Áreas de texto

Mediante las etiquetas `<textarea></textarea>` podemos crear un campo de texto de múltiples líneas. Los atributos que podemos utilizar son:

* `name=""`: Nombre del campo.
* `cols="num"`: Número de columnas de texto visibles. Este atributo es opcional.
* `rows="num"`: Número de filas de texto visibles. Este atributo es opcional.



## Ejemplo

A continuación se incluye un ejemplo de uso de los formularios en el que se han incluido la mayoría de los campos que hemos visto: 

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
   <title>Ejemplo</title>
   <meta charset="utf-8"/>
</head>
<body>
    <h2>Formulario de registro</h2>
    <p>Escribe tus datos de usuario en el siguiente formulario y 
	    por último aprieta el botón enviar.</p>

    <form action="http://www.miweb.com/procesarformulario" method="POST">
		<p>
			<label for="usuario">Usuario: </label>
			<input name="usuario" type="text" maxlenght="32"/>
		</p>
		<p>
			<label for="password">Contraseña: </label>
			<input name="password" type="password" maxlenght="16"/>
		</p>
		<p>
			<label for="nombre">Nombre completo: </label>
			<input name="nombre" type="text" maxlenght="64"/>
		</p>
		<p>
			<label for="direccion">Dirección: </label>
			<input name="direccion" type="text" maxlenght="128"/>
		</p>
		<p>
			<label for="ciudad">Ciudad: </label>
			<select name="ciudad">
				<option value="A Coruña">A Coruña</option>
				<option value="Álava">Álava</option>
				<option value="Albacete">Albacete</option>
				<option value="Alicante">Alicante</option>
				<option value="Almería">Almería</option>
				<option value="Asturias">Asturias</option>
				<!-- resto de ciudades... -->
			</select>
		</p>
		<p>
			<label for="tipo">Tipo de cliente: </label><br/>
			<input type="radio" name="tipo" value="particular" checked/> Particular<br/>
			<input type="radio" name="tipo" value="profesional"/> Profesional<br/>
		</p>
		<p>
			<label for="comentarios">Comentarios: </label><br/>
			<textarea name="comentarios" rows="4" cols="50"></textarea>
		</p>
		<p>
			<input type="checkbox" name="terminos" value="terminos"/>
			<label for="terminos">Acepto los términos y condiciones de uso</label>
		</p>
		<p>
			<input type="submit" value="Enviar"/>
			<input type="reset" value="Borrar formulario"/>
		</p>
	</form>
   
</body>
</html>
```

Como se puede ver cada par de etiqueta y campo de formulario se ha encerrado dentro de un párrafo `<p>` para que ocupe una única línea y que el siguiente campo baje a la línea siguiente. Este mismo efecto se podría conseguir usando la etiqueta `<div>`. Para mejorar el aspecto visual del formulario se tendrían que aplicar estilos CSS, los cuales se tratarán en el siguiente capítulo. 


Si guardamos este código en un fichero ".html" y lo abrimos con el navegador obtendríamos un resultado similar al siguiente: 

![](images/ejemplo_formulario_1.png)







