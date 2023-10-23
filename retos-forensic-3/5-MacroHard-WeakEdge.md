# MacroHard-WeakEdge
## Objetivo
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics%20is%20fun.pptm)
## Pistas


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
----------------------------------------------------------------------------
lo descargamos y extraemos como siempre hemos hecho(se me olvido copiarlo)

-------------------------------------------
descargamos visual studio
┌──(kali㉿kali)-[~]
└─$ cd Downloads          
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ ls -la
total 238624
drwxr-xr-x 11 kali kali      4096 Oct 22 20:52 .
drwx------ 21 kali kali      4096 Oct 22 20:52 ..
-rw-r--r--  1 kali kali  95652786 Oct 22 20:52 code_1.83.1-1696982868_amd64.deb
-rw-r--r--  1 kali kali   2412544 Oct  5 10:18 DeepSoundSetup.msi
drwxr-xr-x  2 kali kali      4096 Oct  4 18:12 FC
drwxr-xr-x  2 kali kali      4096 Oct 16 12:32 forensic
drwxr-xr-x  2 kali kali      4096 Oct 18 12:10 forensic-2
drwxr-xr-x  5 kali kali      4096 Oct 18 17:31 forensic2
drwxr-xr-x  7 kali kali      4096 Oct 22 20:31 forensic3
drwxr-xr-x  2 kali kali      4096 Oct  4 19:33 mfa
-rwxr-xr-x  1 kali kali 105411110 Sep 23 15:26 Obsidian-1.4.13.AppImage
drwxr-xr-x  2 kali kali      4096 Oct  4 19:38 pci
-rw-r--r--  1 kali kali      6192 Oct  4 18:36 securitynews.zip
drwxr-xr-x  2 kali kali      4096 Oct  4 18:41 sn
-rwxr-xr-x  1 kali kali  40814520 Oct  4 18:56 SonicVisualiser-4.5.2-x86_64.AppImage
drwxr-xr-x  2 kali kali      4096 Oct  5 12:14 tt1
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ sudo dpkg -i code_1.83.1-1696982868_amd64.deb 
[sudo] password for kali: 
Selecting previously unselected package code.
(Reading database ... 436327 files and directories currently installed.)
Preparing to unpack code_1.83.1-1696982868_amd64.deb ...
Unpacking code (1.83.1-1696982868) ...
Setting up code (1.83.1-1696982868) ...
Processing triggers for desktop-file-utils (0.26-1) ...
Processing triggers for mailcap (3.70+nmu1) ...
Processing triggers for shared-mime-info (2.2-1) ...
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ 
------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ cd Downloads/forensic3/mhwe/
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ ls /la
ls: cannot access '/la': No such file or directory
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ ls -la
total 132
drwxr-xr-x 5 kali kali   4096 Oct 22 20:33  .
drwxr-xr-x 7 kali kali   4096 Oct 22 20:31  ..
-rw-r--r-- 1 kali kali  10660 Jan  1  1980 '[Content_Types].xml'
drwxr-xr-x 2 kali kali   4096 Oct 22 20:33  docProps
-rw-r--r-- 1 kali kali 100093 Mar 23  2021 'Forensics is fun.pptm'
drwxr-xr-x 7 kali kali   4096 Oct 22 20:33  ppt
drwxr-xr-x 2 kali kali   4096 Oct 22 20:33  _rels
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ code .                      

exploramos las carpetas y buscamos el hidden en ppt-slide-masters-


┌──(kali㉿kali)-[~]
└─$ cd Downloads/forensic3/mhwe/
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ ls /la
ls: cannot access '/la': No such file or directory
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ ls -la
total 132
drwxr-xr-x 5 kali kali   4096 Oct 22 20:33  .
drwxr-xr-x 7 kali kali   4096 Oct 22 20:31  ..
-rw-r--r-- 1 kali kali  10660 Jan  1  1980 '[Content_Types].xml'
drwxr-xr-x 2 kali kali   4096 Oct 22 20:33  docProps
-rw-r--r-- 1 kali kali 100093 Mar 23  2021 'Forensics is fun.pptm'
drwxr-xr-x 7 kali kali   4096 Oct 22 20:33  ppt
drwxr-xr-x 2 kali kali   4096 Oct 22 20:33  _rels
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ code .                      
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " "
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic3/mhwe]
└─$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://docs.fileformat.com/presentation/pptm/