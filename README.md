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
##### Externo
En la cabecera del HTML,incluimos una relación al archivo CSS en cuestión. Los navegadores sabrán que deben aplicar los estilos del archivo, ejemplo.css al documento HTML actual.
```html
	<!DOCTYPE html>
	<html>
	<head>
	<link rel="stylesheet" type="text/css" href="ejemplo.css" />
		<title></title>
	</head>
	</body>
	</html>
```
### Crea una lista sin ordenar con 5 ingredientes de una receta de cocina
### Como se puede incluir javascript en HTML
### ¿Que diferencia hay entre una clase y una ID
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
