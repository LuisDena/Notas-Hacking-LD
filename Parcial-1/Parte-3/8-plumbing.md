# plumbing
## Objetivo
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.
## Pistas
P1: Remember the flag format is picoCTF{XXXX}
P2: What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
P3:
P4:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{digital_plumb3r_ea8bfec7}
------------------------------------------------------
dena-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 | grep "pico"
picoCTF{digital_plumb3r_ea8bfec7}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 

https://www.linfo.org/pipes.html


