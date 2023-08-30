# Level 1 -> 2
## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos de acceso al nivel
``` bash
Usr: bandit1
Pass: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
## Solución
``` bash
ssh bandit1@bandit.labs.overthewire.org -p 2220

Pass lvl 2: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```
## Notas Adicionales
Cuando un archivo comienza con '-' para poder acceder hemos de poner ./ o bien la ruta completa de dicho archivo 

| Comando  | Descripción | 
|------------|--------------|
| | |

## Referencias 
- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)