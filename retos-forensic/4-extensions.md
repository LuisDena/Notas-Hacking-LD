# extensions
## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Pistas
P1: How do operating systems know what kind of file it is? (It's not just the ending!
P2: Make sure to submit the flag as picoCTF{XXXXX} 

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{now_you_know_about_extensions}
----------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt    
--2023-10-16 12:28:36--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt                                  100%[===================================================================================>]   9.75K  --.-KB/s    in 0s      

2023-10-16 12:28:44 (122 MB/s) - ‘flag.txt’ saved [9984/9984]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ ls
flag.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ file flag.txt 
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ mv flag.txt  flag-png          
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ mv flag.txt  flag.png
mv: cannot stat 'flag.txt': No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ mv flag-png  flag.png
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ ls
flag.png
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$              
-------------------------------
Abrimos la imagen y nos da la flag
picoCTF{now_you_know_about_extensions}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
