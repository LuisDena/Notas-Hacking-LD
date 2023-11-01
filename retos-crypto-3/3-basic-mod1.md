# basic-mod1
## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/128/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Pistas
P1: Do you know what `mod 37` means?
P2: `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{R0UND_N_R0UND_B6B25531}
--------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ code .
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ wget https://artifacts.picoctf.net/c/128/message.txt                                   
--2023-11-01 12:54:08--  https://artifacts.picoctf.net/c/128/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.34, 18.160.124.108, 18.160.124.119, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.34|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 84 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                  100%[==============================================>]      84  --.-KB/s    in 0s      

2023-11-01 12:54:37 (42.5 MB/s) - ‘message.txt’ saved [84/84]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ cat message.txt 
165 248 94 346 299 73 198 221 313 137 205 87 336 110 186 69 223 213 216 216 177 138                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ python3 exp.py
R
U
N
D
N
R
U
N
D
B
B
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ python3 exp.py
R
0
U
N
D
N
R
0
U
N
D
B
6
B
2
5
5
3
1
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ python3 exp.py
R0UND_N_R0UND_B6B25531
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ python3 exp.py
picoCTF{R0UND_N_R0UND_B6B25531}
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/3]
└─$ 
-------------------------------- el script -------------------------------------
f = open('message.txt').read().split()

flag = ''

for c in f :

i = int(c) % 37

if i>=0 and i <=25:

flag+= (chr(i + 65))

elif i >=26 and i <=35:

flag+= (chr(i+22))

else:

flag+= ("_")

print(f"picoCTF{{{flag}}}")
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
