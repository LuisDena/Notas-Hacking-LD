# Packets Primer
## Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)
## Pistas
P1:Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{p4ck37_5h4rk_01b0a0d6}
--------------------------------------------------------------------------
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ wget https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
--2023-10-29 01:48:57--  https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.103, 18.154.144.85, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 778 [application/octet-stream]
Saving to: ‘network-dump.flag.pcap’

network-dump.flag.pcap                    100%[===================================================================================>]     778  --.-KB/s    in 0s      

2023-10-29 01:48:57 (8.55 MB/s) - ‘network-dump.flag.pcap’ saved [778/778]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ wireshark network-dump.flag.pcap             

--------------------------------------------------------------
en el wireshark le damos a seguir tcp stream y nos da
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
