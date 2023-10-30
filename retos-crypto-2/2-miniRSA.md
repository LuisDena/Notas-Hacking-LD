# miniRSA
## Objetivo
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext)? Something seems a bit small.
## Pistas
P1: RSA [tutorial](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
P2: How could having too small an e affect the security of this 2048 bit key?
P3: Make sure you don't lose precision, the numbers are pretty big (besides the e value)


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{n33d_a_lArg3r_e_606ce004}
---------------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/crypto-2/1]
└─$ cd ..
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2]
└─$ mkdir 2
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2]
└─$ cd 2 
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ wget https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext
--2023-10-30 13:20:22--  https://jupiter.challenges.picoctf.org/static/ee7e2388b45f521b285334abb5a63771/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 884 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                                100%[====================================================================================>]     884  --.-KB/s    in 0s      

2023-10-30 13:20:37 (9.05 MB/s) - ‘ciphertext’ saved [884/884]
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ cat ciphertext 

N: 29331922499794985782735976045591164936683059380558950386560160105740343201513369939006307531165922708949619162698623675349030430859547825708994708321803705309459438099340427770580064400911431856656901982789948285309956111848686906152664473350940486507451771223435835260168971210087470894448460745593956840586530527915802541450092946574694809584880896601317519794442862977471129319781313161842056501715040555964011899589002863730868679527184420789010551475067862907739054966183120621407246398518098981106431219207697870293412176440482900183550467375190239898455201170831410460483829448603477361305838743852756938687673
e: 3

ciphertext (c): 2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125 
     ┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ sudo python3 -m pip install gmpy2                                                          
[sudo] password for kali: 
DEPRECATION: Loading egg at /usr/local/lib/python3.11/dist-packages/PySoundFile-0.9.0.post1-py3.11.egg is deprecated. pip 23.3 will enforce this behaviour change. A possible replacement is to use pip for package installation..                                                                                                            
DEPRECATION: Loading egg at /usr/local/lib/python3.11/dist-packages/sstv-0.1-py3.11.egg is deprecated. pip 23.3 will enforce this behaviour change. A possible replacement is to use pip for package installation..                                                                                                                           
Collecting gmpy2                                                                                                                                                       
  Downloading gmpy2-2.1.5-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.8 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.8/1.8 MB 69.2 kB/s eta 0:00:00
Installing collected packages: gmpy2
Successfully installed gmpy2-2.1.5
WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv                                                                                                                 
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ code .        
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ python3 exp.py 
Traceback (most recent call last):
  File "/home/kali/Downloads/crypto-2/2/exp.py", line 3, in <module>
    gympy2.get_context().precision = 2048
    ^^^^^^
NameError: name 'gympy2' is not defined. Did you mean: 'gmpy2'?
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ python3 exp.py
Ecnontre t :0
Flag: picoCTF{n33d_a_lArg3r_e_606ce004}
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/crypto-2/2]
└─$ 

--------------------------------------------------------------------------------
el exp

from gmpy2 import *

  

gmpy2.get_context().precision = 2048

  

n = 29331922499794985782735976045591164936683059380558950386560160105740343201513369939006307531165922708949619162698623675349030430859547825708994708321803705309459438099340427770580064400911431856656901982789948285309956111848686906152664473350940486507451771223435835260168971210087470894448460745593956840586530527915802541450092946574694809584880896601317519794442862977471129319781313161842056501715040555964011899589002863730868679527184420789010551475067862907739054966183120621407246398518098981106431219207697870293412176440482900183550467375190239898455201170831410460483829448603477361305838743852756938687673

e = 3

c = 2205316413931134031074603746928247799030155221252519872649649212867614751848436763801274360463406171277838056821437115883619169702963504606017565783537203207707757768473109845162808575425972525116337319108047893250549462147185741761825125

  

for t in range (100000):

m, r = iroot(t*n + c, e)

if r :

print('Ecnontre t :'+str(t))

print('Flag: ' + str(bytes.fromhex(hex(m)[2:]).decode()))

---------------------------------------------------------------------------------
Nos queda que:
m = raiz(tn+c , 3)


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://gmpy2.readthedocs.io/en/latest/intro.html
