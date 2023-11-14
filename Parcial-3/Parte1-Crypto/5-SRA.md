# SRA
## Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.
## Pistas


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:

-

-
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/5]
└─$ python3 exp.py
[+] Opening connection to saturn.picoctf.net on port 54906: Done
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:23: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 38466986707375721520563549161076044532047684563431751385492509417701486757415
d= 23961818805940889773561741783809005420315690919875924167865955840491701179713
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:30: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  1570385719084948093089915871285490788231229435815908442189431147918304620214850880
[2, 2, 2, 2, 2, 2, 3, 3, 3, 5, 19, 31, 101, 733, 38993, 43093, 12741397, 316794896233, 42342930338699, 14513843583406599313239920941]
{292716541849173422389782099237485509321, 297391769575946306911015461062200950103, 173765696506380383736578267405980887521, 316224559687467221201558393117999726671, 275170844921024108273636777169347130577, 198261179717297537940676974041467300069}
m5zV1K557xS1VDcm
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:56: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> m5zV1K557xS1VDcm\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_dd808298}\r\n'
m5zV1K557xS1VDcm
[*] Closed connection to saturn.picoctf.net port 54906
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/5]
└─$ 
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/5]
└─$ python3 exp.py
[+] Opening connection to saturn.picoctf.net on port 54906: Done
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:23: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 38466986707375721520563549161076044532047684563431751385492509417701486757415
d= 23961818805940889773561741783809005420315690919875924167865955840491701179713
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:30: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  1570385719084948093089915871285490788231229435815908442189431147918304620214850880
[2, 2, 2, 2, 2, 2, 3, 3, 3, 5, 19, 31, 101, 733, 38993, 43093, 12741397, 316794896233, 42342930338699, 14513843583406599313239920941]
{292716541849173422389782099237485509321, 297391769575946306911015461062200950103, 173765696506380383736578267405980887521, 316224559687467221201558393117999726671, 275170844921024108273636777169347130577, 198261179717297537940676974041467300069}
m5zV1K557xS1VDcm
/home/kali/Downloads/Parcial-3/Parte-1/5/exp.py:56: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> m5zV1K557xS1VDcm\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_dd808298}\r\n'
m5zV1K557xS1VDcm
[*] Closed connection to saturn.picoctf.net port 54906
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/5]
└─$ 
--------------------------------------------
from pwn import *

import primefac

from itertools import combinations

from Crypto.Util.number import long_to_bytes

  

def sub_lists (l):

comb = []

  

#Iterating till length of list

for i in range(1,len(l)+1):

comb += [list(j) for j in combinations(l, i)]

return comb

  

def divisors(phi):

print("Give me the divisors of ", phi-1)

return(eval(input()))

  
  

r = remote('saturn.picoctf.net', 54906)

  

r.recvuntil("anger =")

ciphertext=int(r.recvline())

  

r.recvuntil("envy =")

d=int(r.recvline())

print("cipher=",ciphertext)

print("d=",d)

print(r.recvuntil("vainglory?"))

r.recvline()

  

factors=divisors(d*65537)

combos = sub_lists(factors)

primes = set()

  

for l in combos:

product = 1

  

for k in l:

product = product * k

if product.bit_length()==128 and primefac.isprime(product+1):

primes.add(product+1)

print(primes)

primelist = list(primes)

  

for p in primelist:

for q in primelist:

n=p*q

  

plain = pow(ciphertext,d,n)

try:

plaintext = long_to_bytes(plain)

  

print(plaintext.decode())

r.sendline(plaintext.decode())

print(r.recvline())

print(r.recvline())

print(r.recvline())

except:

continue
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.dcode.fr/prime-factors-decomposition
