# Local Authority
## Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:49386/) and see what you can discover.
## Pistas
How is the password checked on this website?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
---------------------------------------------------------------
nos metemos a la pagina e intentamos logearnos una vez hecho esto inspeccionamos la pagina y podemos ver que hay un link secure.js y de ahí sacamos las credenciales y nos logeamos
------------------------------------------------------
|   |   |
|---|---|
||<!DOCTYPE html>|
||<html lang="en">|
||<head>|
||<meta charset="UTF-8">|
||<meta name="viewport" content="width=device-width, initial-scale=1.0">|
||<meta http-equiv="X-UA-Compatible" content="ie=edge">|
||<link rel="stylesheet" href="[style.css](http://saturn.picoctf.net:49386/style.css)">|
||<title>Login Page</title>|
||</head>|
||<body>|
||<script src="[secure.js](http://saturn.picoctf.net:49386/secure.js)"></script>|
|||
||<p id='msg'></p>|
|||
||<form hidden action="admin.php" method="post" id="hiddenAdminForm">|
||<input type="text" name="hash" required id="adminFormHash">|
||</form>|
|||
||<script type="text/javascript">|
||function filter(string) {|
||filterPassed = true;|
||for (let i =0; i < string.length; i++){|
||cc = string.charCodeAt(i);|
|||
||if ( (cc >= 48 && cc <= 57) \||
||(cc >= 65 && cc <= 90) \||
||(cc >= 97 && cc <= 122) )|
||{|
||filterPassed = true;|
||}|
||else|
||{|
||return false;|
||}|
||}|
|||
||return true;|
||}|
|||
||window.username = "admin";|
||window.password = "admin";|
|||
||usernameFilterPassed = filter(window.username);|
||passwordFilterPassed = filter(window.password);|
|||
||if ( usernameFilterPassed && passwordFilterPassed ) {|
|||
||loggedIn = checkPassword(window.username, window.password);|
|||
||if(loggedIn)|
||{|
||document.getElementById('msg').innerHTML = "Log In Successful";|
||document.getElementById('adminFormHash').value = "2196812e91c29df34f5e217cfd639881";|
||document.getElementById('hiddenAdminForm').submit();|
||}|
||else|
||{|
||document.getElementById('msg').innerHTML = "Log In Failed";|
||}|
||}|
||else {|
||document.getElementById('msg').innerHTML = "Illegal character in username or password."|
||}|
||</script>|
|||
||</body>|
||</html>|
|||
---------------------------------------------------

  

function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
