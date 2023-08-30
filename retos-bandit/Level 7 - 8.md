# Level 7 -> 8
## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
``` bash
usr: bandit7
pass: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Solución
```bash
pass lvl 8: TESKZC0XvTetK0S9xNwm25STk5iWrBvP


bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$

```
## Notas Adicionales
puedes buscarlo con nano pero no es la mejor opción 

| Comando  | Descripción | 
|------------|--------------|
| wc | contar palabras de un archivo |
| grep | sirve para buscar patrones en cada archivo, pueden ser varios patrones separados|



## Referencias 