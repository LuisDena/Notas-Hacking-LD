# Includes
## Objetivo
Go to this [website](http://saturn.picoctf.net:61941/) and see what you can discover.
## Pistas
P1: Is there more code than what the inspector initially shows?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}
---------------------------------------
Entramos a la pagina clickeamos el unico boton y nos da la pista y la inspeccionamos y nos metemos a los archivos de estilo y js para ver la flag
-----------------------------------------
|   |   |
|---|---|
||<!DOCTYPE html>|
||<html lang="en">|
||<head>|
||<meta charset="UTF-8">|
||<meta name="viewport" content="width=device-width, initial-scale=1.0">|
||<meta http-equiv="X-UA-Compatible" content="ie=edge">|
||<link rel="stylesheet" href="[style.css](http://saturn.picoctf.net:61941/style.css)">|
||<title>On Includes</title>|
||</head>|
||<body>|
||<script src="[script.js](http://saturn.picoctf.net:61941/script.js)"></script>|
|||
||<h1>On Includes</h1>|
||<p>Many programming languages and other computer files have a directive,|
||often called include (sometimes copy or import), that causes the|
||contents of a second file to be inserted into the original file. These|
||included files are called copybooks or header files. They are often used|
||to define the physical layout of program data, pieces of procedural code|
||and/or forward declarations while promoting encapsulation and the reuse|
||of code.</p>|
||<br>|
||<p> Source: Wikipedia on Include directive </p>|
||<button type="button" onclick="greetings();">Say hello</button>|
||</body>|
||</html>|
|||
CSS -----------------------------------------------------------
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */
JS ---------------------------------------------------------------
  

function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_6edef411}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
