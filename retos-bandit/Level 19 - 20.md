# Level 19 -> 20
## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos de acceso al nivel
```bash
Usuario: bandit19
Contraseña: awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Solución
```bash
Pass siguiente lvl:VxCazJaVykI6W36BkBU0mJTCM8rR95XT
-------------------------------------
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rwsr-x---  1 bandit20 bandit19 14876 Apr 23 18:04 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ id
uid=11019(bandit19) gid=11019(bandit19) groups=11019(bandit19)
bandit19@bandit:~$ sudo cat /etc/bandit_pass/bandit20
sudo: /usr/bin/sudo must be owned by uid 0 and have the setuid bit set
bandit19@bandit:~$ ./bandit20-do id
uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)
bandit19@bandit:~$ ./bandit20-do /etc/b
bandit_pass/            bash_completion.d/      byobu/
bash.bashrc             bindresvport.blacklist
bash_completion         binfmt.d/
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| setuid binary | darle permisos temporales de un usr a otro |
| la s en esa parte | |

## Referencias 
https://en.wikipedia.org/wiki/Setuid