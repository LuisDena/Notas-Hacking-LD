# PW Crack 3
## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Pistas
P1: To view the level3.hash.bin file in the webshell, do: $ bvi level3.hash.bin
P2: To exit `bvi` type `:q` and press enter.
P3: The `str_xor` function does not need to be reverse engineered for this challenge.
P4:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{m45h_fl1ng1ng_cd6ed2eb}
---------------------------------------------------------
dena-picoctf@webshell:~/PWC1$ cd ..
dena-picoctf@webshell:~$ mkdir PWC2
dena-picoctf@webshell:~$ cd PWC2/
dena-picoctf@webshell:~/PWC2$ wget https://artifacts.picoctf.net/c/13/level2.py
dena-picoctf@webshell:~$ mkdir PWC3
dena-picoctf@webshell:~$ cd PWC3/
dena-picoctf@webshell:~/PWC3$ wget https://artifacts.picoctf.net/c/17/level3.py
--2023-09-27 16:16:20--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py               100%[============================>]   1.31K  --.-KB/s    in 0s      

2023-09-27 16:16:21 (59.6 MB/s) - 'level3.py' saved [1337/1337]

dena-picoctf@webshell:~/PWC3$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2023-09-27 16:16:48--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc     100%[============================>]      31  --.-KB/s    in 0s      

2023-09-27 16:16:49 (7.35 MB/s) - 'level3.flag.txt.enc' saved [31/31]

dena-picoctf@webshell:~/PWC3$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2023-09-27 16:16:55--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin         100%[============================>]      16  --.-KB/s    in 0s      

2023-09-27 16:16:55 (1.03 MB/s) - 'level3.hash.bin' saved [16/16]

dena-picoctf@webshell:~/PWC3$ ls -la
total 16
drwxrwxr-x  2 dena-picoctf dena-picoctf   73 Sep 27 16:16 .
drwxr-xr-x 10 dena-picoctf dena-picoctf 4096 Sep 27 16:15 ..
-rw-rw-r--  1 dena-picoctf dena-picoctf   31 Mar 16  2023 level3.flag.txt.enc
-rw-rw-r--  1 dena-picoctf dena-picoctf   16 Mar 16  2023 level3.hash.bin
-rw-rw-r--  1 dena-picoctf dena-picoctf 1337 Mar 16  2023 level3.py
dena-picoctf@webshell:~/PWC3$ nano level3.py 
dena-picoctf@webshell:~/PWC3$ nano level3.
level3.flag.txt.enc  level3.hash.bin      level3.py            
dena-picoctf@webshell:~/PWC3$ nano level3.
level3.flag.txt.enc  level3.hash.bin      level3.py            
dena-picoctf@webshell:~/PWC3$ nano level3.flag.txt.enc 
dena-picoctf@webshell:~/PWC3$ nano level3.hash.bin     
dena-picoctf@webshell:~/PWC3$ bvi level3.hash.bin

bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
dena-picoctf@webshell:~/PWC3$ cat level3.py 
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: dba8
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: f09e
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 752e
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 3961
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: f159
That password is incorrect
dena-picoctf@webshell:~/PWC3$ f09e
-bash: f09e: command not found
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: f09e
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 4dcf       
That password is incorrect
dena-picoctf@webshell:~/PWC3$ python level3.py 
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
dena-picoctf@webshell:~/PWC3$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



