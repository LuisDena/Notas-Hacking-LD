# Easy1
## Objetivo
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.
## Pistas
P1: Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
P2: Please use all caps for the message.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{CRYPTOISFUN}
------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ cd ..     
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ mkdir easy-1 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ cd easy-1 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/easy-1]
└─$ wget https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt      
--2023-10-24 21:03:22--  https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1571 (1.5K) [application/octet-stream]
Saving to: ‘table.txt’

table.txt                                 100%[===================================================================================>]   1.53K  --.-KB/s    in 0s      

2023-10-24 21:03:23 (23.8 MB/s) - ‘table.txt’ saved [1571/1571]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/easy-1]
└─$ open table.txt 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/easy-1]
└─$ [8748:1024/210638.319915:ERROR:object_proxy.cc(590)] Failed to call method: org.freedesktop.portal.Settings.Read: object_path= /org/freedesktop/portal/desktop: org.freedesktop.DBus.Error.UnknownMethod: No such interface “org.freedesktop.portal.Settings” on object at path /org/freedesktop/portal/desktop
libva error: vaGetDriverNameByIndex() failed with unknown libva error, driver_name = (null)
[main 2023-10-25T01:06:40.834Z] update#setState idle
[main 2023-10-25T01:07:10.920Z] update#setState checking for updates
[main 2023-10-25T01:07:11.098Z] update#setState idle


con la tabla y los valores otorgado hacemos la conversion siguiendo la tabla de vigenere
de forma manual o bien meterlo al cyberchef 

LO QUE NOS DA picoCTF{CRYPTOISFUN}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://es.wikipedia.org/wiki/Libreta_de_un_solo_uso
https://www.ugr.es/~anillos/textos/pdf/2012/EXPO-1.Criptografia/02a11.htm#:~:text=El%20cifrado%20Vigen%C3%A8re%20es%20un,se%20ha%20reinventado%20muchas%20veces.
https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkIg