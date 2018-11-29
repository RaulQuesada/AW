# HTML y CSS *aun no terminado*<br>
### Estructura mínima de una web 
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	</head>
	<body>
	</body>
	</html>
```
<br>Por ejemplo en Sublime, donde pone "Plain text", seleccionamos HTML, y escribimos en la primer linea "html", tabulamos y nos saldra la estructura basica para trabajar.

### Explica las 3 formas de usar CSS en HTML
#### Interno
Añadir en la cabecera HTML del documento, mediante style. Hay que tener en cuenta que utilizándolo, arruinamos la ventaja de tener los estilos en un documento independiente, por lo que siempre es preferible guardarlo en un archivo externo CSS que expliquaré a continuación.
```html
	<!DOCTYPE html>
	<html>
	<head>
	<style type="text/css">
       		div {
         	color:red;
      	 }
   	 </style>
		<title></title>
	</head>
	<body>
	</body>
	</html>
```
#### Externo
En la cabecera del HTML,incluimos una relación al archivo CSS en cuestión. Los navegadores sabrán que deben aplicar los estilos del archivo, ejemplo.css al documento HTML actual.
```html
	<!DOCTYPE html>
	<html>
	<head>
	<link rel="stylesheet" type="text/css" href="ejemplo.css" />
		<title></title>
	</head>
	<body>
	</body>
	</html>
```
#### Inline
Se puede hacer directamente en las propias etiquetas, a través de "span style":
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	</head>
	<body>
	<article> Buenas <span style="background-color:blue>amigo lector</span>
	</body>
	</html>
```
### Crea una lista sin ordenar con 5 ingredientes de una receta de cocina
En el body ponemos "ul" para listas desordenadas y para cada uno de los elementos ponemos "li" para identificarlos.
```html
	<!DOCTYPE html>
	<html>
	<head>
	<style type="text/css">
   	 </style>
		<title></title>
	</head>
	<body>
	<ul>
  		<li>Harina</li>
  		<li>Te</li>
  		<li>Leche</li>
		<li>Pan</li>
		<li>Berberechos</li>
	</ul>
	</body>
	</html>
```
### Como se puede incluir javascript en HTML
Dentro del body ponemos la funcion "script" y ponemos lo que deseamos como por ejemplo la siguiente alerta.
```html
	<!DOCTYPE html>
	<html>
	<head>
	<style type="text/css">
   	 </style>
		<title></title>
	</head>
	<body>
		<script type="text/javascript">
			alert("hola wapeton");
		</script>
	</body>
	</html>
```
Y nos saldría la alerta cuando entremos en la página web o al reiniciarla
### ¿Que diferencia hay entre una clase y una ID
#### ID
El atributo “id” de un elemento es único así que no debería haber otro elemento con el mismo nombre de identificador (id) dentro del documento HTML.
```html
<!DOCTYPE html>
<html>
<head>
	<title> Cajitas </title>
	<style type="text/css">
		div{
			margin:0 0 25px;
			overflow: hidden;
			padding: 20px;
			width: 180px;
			height: 180px;
		}
		#CajaAzul{
			
			background-color: #d8ecf7;
			border: 1px solid #afcde3; 
		}

		#CajaRoja{
			
			background-color: #A00;
			border: 1px solid #F00; 
		}

		#CajaVerde{
			
			background-color: green;
			border: 1px solid #0F0;
		}
	</style>
</head>
<body>
	<div id="CajaAzul"><center>Caja azul</center></div>
	<div id="CajaRoja"><center>Caja roja</center></div>
	<div id="CajaVerde"><center>Caja verde</center></div>
</body>

</html>
```
#### CLASS
A diferencia del valor del atributo “id”, puede ser utilizado en más de un elemento del documento HTML, esto nos es importante cuando aplicamos los mismos estilos a diferentes elementos, dado que nos permite reducir las líneas de código en nuestro archivo .css.
```html
<!DOCTYPE html>
<html>
<head>
	<title></title>

	<style type="text/css">
	.container{
		text-align: center;
	}
	.container div{
		border: 1px solid lightblue;
		width: 19%;
		height: 120px;
		display: inline-block; 

	}	

	</style>

</head>
<body>

<div class="container">
	<div>PRUEBA</div>
	<div>PRUEBA</div>
	<div>PRUEBA</div>


</div>

</body>
</html>
```
### Código para hacer un enlace a otra página y que esta se abra en una nueva ventana
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	</head>
	<body>
	<a target="_blank" href="https://www.w3schools.com/css/exercise.asp">Ejercicios CSS</a>
	</body>
	</html>
```
### ¿Qué son las pseudoclases?, pon ejemplos.
Una pseudoclase CSS es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Estas permiten aplicar un estilo a un elemento no sólo en relación con el contenido del árbol de documento, sino también en relación a factores externos como el historial del navegador (:visited, por ejemplo), el estado de su contenido (como :active, que es cuando el usuario activ auna funcion), o la posición del ratón (como :hover que permite saber si el ratón está encima de un elemento o no).
#### Ejemplo :visited
La pseudo-clase (:visited) representa enlaces que el usuario ya ha visitado
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	<style>
		a {
  		background-color: white;
  		border: 1px solid blue;
		}

		a:visited {
	  	background-color: white;
  		border-color: hotpink;
  		color: hotpink;
		}
	</style>
	</head>
	<body>
	<a href="">Este enlace ha sido visto.</a>
	</body>
	</html>
```
Si no hemos entrado en el enlace nos saldran las letras de color azul con fondo blanco , en cambio si ya hemos entrado alguna vez, nos saldra con fondo blanco y las letras de color rosa chillon.
#### Ejemplo :active
Representa un elemento como el boton, que el usuario está activando.  Cuando se usa el mouse, la activación generalmente comienza cuando el usuario presiona el botón del mouse y termina cuando este se ha soltado.
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	<style>
		a:active {
		color: lightblue; 
		}
	</style>
	</head>
	<body>
	<a href="Ejemplo">Si activamos este enlace cambiará su color a azul claro</a>
	</body>
	</html>
```
#### Ejemplo : hover
Cuando el usuario interactúa con un elemento con un dispositivo señalador,como por ejemplo el mouse, pero no necesariamente lo activa. Generalmente se activa cuando el usuario se desplaza sobre dicho elemento con el cursor
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	<style>
		a {
 		 background-color: blue;
		}

		a:hover {
		background-color: yellow; 
		}
	</style>
	</head>
	<body>
	<a href="Ejemplo">Pasa el mouse por aqui.</a>
	</body>
	</html>
```
Asi de esta forma cuando tengamos el cursos encima del enlace, este cambiara de color de azul a amarillo
### Explica el modelo de caja de CSS (margin, border y padding)
El margin es el espacio que se deja entre el elemento en el que le ponemos el estilo y los diferentes elementos.
<br>
El padding es el espacio que se deja dentro de la caja para empezar a poner cosas dentro
<br>
El border como su propio nombre indica proporciona un borde adcional a la dimension del elemento o caja con dimensiones relativas
<br>
Si proporcionamos estos tres funciones a un mismo elemento, si este antes tenia un width de: 150px pasaran a sumarse estos tres ultimos valores.  Por ejemplo
```html
<html>
<head>
	<title> Cajitas </title>
	<style type="text/css">
		div{
			margin:25px;
			padding: 20px;
			border: 5px;
			width: 150px;
			height: 150px;
		}
	</style>
</head>
<body>
	<div>Espacio de trabajo</div>
	
</body>

</html>
```
En el ejemplo vemos como el width es de 150px pero sumandole las tres funciones quedaria una dimension de la caja total de 200px
### Explica que son los selectores de CSS y pon ejemplos
### Di a quien afectan:
 ###### p a { color: red;<br>
 ###### p > a { color: red; }<br>
 ###### h1 + h2 { color: red }<br>
 ###### a[class] { color: blue; }<br>
 ###### a[class="externo"] { color: blue; }<br>
 ###### a[href="http://www.ejemplo.com"] { color: blue; }
