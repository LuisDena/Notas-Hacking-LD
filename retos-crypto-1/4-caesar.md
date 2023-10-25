# caesar
## Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).
## Pistas
P1:caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{crossingtherubiconvfhsjkou}
---------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads]
└─$ cd crypto-1 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ mkdir ceasar  
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1]
└─$ cd ceasar  
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
--2023-10-24 21:29:52--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                                100%[===================================================================================>]      35  --.-KB/s    in 0s      

2023-10-24 21:29:53 (20.1 MB/s) - ‘ciphertext’ saved [35/35]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ cat ciphertext            
picoCTF{ynkooejcpdanqxeykjrbdofgkq}                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ 


haciendo uso de cyberchef 
con python
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ cat ciphertext            
picoCTF{ynkooejcpdanqxeykjrbdofgkq}                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ python3 exp.py                
abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ python3 exp.py
ynkooejcpdanqxeykjrbdofgkq
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ python3 exp.py
  File "/home/kali/Downloads/crypto-1/ceasar/exp.py", line 14
    print salida
    ^^^^^^^^^^^^
SyntaxError: Missing parentheses in call to 'print'. Did you mean print(...)?
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ python3 exp.py
crossingtherubiconvfhsjkou
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-1/ceasar]
└─$ 

el exploit

import string
import re

abc=string.ascii_letters

encriptado = open('ciphertext','r').read()
encriptado = re.findall('\{(.*?)\}',encriptado)[0]


rot=30
salida = ''
for car in encriptado:
        salida+=abc[(abc.find(car)+rot)%26]
print (salida)




```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://privacycanada.net/classical-encryption/caesar-cipher/