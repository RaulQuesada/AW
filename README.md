# HTML y CSS<br>
### Estructura mínima de una web 
```html
	<!DOCTYPE html>
	<html>
	<head>
		<title></title>
	</head>
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
### ¿Qué son las pseudoclases?, pon ejemplos.
### Explica el modelo de caja de CSS (margin, border y padding)
### Explica que son los selectores de CSS y pon ejemplos
### Di a quien afectan:
  p a { color: red;<br>
  p > a { color: red; }<br>
  h1 + h2 { color: red }<br>
  a[class] { color: blue; }<br>
  a[class="externo"] { color: blue; }<br>
  a[href="http://www.ejemplo.com"] { color: blue; }
