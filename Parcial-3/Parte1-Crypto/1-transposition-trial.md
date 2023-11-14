# transposition-trial
## Objetivo
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/191/message.txt).
## Pistas
P1: Split the message up into blocks of 3 and see how the first block is scrambled

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
--------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1]
└─$ cd 1      
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ wget https://artifacts.picoctf.net/c/191/message.txt                                      
--2023-11-13 16:37:56--  https://artifacts.picoctf.net/c/191/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.103, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 54 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                  100%[==============================================>]      54  --.-KB/s    in 0s      

2023-11-13 16:37:57 (23.4 MB/s) - ‘message.txt’ saved [54/54]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ ls -la                                     
total 12
drwxr-xr-x 2 kali kali 4096 Nov 13 16:37 .
drwxr-xr-x 7 kali kali 4096 Nov 13 16:37 ..
-rw-r--r-- 1 kali kali   54 Mar 15  2023 message.txt
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ open message.txt 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ [2798:1113/163904.418653:ERROR:object_proxy.cc(590)] Failed to call method: org.freedesktop.DBus.StartServiceByName: object_path= /org/freedesktop/DBus: org.freedesktop.DBus.Error.NoReply: Did not receive a reply. Possible causes include: the remote application did not send a reply, the message bus security policy blocked the reply, the reply timeout expired, or the network connection was broken.
[2798:1113/163904.778742:ERROR:object_proxy.cc(590)] Failed to call method: org.freedesktop.portal.Settings.Read: object_path= /org/freedesktop/portal/desktop: org.freedesktop.DBus.Error.UnknownMethod: No such interface “org.freedesktop.portal.Settings” on object at path /org/freedesktop/portal/desktop
libva error: vaGetDriverNameByIndex() failed with unknown libva error, driver_name = (null)
[main 2023-11-13T21:39:07.009Z] update#setState idle
[main 2023-11-13T21:39:14.567Z] Blocked vscode-file request vscode-file://vscode-app/usr/share/code/resources/app/out/vs/editor/common/services/editorSimpleWorker.nls.js
[main 2023-11-13T21:39:15.735Z] Extension host with pid 3104 exited with code: 0, signal: unknown.

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ cat message.txt 
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V6E5926A}4                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/1]
└─$ 

----------------------------------------------------------------------------------------
Dentro de la pagina nos deja mover las columnas generadas, movemos la tercera la posicion de la primera y así se decodifica

The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://tholman.com/other/transposition/