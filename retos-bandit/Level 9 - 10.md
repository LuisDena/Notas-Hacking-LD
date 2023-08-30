# Level 9 -> 10
## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
```
usr: bandit9
pass:EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Solución
```
pass lvl 10:G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

bandit9@bandit:~$ cat data.txt | strings -n 12
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$ cat data.txt | strings -n 12 | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$ cat data.txt | strings -n 12 | grep "=="
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$ cat data.txt | strings -n 20 | grep "=="
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$ cat data.txt | strings -n 20 | tr -d =
 G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| strings | despliega solo las cadenas de char
|-n | numero de caracteres |
| tr -d 'char'| sirve para eliminar un char determinado de la salida|
## Referencias 
