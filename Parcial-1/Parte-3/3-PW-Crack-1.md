# PW Crack 1
## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Pistas
P1: To view the file in the webshell, do: `$ nano level1.py`
P2: To exit `nano`, press Ctrl and x and follow the on-screen prompts.
P3: The `str_xor` function does not need to be reverse engineered for this challenge.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{545h_r1ng1ng_fa343060}
------------------------------------------------------
dena-picoctf@webshell:~/PWC1$ wget https://artifacts.picoctf.net/c/11/level1.py
--2023-09-27 16:08:11--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py               100%[============================>]     876  --.-KB/s    in 0s      

2023-09-27 16:08:11 (52.7 MB/s) - 'level1.py' saved [876/876]

dena-picoctf@webshell:~/PWC1$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2023-09-27 16:08:21--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.71, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc     100%[============================>]      30  --.-KB/s    in 0s      

2023-09-27 16:08:22 (2.16 MB/s) - 'level1.flag.txt.enc' saved [30/30]

dena-picoctf@webshell:~/PWC1$ nano level1.py
dena-picoctf@webshell:~/PWC1$ python3 level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
dena-picoctf@webshell:~/PWC1$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



