# Obedient-cat
## Objetivo
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).

## Datos de acceso al nivel
```bash
Usuario: Dena 
Contraseña: notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
--------------------------------------------------------
dena-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
--2023-09-25 16:49:26--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag.1'

flag.1                  100%[============================>]      34  --.-KB/s    in 0s      

2023-09-25 16:49:26 (19.0 MB/s) - 'flag.1' saved [34/34]

dena-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
dena-picoctf@webshell:~$ 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| wget | descargar de internet con el enlace |

## Referencias 
