# Codebook
## Objetivo
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
## Pistas
P1: On the webshell, use `ls` to see if both files are in the directory you are in
P2: The `str_xor` function does not need to be reverse engineered for this challenge.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{c0d3b00k_455157_d9aa2df2}
--------------------------------------------------------
dena-picoctf@webshell:~$ ls -la
total 28
drwxr-xr-x 3 dena-picoctf dena-picoctf  126 Sep 25 17:32 .
drwxr-xr-x 3 root         root           26 Sep 25 16:30 ..
-rw------- 1 dena-picoctf dena-picoctf 1440 Sep 25 17:46 .bash_history
-rw-r--r-- 1 dena-picoctf dena-picoctf  220 Sep 25 16:30 .bash_logout
-rw-r--r-- 1 dena-picoctf dena-picoctf 3771 Sep 25 16:30 .bashrc
-rw-r--r-- 1 dena-picoctf dena-picoctf  807 Sep 25 16:30 .profile
drwx------ 2 dena-picoctf dena-picoctf   48 Sep 25 17:33 .ssh
-rw-rw-r-- 1 dena-picoctf dena-picoctf  167 Sep 25 16:33 .wget-hsts
-rw-r--r-- 1 root         root         4443 Sep 26 21:49 README.txt
dena-picoctf@webshell:~$ mkdir codebook
dena-picoctf@webshell:~$ cd codebook/
dena-picoctf@webshell:~/codebook$ wget https://artifacts.picoctf.net/c/1/code.py
--2023-09-26 21:50:22--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                 100%[============================>]   1.25K  --.-KB/s    in 0s      

2023-09-26 21:50:22 (567 MB/s) - 'code.py' saved [1278/1278]

dena-picoctf@webshell:~/codebook$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-09-26 21:50:34--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt            100%[============================>]      27  --.-KB/s    in 0s      

2023-09-26 21:50:34 (11.4 MB/s) - 'codebook.txt' saved [27/27]

dena-picoctf@webshell:~/codebook$ ls   
code.py  codebook.txt
dena-picoctf@webshell:~/codebook$ ls -la
total 8
drwxrwxr-x 2 dena-picoctf dena-picoctf   41 Sep 26 21:50 .
drwxr-xr-x 4 dena-picoctf dena-picoctf  142 Sep 26 21:50 ..
-rw-rw-r-- 1 dena-picoctf dena-picoctf 1278 Mar 16  2023 code.py
-rw-rw-r-- 1 dena-picoctf dena-picoctf   27 Mar 16  2023 codebook.txt
dena-picoctf@webshell:~/codebook$ chmod +x code.py 
dena-picoctf@webshell:~/codebook$ ./code.py 
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
./code.py: line 7: syntax error near unexpected token `('
./code.py: line 7: `def str_xor(secret, key):'
dena-picoctf@webshell:~/codebook$ cat codebook.txt 
azbycxdwevfugthsirjqkplomn
dena-picoctf@webshell:~/codebook$ nano code.py 
dena-picoctf@webshell:~/codebook$ nano code.py 
dena-picoctf@webshell:~/codebook$ nano code.py 
dena-picoctf@webshell:~/codebook$ nano code.py 
dena-picoctf@webshell:~/codebook$ python3 code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}
dena-picoctf@webshell:~/codebook$ ^C
dena-picoctf@webshell:~/codebook$ 
```
## Notas Adicionales
4: c, 14:h, 13:t,14:h,23:o,25:n,16:i,0:a,25:n,
pass: chthonian
| Comando  | Descripción | 
|------------|--------------|

## Referencias 
