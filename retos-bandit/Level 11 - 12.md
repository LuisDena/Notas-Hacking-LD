# Level 11 -> 12 
## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de acceso al nivel
```bash
Usuario: bandit11
Contraseña:6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
## Solución
```bash
Pass siguiente lvl:JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

bandit11@bandit:~$
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$ python3
Python 3.10.6 (main, Mar 10 2023, 10:55:28) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> datos = opeb('data.txt').read()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'opeb' is not defined. Did you mean: 'open'?
>>> datos = open('data.txt').read()
>>> datos
'Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi\n'
>>> codecs.decode(datos,'rot13')
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv\n'
>>>


```
## Notas Adicionales
algoritmo de cesar (rot13) 

| Comando  | Descripción | 
|------------|--------------|
| tr (transform)| cambiar un char por otro charOld-charNew|
## Referencias 
https://en.wikipedia.org/wiki/Rot13