# Scavenger-Hun
## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?
## Pistas
P1: You should have enough hints to find the files, don't run a brute forcer.
P2:
P3:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}
----------------------------------------------------------------------------------------
|   |   |
|---|---|
||<!doctype html>|
||<html>|
||<head>|
||<title>Scavenger Hunt</title>|
||<link href="[https://fonts.googleapis.com/css?family=Open+Sans\|Roboto](https://fonts.googleapis.com/css?family=Open+Sans\|Roboto)" rel="stylesheet">|
||<link rel="stylesheet" type="text/css" href="[mycss.css](http://mercury.picoctf.net:55079/mycss.css)">|
||<script type="application/javascript" src="[myjs.js](http://mercury.picoctf.net:55079/myjs.js)"></script>|
||</head>|
|||
||<body>|
||<div class="container">|
||<header>|
||<h1>Just some boring HTML</h1>|
||</header>|
|||
||<button class="tablink" onclick="openTab('tabintro', this, '#222')" id="defaultOpen">How</button>|
||<button class="tablink" onclick="openTab('tababout', this, '#222')">What</button>|
|||
||<div id="tabintro" class="tabcontent">|
||<h3>How</h3>|
||<p>How do you like my website?</p>|
||</div>|
|||
||<div id="tababout" class="tabcontent">|
||<h3>What</h3>|
||<p>I used these to make this site: <br/>|
||HTML <br/>|
||CSS <br/>|
||JS (JavaScript)|
||</p>|
||<!-- Here's the first part of the flag: picoCTF{t -->|
||</div>|
|||
||</div>|
|||
||</body>|
||</html>|
|||
----------------------------------------------------------------------------------------
div.container {
    width: 100%;
}

header {
    background-color: black;
    padding: 1em;
    color: white;
    clear: left;
    text-align: center;
}

body {
    font-family: Roboto;
}

h1 {
    color: white;
}

p {
    font-family: "Open Sans";
}

.tablink {
    background-color: #555;
    color: white;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    font-size: 17px;
    width: 50%;
}

.tablink:hover {
    background-color: #777;
}

.tabcontent {
    color: #111;
    display: none;
    padding: 50px;
    text-align: center;
}

#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
-------------------------------------------------------------------------------------
function openTab(tabName,elmnt,color) {
    var i, tabcontent, tablinks;
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
	tabcontent[i].style.display = "none";
    }
    tablinks = document.getElementsByClassName("tablink");
    for (i = 0; i < tablinks.length; i++) {
	tablinks[i].style.backgroundColor = "";
    }
    document.getElementById(tabName).style.display = "block";
    if(elmnt.style != null) {
	elmnt.style.backgroundColor = color;
    }
}

window.onload = function() {
    openTab('tabintro', this, '#222');
}

/* How can I keep Google from indexing my website? */
Gracias a ese comentario sabemos que tenemos que usar robots.txt la parte indexada lo que da
http://mercury.picoctf.net:55079/robots.txt
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
Gracias a ese comentario sabemos que tenemos que ver el apache server, esto lo hacemos agregando `.htaccess` en la direccion de la pagina

http://mercury.picoctf.net:55079/.htaccess

# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
Con esto podemos ver que se tiene que hacer gracias al comentario que nos dice que esta guardando información en una MAC por lo que tenemos que verlo  

http://mercury.picoctf.net:55079/.DS_Store

Congrats! You completed the scavenger hunt. Part 5: _74cceb07}

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.hostinger.mx/tutoriales/que-es-el-archivo-htaccess
https://en.wikipedia.org/wiki/.DS_Store
https://www.hackplayers.com/2018/07/rutas-web-mediante-dsstore.html
