# Pixelated

## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png)
## Pistas
P1: [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
P2: Think of different ways you can "stack" images

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{d562333d}
--------------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/crypto-3]
└─$ mkdir 2       
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3]
└─$ cd 2 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ wget https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png
--2023-11-01 12:25:02--  https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197176 (193K) [application/octet-stream]
Saving to: ‘scrambled1.png’

scrambled1.png                100%[==============================================>] 192.55K   846KB/s    in 0.2s    

2023-11-01 12:25:17 (846 KB/s) - ‘scrambled1.png’ saved [197176/197176]

                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ wget https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png
--2023-11-01 12:25:26--  https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197174 (193K) [application/octet-stream]
Saving to: ‘scrambled2.png’

scrambled2.png                100%[==============================================>] 192.55K   335KB/s    in 0.6s    

2023-11-01 12:25:29 (335 KB/s) - ‘scrambled2.png’ saved [197174/197174]

                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ ls -la 
total 400
drwxr-xr-x 2 kali kali   4096 Nov  1 12:25 .
drwxr-xr-x 5 kali kali   4096 Nov  1 12:24 ..
-rw-r--r-- 1 kali kali 197176 Mar 15  2021 scrambled1.png
-rw-r--r-- 1 kali kali 197174 Mar 15  2021 scrambled2.png
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ convert scrambled1.png scrambled2.png -compose Add -c composite todo.png
convert-im6.q16: unrecognized option `-c' @ error/convert.c/ConvertImageCommand/1166.
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ convert scrambled1.png scrambled2.png -compose Add -composite todo.png 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$ open todo.png 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/2]
└─$                        


------------------------------------------------otro modo
el exploit

from PIL import image

import numpy as np

  

imagen1 = np.asarray(Image.open('scrambled1.png'))

  

imagen2 = np.asarray(Image.open('scrambled2.png'))

  

data = imagen1 + imagen2

  

print(data)

  

nueva = Image.fromarray(data)

nueva.save('lachida.png','PNG')

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://imagemagick.org/index.php
https://pypi.org/project/Pillow/
https://numpy.org/