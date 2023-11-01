# Mind your Ps and Qs
## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)
## Pistas
P1: Bits are expensive, I used only a little bit over 100 to save money
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{sma11_N_n0_g0od_55304594}
--------------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/crypto-3/1]
└─$ ls -la
total 12
drwxr-xr-x 2 kali kali 4096 Oct 31 22:37 .
drwxr-xr-x 4 kali kali 4096 Oct 31 22:37 ..
-rw-r--r-- 1 kali kali  205 Mar 15  2021 values
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads/crypto-3/1]
└─$ cat values  
Decrypt my super sick RSA:
c: 421345306292040663864066688931456845278496274597031632020995583473619804626233684
n: 631371953793368771804570727896887140714495090919073481680274581226742748040342637
e: 65537                                                                                                                     
┌──(kali㉿kali)-[~]
└─$ python3       
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
>>> n = 631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> e = 65537
>>> p = 1461849912200000206276283741896701133693
>>> q = 431899300006243611356963607089521499045809
>>> t = (p-1)*(q-1)
>>> d = pow (e,-1,t)
>>> m = pow (c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639647889241102700065917
>>> bytes.fromhex(hex(m)[2:]).decode()
'picoCTF{sma11_N_n0_g0od_55304594}'
>>> 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
http://factordb.com/index.php?query=631371953793368771804570727896887140714495090919073481680274581226742748040342637
