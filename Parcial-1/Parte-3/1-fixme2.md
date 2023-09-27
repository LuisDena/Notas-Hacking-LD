# fixme2
## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)
## Pistas
P1: Are equality and assignment the same symbol?
P2: To view the file in the webshell, do: `$ nano fixme2.py`
P3: To exit `nano`, press Ctrl and x and follow the on-screen prompts.
P4: The `str_xor` function does not need to be reverse engineered for this challenge.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
--------------------------------------------------------------
dena-picoctf@webshell:~$ mkdir fixme2
dena-picoctf@webshell:~$ cd fixme2/
dena-picoctf@webshell:~/fixme2$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2023-09-27 15:50:33--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.93, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py               100%[============================>]   1.00K  --.-KB/s    in 0s      

2023-09-27 15:50:33 (47.0 MB/s) - 'fixme2.py' saved [1029/1029]

dena-picoctf@webshell:~/fixme2$ ls -la
total 4
drwxrwxr-x 2 dena-picoctf dena-picoctf   23 Sep 27 15:50 .
drwxr-xr-x 6 dena-picoctf dena-picoctf  165 Sep 27 15:50 ..
-rw-rw-r-- 1 dena-picoctf dena-picoctf 1029 Mar 16  2023 fixme2.py
dena-picoctf@webshell:~/fixme2$ nano fixme2.py 
dena-picoctf@webshell:~/fixme2$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
dena-picoctf@webshell:~/fixme2$ 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



