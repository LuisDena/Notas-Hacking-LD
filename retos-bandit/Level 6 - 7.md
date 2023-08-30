# Level 6 -> 7

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel
```bash
usr: bandit6
pass: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Solución
``` bash
pass lvl 7: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

bandit6@bandit:~$ man find
bandit6@bandit:~$ find / -size 33c - user bandit7 -group bandit6 2>/dev/null
bandit6@bandit:~$
bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$ ^C
bandit6@bandit:~$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
|- usr | para especificar usr en find 
| - group | para especificar grupo |
| 2>/dev/null| no mostrar los errores(cualquier comando)
|

## Referencias 