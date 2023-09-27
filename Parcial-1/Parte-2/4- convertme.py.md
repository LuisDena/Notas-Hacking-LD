# convertme.py
## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Pistas
P1: Look up a decimal to binary number conversion app on the web or use your computer's calculator!
P2: The `str_xor` function does not need to be reverse engineered for this challenge.
P3: If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
P4: To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
P5: Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
P6: Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{4ll_y0ur_b4535_722f6b39}
------------------------------------------------------
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

dena-picoctf@webshell:~$ ls -la
total 28
drwxr-xr-x 4 dena-picoctf dena-picoctf  140 Sep 26 22:11 .
drwxr-xr-x 3 root         root           26 Sep 25 16:30 ..
-rw------- 1 dena-picoctf dena-picoctf 1440 Sep 25 17:46 .bash_history
-rw-r--r-- 1 dena-picoctf dena-picoctf  220 Sep 25 16:30 .bash_logout
-rw-r--r-- 1 dena-picoctf dena-picoctf 3771 Sep 25 16:30 .bashrc
drwxrwxr-x 3 dena-picoctf dena-picoctf   19 Sep 26 21:52 .local
-rw-r--r-- 1 dena-picoctf dena-picoctf  807 Sep 25 16:30 .profile
drwx------ 2 dena-picoctf dena-picoctf   48 Sep 25 17:33 .ssh
-rw-rw-r-- 1 dena-picoctf dena-picoctf  167 Sep 25 16:33 .wget-hsts
-rw-r--r-- 1 root         root         4443 Sep 26 21:49 README.txt
dena-picoctf@webshell:~$ mkdir convertme
dena-picoctf@webshell:~$ cd convertme/
dena-picoctf@webshell:~/convertme$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-09-26 22:13:02--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.18, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py            100%[============================>]   1.16K  --.-KB/s    in 0s      

2023-09-26 22:13:02 (312 MB/s) - 'convertme.py' saved [1189/1189]

dena-picoctf@webshell:~/convertme$ python3 convertme.py              
If 74 is in decimal base, what is it in binary base?
Answer: ^CTraceback (most recent call last):
  File "/home/dena-picoctf/convertme/convertme.py", line 23, in <module>
    ans = input('Answer: ')
KeyboardInterrupt

dena-picoctf@webshell:~/convertme$ python3 convertme.py
If 63 is in decimal base, what is it in binary base?
Answer: 64
That isn't a binary number. Binary numbers contain only 1's and 0's
dena-picoctf@webshell:~/convertme$ python3 convertme.py
If 83 is in decimal base, what is it in binary base?
Answer: 1001010
74 and 83 are not equal.
dena-picoctf@webshell:~/convertme$ python3 convertme.py
If 87 is in decimal base, what is it in binary base?
Answer: 1010111
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
dena-picoctf@webshell:~/convertme$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=87
