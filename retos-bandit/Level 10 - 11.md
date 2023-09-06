# Level 10->11
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso al nivel
```bash
Usuario:bandit10
Contraseña:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Solución
```bash
Pass siguiente lvl: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

bandit10@bandit:~$ echo "aG9sYSBwcm9mZSBob3kgbm8gdmVuaW1vcwo=" | base64 -d
hola profe hoy no venimos
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$

con python:

>>> data
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'data' is not defined. Did you mean: 'datos'?
>>> base64.b64decode(datos)
b'The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM\n'
>>>

```
## Notas Adicionales
Primero leer el archivo 
codificar : convertir archivo en algo no legible para otras personas.

| Comando  | Descripción | 
|------------|--------------|
| Base64| esquema de codificacion de binario a texto |
| == | completa el pading |
| base64 -d | para decodificar segun base


## Referencias 
https://en.wikipedia.org/wiki/Base64
https://docs.python.org/3/library/codecs.html
https://stackabuse.com/encoding-and-decoding-base64-strings-in-python/
https://gchq.github.io/CyberChef/