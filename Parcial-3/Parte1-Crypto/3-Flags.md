# Flags
## Objetivo
What do the [flags](https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png) mean?
## Pistas
P1: The flag is in the format PICOCTF{}

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: PICOCT{F1AG5AND5TUFF}
-----------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/3]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png
--2023-11-13 16:49:48--  https://jupiter.challenges.picoctf.org/static/fbeb5f9040d62b18878d199cdda2d253/flag.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43257 (42K) [application/octet-stream]
Saving to: ‘flag.png’

flag.png                     100%[==============================================>]  42.24K  --.-KB/s    in 0.004s  

2023-11-13 16:49:49 (11.2 MB/s) - ‘flag.png’ saved [43257/43257]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/3]
└─$ file flag.png 
flag.png: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/3]
└─$ open flag.png 
-----------------------------------------------------------------------------
En la pagina acomodamos el orden de la imagen las banderas lo que nos da 
PICOCT{F1AG5AND5TUFF}


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://en.wikipedia.org/wiki/Flag_semaphore
https://en.wikipedia.org/wiki/International_maritime_signal_flags
https://shorelinesillustrated.com/nautical-flags-guide/

https://www.dcode.fr/maritime-signals-code
