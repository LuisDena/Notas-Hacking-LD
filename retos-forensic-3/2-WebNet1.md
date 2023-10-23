# WebNet1
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Pistas
P1:Try using a tool like Wireshark.
P2:How can you decrypt the TLS stream?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{honey.roasted.peanuts}
----------------------------------------------------------------
similar al anterior
usando wireshark para desencriptar el pcap de TLS haciendo uso de la key

cargando a en edicion-preferencias-protocolos-tls y ponemrs la llave rsa la agregamos y ahora buscamos la imagen que se esta descargando (vulture) y da descargamos con file-export object-http-image y la examinamos
---------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ cd Downloads    
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ cd forensic3/        
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3]
└─$ mkdir webnet1
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3]
└─$ cd webnet1   
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
--2023-10-22 19:59:17--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                              100%[===================================================================================>]  90.36K   430KB/s    in 0.2s    

2023-10-22 19:59:18 (430 KB/s) - ‘capture.pcap’ saved [92525/92525]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
--2023-10-22 19:59:33--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key                              100%[===================================================================================>]   1.66K  --.-KB/s    in 0s      

2023-10-22 19:59:34 (15.7 MB/s) - ‘picopico.key’ saved [1704/1704]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ wireshark capture.pcap                                                                          
 ** (wireshark:7362) 20:01:20.365237 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
 ** (wireshark:7362) 20:01:34.736044 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 7801, resource id: 21034609, major code: 40 (TranslateCoords), minor code: 0
^C
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ open vulture.jpg 

┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ strings vulture.jpg -n15            
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/forensic3/webnet1]
└─$ 
-------------------------------------------
se puede hacer directamente en wireshark pero te da una flag falsa


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.cloudflare.com/es-es/learning/ssl/transport-layer-security-tls/