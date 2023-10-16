# SharkOnWire
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Pistas
P1: Try using a tool like Wireshark
P2: What are streams?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{StaT31355_636f6e6e}
-------------------------------------------------
Descargamos la imagen con wget y hacemos uso de wireshark 

┌──(kali㉿kali)-[~/Downloads]
└─$ wget https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap 
--2023-10-16 12:22:17--  https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap                              100%[===================================================================================>] 233.84K   145KB/s    in 1.6s    

2023-10-16 12:22:33 (145 KB/s) - ‘capture.pcap’ saved [239455/239455]

Dentro del wireshark,abrimos el archivo y buscamos aquella que tenga la extension UDP
e intentamos decodificar subiendo el stream level

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
