# Lookey here
## Objetivo
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/126/anthem.flag.txt).
## Pistas
P1: Download the file and search for the flag based on the known prefix.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{gr3p_15_@w3s0m3_2116b979}
----------------------------------------------------------------------
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ wget https://artifacts.picoctf.net/c/126/anthem.flag.txt 
--2023-10-29 01:46:59--  https://artifacts.picoctf.net/c/126/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.104, 18.154.144.103, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.txt                           100%[===================================================================================>] 106.12K  --.-KB/s    in 0.1s    

2023-10-29 01:47:00 (815 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ ls    
anthem.flag.txt  cat.jpg  drawing.flag.svg  shark1.pcapng
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ strings anthem.flag.txt | grep pico                  
      we think that the men of picoCTF{gr3p_15_@w3s0m3_2116b979}
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
