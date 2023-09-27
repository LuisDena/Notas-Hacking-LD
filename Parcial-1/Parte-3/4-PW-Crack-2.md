# PW Crack 2
## Objetivo
Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Pistas
P1: Does that encoding look familiar?
P2: The `str_xor` function does not need to be reverse engineered for this challenge.
P3:
P4:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{tr45h_51ng1ng_489dea9a}
--------------------------------------------------------
dena-picoctf@webshell:~/PWC1$ cd ..
dena-picoctf@webshell:~$ mkdir PWC2
dena-picoctf@webshell:~$ cd PWC2/
dena-picoctf@webshell:~/PWC2$ wget https://artifacts.picoctf.net/c/13/level2.py
--2023-09-27 16:12:24--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py               100%[============================>]     914  --.-KB/s    in 0s      

2023-09-27 16:12:24 (149 MB/s) - 'level2.py' saved [914/914]

dena-picoctf@webshell:~/PWC2$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2023-09-27 16:12:38--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc     100%[============================>]      31  --.-KB/s    in 0s      

2023-09-27 16:12:38 (1.25 MB/s) - 'level2.flag.txt.enc' saved [31/31]

dena-picoctf@webshell:~/PWC2$ nano level2.py 
dena-picoctf@webshell:~/PWC2$ python -c "print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) 
"
  File "<string>", line 1
    print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) 
         ^
SyntaxError: '(' was never closed
dena-picoctf@webshell:~/PWC2$ python -c "print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) )"
de76
dena-picoctf@webshell:~/PWC2$ python3 level2.py                                             
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
dena-picoctf@webshell:~/PWC2$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



