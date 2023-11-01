# HideToSee
## Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/238/atbash.jpg).
## Pistas
P1: Download the image and try to extract it.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{atbash_crack_8a0feddc}
------------------------------------------------------------------------------------
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ ls -la
total 60
drwxr-xr-x 2 kali kali  4096 Nov  1 13:11 .
drwxr-xr-x 8 kali kali  4096 Nov  1 13:11 ..
-rw-r--r-- 1 kali kali 51497 Mar 15  2023 atbash.jpg
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ open atbash.jpg 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ sudo apt install steghide          
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
steghide is already the newest version (0.5.1-15).
The following packages were automatically installed and are no longer required:
  gcc-12-base graphicsmagick libarmadillo11 libcodec2-1.1 libgcc-12-dev libgfapi0 libgfrpc0 libgfxdr0 libglusterfs0
  libgraphicsmagick-q16-3 libgupnp-igd-1.0-4 libjim0.81 libnfs13 libobjc-12-dev libstdc++-12-dev python3-jdcal
Use 'sudo apt autoremove' to remove them.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ steghide --extract -sf atbash.jpg  
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_8z0uvwwx}
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/4]
└─$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfOHowdXZ3d3h9