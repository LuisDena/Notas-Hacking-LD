#  Vigenere
## Objetivo
Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/160/cipher.txt) using this key "CYLAB".
## Pistas
P1: https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}
--------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/2]
└─$ wget https://artifacts.picoctf.net/c/160/cipher.txt 
--2023-11-13 16:46:49--  https://artifacts.picoctf.net/c/160/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.104, 18.154.144.103, 18.154.144.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.104|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt                   100%[==============================================>]      43  --.-KB/s    in 0s      

2023-11-13 16:46:50 (18.5 MB/s) - ‘cipher.txt’ saved [43/43]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/2]
└─$ cat cipher.txt 
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/2]
└─$ 
--------------------------------------------------------------------------------------
LLevamos ese texto al cyberchef y con la key lo decodificamos sando Vigenere decode
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('CYLAB')&input=cmdub0RWRHtPME5VX1dRM19HMUczTzNUM19BMUFIM1NfMjk1MWM4OWZ9DQo