# What-Lies-Within
## Objetivo
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Pistas
P1: There is data encoded somewhere... there might be an online decoder.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{h1d1ng_1n_th3_b1t5}
-----------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
--2023-10-16 12:32:14--  https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 625219 (611K) [application/octet-stream]
Saving to: ‘buildings.png’

buildings.png                             100%[===================================================================================>] 610.57K   245KB/s    in 2.5s    

2023-10-16 12:32:25 (245 KB/s) - ‘buildings.png’ saved [625219/625219]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ sudo gem install zsteg    
[sudo] password for kali: 
Fetching zsteg-0.2.13.gem
Fetching rainbow-3.1.1.gem
Fetching iostruct-0.0.5.gem
Fetching zpng-0.4.5.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.0.5
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.0.5
Installing ri documentation for iostruct-0.0.5
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 2 seconds
4 gems installed
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://wiki.bi0s.in/steganography/zsteg/