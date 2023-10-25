# The Numbers
## Objetivo
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?
## Pistas
P1: The flag is in the format PICOCTF{}
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{thenumbersmason}
--------------------------------------------------------------------
──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ mkdir Numbers 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ cd Numbers 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
--2023-10-24 20:54:51--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.png                           100%[===================================================================================>]  98.36K  --.-KB/s    in 0.1s    

2023-10-24 20:54:52 (793 KB/s) - ‘the_numbers.png’ saved [100721/100721]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ ls    
the_numbers.png
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ file the_numbers.png                 
the_numbers.png: PNG image data, 774 x 433, 8-bit/color RGB, non-interlaced
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ open the_numbers.png 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/Numbers]
└─$ 
-------------------------------------------------------------------------
Vemos la imagen y asumiendo que la bandera empieza con picoCTF nos quedaría
 p  i  c  o  C  T  F {T } 
 16 9  3  15 3  20 6
por lo que podemos asumir que es por numero de alfabeto por lo que lo metemos al cyberchef

lo que nos da picoCTF{thenumbersmason}

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://gchq.github.io/CyberChef/#recipe=A1Z26_Cipher_Decode('Space')&input=MTYgOSAzIDE1IDMgMjAgNiB7IDIwIDggNSAxNCAyMSAxMyAyIDUgMTggMTkgMTMgMSAxOSAxNSAxNCB9