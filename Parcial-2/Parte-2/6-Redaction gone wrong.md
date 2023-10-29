#  Redaction gone wrong
## Objetivo
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Pistas
P1:How can you be sure of the redaction?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{C4n_Y0u_S33_m3_fully}
--------------------------------------------------------------------------
┌──(kali㉿kali)-[~]
└─$ cd Downloads/Parcial_Parte2 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
--2023-10-29 01:51:35--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.107, 18.154.144.85, 18.154.144.103, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.107|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs.pdf         100%[===================================================================================>]  34.10K  --.-KB/s    in 0.07s   

2023-10-29 01:51:35 (505 KB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/Parcial_Parte2]
└─$ open Financial_Report_for_ABC_Labs.pdf 
                                                                                                                                                                      
--------------------------------------------------------------------------
Abrimos el pdf copiamos y pegamos el contenido
-----------------------------------------------
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
