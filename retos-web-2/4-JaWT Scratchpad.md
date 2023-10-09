# JaWT Scratchpad
## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Pistas
P1:Internal server errors can be intentionally returned by this challenge. If you experience one, try clearing your cookies.
P2:What is that cookie?
P3:Have you heard of JWT?
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{jawt_was_just_what_you_thought_44c752f5}
---------------------------------------
con cookie editor vemos el jwt en busca de la cookie

con el valor
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSm9lIn0.V7H66QozpyaAHo2QPSny-C3lIKjifq1y8y2MApY-mno

cambio el user que use "Joe" en el debuger, por admin copio el jwt codificado y lo pego en la cookie 

recargamos la pagina y da error por lo que tenemos que crakear la contraseña secreta para obtener la firma jwt

tenemos que crakearla con lo que nos indica que es 
JWT HS256

usando john

┌──(kali㉿kali)-[~/Downloads]
└─$ sudo gzip /usr/share/wordlists/rockyou.txt.gz 
gzip: /usr/share/wordlists/rockyou.txt.gz: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
┌──(kali㉿kali)-[~/Downloads]
└─$ ls /usr/share/wordlists                            
amass  dirb  dirbuster  fasttrack.txt  fern-wifi  john.lst  legion  metasploit  nmap.lst  rockyou.txt  sqlmap.txt  wfuzz  wifite.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ john pass.txt -w=/usr/share/wordlists/rockyou.txt 
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:03 25.35% (ETA: 15:11:35) 0g/s 1262Kp/s 1262Kc/s 1262KC/s shell7737..sheenyboy1
0g 0:00:00:04 34.72% (ETA: 15:11:35) 0g/s 1273Kp/s 1273Kc/s 1273KC/s newpats12..new14uu11
0g 0:00:00:05 43.34% (ETA: 15:11:35) 0g/s 1258Kp/s 1258Kc/s 1258KC/s laviniger9..laurentiumo
ilovepico        (?)     
1g 0:00:00:05 DONE (2023-10-09 15:11) 0.1697g/s 1255Kp/s 1255Kc/s 1255KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably

le cambiamos la firma 

copiamos el resultado, y lo pegamos con cookie editor

picoCTF{jawt_was_just_what_you_thought_44c752f5}


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://jwt.io/introduction
https://jwt.io/#debugger-io
https://github.com/openwall/john