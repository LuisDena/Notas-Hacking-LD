# what's a net cat?
## Objetivo
Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `25103` to get the flag?
## Pistas

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{nEtCat_Mast3ry_d0c64587}
--------------------------------------------------------
dena-picoctf@webshell:~$ mkdir wnc
dena-picoctf@webshell:~$ cd wnc/
dena-picoctf@webshell:~/wnc$ nc jupiter.challenges.picoctf.org 25103
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_d0c64587}
^C
dena-picoctf@webshell:~/wnc$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
