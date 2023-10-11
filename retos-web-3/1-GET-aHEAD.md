# GET-aHEAD
## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:28916/](http://mercury.picoctf.net:28916/)
## Pistas

P1: Maybe you have more than 2 choices
P2: Check out tools like Burpsuite to modify your requests and look at the responses
P3:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
----------------------------------------------------------------------------------------
|   |   |
|---|---|
|||
||<!doctype html>|
||<html>|
||<head>|
||<title>Red</title>|
||<link rel="stylesheet" type="text/css" href="[//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css](http://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css)">|
||<style>body {background-color: red;}</style>|
||</head>|
||<body>|
||<div class="container">|
||<div class="row">|
||<div class="col-md-6">|
||<div class="panel panel-primary" style="margin-top:50px">|
||<div class="panel-heading">|
||<h3 class="panel-title" style="color:red">Red</h3>|
||</div>|
||<div class="panel-body">|
||<form action="index.php" method="GET">|
||<input type="submit" value="Choose Red"/>|
||</form>|
||</div>|
||</div>|
||</div>|
||<div class="col-md-6">|
||<div class="panel panel-primary" style="margin-top:50px">|
||<div class="panel-heading">|
||<h3 class="panel-title" style="color:blue">Blue</h3>|
||</div>|
||<div class="panel-body">|
||<form action="index.php" method="POST">|
||<input type="submit" value="Choose Blue"/>|
||</form>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||</body>|
||</html>|
|||
-------------
Se puede usar la herramienta que se menciona pero en mi caso usé friefox que permite hacer el reenvio del formulario cambiando el "GET" de la opcion "Red" por "HEAD" lo que nos devuelve en el apartado de "Encabezados de respuesta" la flag
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://portswigger.net/burp
https://developer.mozilla.org/es/docs/Web/HTTP/Methods