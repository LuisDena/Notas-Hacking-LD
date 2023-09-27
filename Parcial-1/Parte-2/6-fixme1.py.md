# fixme1.py
## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## Pistas
P1: Indentation is very meaningful in Python
P2: To view the file in the webshell, do: `$ nano fixme1.py`
P3: To exit `nano`, press Ctrl and x and follow the on-screen prompts.
P4: The `str_xor` function does not need to be reverse engineered for this challenge.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{1nd3nt1ty_cr1515_09ee727a}
--------------------------------------------------
dena-picoctf@webshell:~$ mkdir fixme1
dena-picoctf@webshell:~$ cd fixme1/
dena-picoctf@webshell:~/fixme1$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2023-09-26 22:25:41--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py               100%[============================>]     837  --.-KB/s    in 0s      

2023-09-26 22:25:41 (349 MB/s) - 'fixme1.py' saved [837/837]

dena-picoctf@webshell:~/fixme1$ nano fixme1.py 
dena-picoctf@webshell:~/fixme1$ python3 fixme1.py 
  File "/home/dena-picoctf/fixme1/fixme1.py", line 16
    flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x06) + chr(0x1c) + chr(0x5a) + chr(0x5c) + chr(0x55) + chr(0x40) + chr(0x3a) + chr(0x5e) + chr(0x52) + chr(0x0c) + chr(0x01) + chr(0x42) + chr(0x57) + chr(0x59) + chr(0x0a) + chr(0x14)
TabError: inconsistent use of tabs and spaces in indentation
dena-picoctf@webshell:~/fixme1$ nano fixme1.py 
dena-picoctf@webshell:~/fixme1$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
dena-picoctf@webshell:~/fixme1$ ^C
dena-picoctf@webshell:~/fixme1$ ^C
dena-picoctf@webshell:~/fixme1$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
