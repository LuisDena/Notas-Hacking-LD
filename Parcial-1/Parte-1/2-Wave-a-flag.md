# Wave-A-Flag
## Objetivo

## Datos de acceso al nivel
```bash
Usuario: Dena 
Contraseña: notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
----------------------------------------------------------
dena-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
--2023-09-25 16:50:43--  https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm.1'

warm.1                  100%[============================>]  10.68K  --.-KB/s    in 0s      

2023-09-25 16:50:43 (314 MB/s) - 'warm.1' saved [10936/10936]

dena-picoctf@webshell:~$ chmod +x warm
dena-picoctf@webshell:~$ /.warm
-bash: /.warm: No such file or directory
dena-picoctf@webshell:~$ /. warm
-bash: /.: Is a directory
dena-picoctf@webshell:~$ ls -la
total 60
drwxr-xr-x 2 dena-picoctf dena-picoctf   166 Sep 25 16:50 .
drwxr-xr-x 3 root         root            26 Sep 25 16:30 ..
-rw------- 1 dena-picoctf dena-picoctf   263 Sep 25 16:44 .bash_history
-rw-r--r-- 1 dena-picoctf dena-picoctf   220 Sep 25 16:30 .bash_logout
-rw-r--r-- 1 dena-picoctf dena-picoctf  3771 Sep 25 16:30 .bashrc
-rw-r--r-- 1 dena-picoctf dena-picoctf   807 Sep 25 16:30 .profile
-rw-rw-r-- 1 dena-picoctf dena-picoctf   167 Sep 25 16:33 .wget-hsts
-rw-r--r-- 1 root         root          4443 Sep 25 16:45 README.txt
-rw-rw-r-- 1 dena-picoctf dena-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 dena-picoctf dena-picoctf    34 Mar 16  2021 flag.1
-rwxrwxr-x 1 dena-picoctf dena-picoctf 10936 Mar 16  2021 warm
-rw-rw-r-- 1 dena-picoctf dena-picoctf 10936 Mar 16  2021 warm.1
dena-picoctf@webshell:~$ /warm
-bash: /warm: No such file or directory
dena-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
dena-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| wget | descargar de internet con el enlace |

## Referencias 
