# shark-on-wire-2
## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
## Pistas

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{p1LLf3r3d_data_v1a_st3g0}
------------------------------------------------------------------------
DESCARGAMOS EL ARCHIVO 

USANDO WHITESHARK SELECCIONAMOS EL UDP Y BUSCAMOS LA BANDERA CODIFICADA UBICATE EN START
EN EL 60 ESTA EL END, ESTABLECEMOS UN FILTRO UDP PORT 22


creamos un script para sacar la bandera 

from scapy.all import * 

packets = rdpcap('capture.pcap')

flag= ''

for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)


──(kali㉿kali)-[~/Downloads/forensic2/wireshark]
└─$ python3 exp.py
  File "/home/kali/Downloads/forensic2/wireshark/exp.py", line 9
    if p[UDP].sport > 5000
                          ^
SyntaxError: expected ':'
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2/wireshark]
└─$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2/wireshark]
└─$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://scapy.readthedocs.io/en/latest/introduction.html
