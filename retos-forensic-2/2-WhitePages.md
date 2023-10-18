# WhitePages
## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
## Pistas
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}
------------------------------------------------------------------------------
──(kali㉿kali)-[~/Downloads/forensic2]
└─$ wget https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
--2023-10-18 12:50:48--  https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2982 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt                            100%[====================================================================================>]   2.91K  --.-KB/s    in 0s      

2023-10-18 12:51:01 (20.0 MB/s) - ‘whitepages.txt’ saved [2982/2982]

                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2]
└─$ ls    
img.jpg  message.wav  whitepages.txt
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2]
└─$ file whitepages.txt 
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2]
└─$ 

abrimos el archivo con el editor de texto y reemplazamos los dos tipos de espacios con 0 y 1 respectivamente

ahora se copia ese texto y lo ponemos en cyberchef
lo que nos da picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://es.wikipedia.org/wiki/UTF-8
https://gchq.github.io/CyberChef/