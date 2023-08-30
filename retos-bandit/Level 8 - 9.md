# Level 8 -> 9
## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
```
usr: bandit8
pass: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Solución
```
pass lvl 9: EN632PlfYiZbn3PhVK3XOGSlNInNE00t


bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| pipeline | sirve para redirigir la salida a otro comando|
| sort|ordenar  |
| uniq| puede contar las repetidas o mostrar las no repetidas |
| -d | las repetidas
|-u | las no repetidas





## Referencias 
[Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)
