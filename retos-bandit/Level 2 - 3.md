# Level 2 -> 3
## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de acceso al nivel
``` bash
Usr: bandit2
Pass: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Solución
``` bash
pass lvl 3: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

bandit2@bandit:~$ pwd
/home/bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
## Notas Adicionales
Dándole tab se puede autocompletar el nombre del archivo aunque tenga espacios en el nombre

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
[Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)