# Forbidden Paths
## Objetivo
Here's the [website](http://saturn.picoctf.net:64403/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Pistas
P1:

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}
---------------------------------------------------------------------------
Entramos a la pagina e intentamos acceder a la flag con los datos que nos da el reto, como esta filtrando la direccion de los archivos, intentamos con /.. para que no haga dicho paso y colocamos al final el nombre del archivo que nos interesa tal que:
../../../../../flag.txt 
esto con respecto a la direccion indicada 
lo que nos da 
picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}
---------------------------------------------------------------------
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
