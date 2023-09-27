# Static ain't always noise
## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static)? This [BASH script](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh) might help!

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{d15a5m_t34s3r_ae0b3ef2}
---------------------------------------------------------
dena-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static
dena-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh
dena-picoctf@webshell:~$ ls -la
total 52
drwxr-xr-x 2 dena-picoctf dena-picoctf   142 Sep 25 17:07 .
drwxr-xr-x 3 root         root            26 Sep 25 16:30 ..
-rw------- 1 dena-picoctf dena-picoctf   496 Sep 25 16:57 .bash_history
-rw-r--r-- 1 dena-picoctf dena-picoctf   220 Sep 25 16:30 .bash_logout
-rw-r--r-- 1 dena-picoctf dena-picoctf  3771 Sep 25 16:30 .bashrc
-rw-r--r-- 1 dena-picoctf dena-picoctf   807 Sep 25 16:30 .profile
-rw-rw-r-- 1 dena-picoctf dena-picoctf   167 Sep 25 16:33 .wget-hsts
-rw-r--r-- 1 root         root          4443 Sep 25 16:58 README.txt
-rw-rw-r-- 1 dena-picoctf dena-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 dena-picoctf dena-picoctf 10936 Mar 16  2021 warm.1
dena-picoctf@webshell:~$ 
dena-picoctf@webshell:~$ file static 
static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=7eb9ee1907cc878f15f9949988893b1f0ab1ebdf, not stripped
dena-picoctf@webshell:~$ chmod +x static 
dena-picoctf@webshell:~$ ls
README.txt  static  warm.1
dena-picoctf@webshell:~$ ./static 
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
dena-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_ae0b3ef2}
dena-picoctf@webshell:~$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| strings | siempre hacerlo por si acaso |
| grep | pico (mas facil) |

## Referencias 
