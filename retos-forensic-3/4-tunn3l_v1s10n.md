# tunn3l_v1s10n
## Objetivo
We found this [file](https://mercury.picoctf.net/static/21c07c9dd20cd9f2459a0ae75d99af6e/tunn3l_v1s10n). Recover the flag.
## Pistas
P1: Weird that it won't display right...
P2:

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{qu1t3_a_v13w_2020}
--------------------------------------------
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3]
└─$ mkdir tunel_vision  
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3]
└─$ cd tunel_vision       
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ wget https://mercury.picoctf.net/static/21c07c9dd20cd9f2459a0ae75d99af6e/tunn3l_v1s10n
--2023-10-22 20:17:14--  https://mercury.picoctf.net/static/21c07c9dd20cd9f2459a0ae75d99af6e/tunn3l_v1s10n
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n                             100%[===================================================================================>]   2.76M  2.20MB/s    in 1.3s    

2023-10-22 20:17:16 (2.20 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ file tunn3l_v1s10n 
tunn3l_v1s10n: data
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ xxd tunn3l_v1s10n | head 
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333 2a26 382c 2836 2b27 392d 2b2f  0'#3*&8,(6+'9-+/
00000070: 2623 1d12 0e23 1711 2916 0e55 3d31 9776  &#...#..)..U=1.v
00000080: 668b 6652 996d 569e 7058 9e6f 549c 6f54  f.fR.mV.pX.oT.oT
00000090: ab7e 63ba 8c6d bd8a 69c8 9771 c193 71c1  .~c..m..i..q..q.

┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ xxd tunn3l_v1s10n | head                                           
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333 2a26 382c 2836 2b27 392d 2b2f  0'#3*&8,(6+'9-+/
00000070: 2623 1d12 0e23 1711 2916 0e55 3d31 9776  &#...#..)..U=1.v
00000080: 668b 6652 996d 569e 7058 9e6f 549c 6f54  f.fR.mV.pX.oT.oT
00000090: ab7e 63ba 8c6d bd8a 69c8 9771 c193 71c1  .~c..m..i..q..q.
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ open tunn3l_v1s10n 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ mv tunn3l_v1s10n tunn3l_v1s10n.bmp 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ open tunn3l_v1s10n.bmp 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ hexeditor tunn3l_v1s10n.bmp 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ open tunn3l_v1s10n.bmp 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ exiftool tunn3l_v1s10n.bmp                   
ExifTool Version Number         : 12.65
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:10:22 20:26:14-04:00
File Access Date/Time           : 2023:10:22 20:26:21-04:00
File Inode Change Date/Time     : 2023:10:22 20:26:14-04:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 12.65
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:10:22 20:28:06-04:00
File Access Date/Time           : 2023:10:22 20:26:21-04:00
File Inode Change Date/Time     : 2023:10:22 20:28:06-04:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 320
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x320
Megapixels                      : 0.363
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 12.65
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2023:10:22 20:28:44-04:00
File Access Date/Time           : 2023:10:22 20:28:12-04:00
File Inode Change Date/Time     : 2023:10:22 20:28:44-04:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 1088
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x1088
Megapixels                      : 1.2
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ open tunn3l_v1s10n.bmp     
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/tunel_vision]
└─$ 


Usamos hex editor y con ctrl+t buscamos 0E y la ajustamos a 28 que sería 40 bytes para corregir el encabezado segun las especificaciones hacemos lo mismo para el 0A y lo ajustamos y ya una vez se pueda abrir ajustamos ahora la altura de la imagen en donde corresponde 12 y abrimos la imagen y copiamos la flag que sería 
picoCTF{qu1t3_a_v13w_2020}

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://en.wikipedia.org/wiki/List_of_file_signatures
https://en.wikipedia.org/wiki/BMP_file_formatx|