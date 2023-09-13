# Level 17 ->18
## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**
## Datos de acceso al nivel
```bash
Usuario: bandit17
Contraseña: usar key(cambiando permisos)
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```
## Solución
```bash
Pass siguiente lvl: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

----------------------------------------
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r-----  1 bandit17 bandit17   33 Apr 23 18:04 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Apr 23 18:04 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Apr 23 18:04 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .ssh
bandit17@bandit:~$
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r-----  1 bandit17 bandit17   33 Apr 23 18:04 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Apr 23 18:04 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Apr 23 18:04 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .ssh
bandit17@bandit:~$ head passwords.old
SEN5dn6xYkQItiimhyqAlmecmMwBtUxQ
RJIavo1DXZXFjpv3c4BB22gJf6jkR3By
fRu6dfM5HFNjkRHSPpDqKHMuo4IXDISL
1ryPLzBZjmePEjUMGIGGx0IZoRTP5WfG
C1aTZwWUpZp3RiPhOezpyv8uI7XyRxNX
YwYnbb0AID81Q6gTjIuIlUF8E6CaHury
6crimLWCTIxTbEPuMcETzsXeR1E1dEiO
95tD0m3soHHPT6mjsdCBw4o03alLbbQe
6gWKTBH7ENMeNpFIedCvTBNCgpM0EoIB
MurtzHjt9cWZ6qQvfDk7sXkBsfc9BloE
bandit17@bandit:~$ head passwords.new
SEN5dn6xYkQItiimhyqAlmecmMwBtUxQ
RJIavo1DXZXFjpv3c4BB22gJf6jkR3By
fRu6dfM5HFNjkRHSPpDqKHMuo4IXDISL
1ryPLzBZjmePEjUMGIGGx0IZoRTP5WfG
C1aTZwWUpZp3RiPhOezpyv8uI7XyRxNX
YwYnbb0AID81Q6gTjIuIlUF8E6CaHury
6crimLWCTIxTbEPuMcETzsXeR1E1dEiO
95tD0m3soHHPT6mjsdCBw4o03alLbbQe
6gWKTBH7ENMeNpFIedCvTBNCgpM0EoIB
MurtzHjt9cWZ6qQvfDk7sXkBsfc9BloE
bandit17@bandit:~$ wc passwords.old
 100  100 3300 passwords.old
bandit17@bandit:~$ wc passwords.new
 100  100 3300 passwords.new
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< glZreTEH1V3cGKL6g4conYqZqaEj0mte
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< glZreTEH1V3cGKL6g4conYqZqaEj0mte
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| diff | sirve para comparar archivos linea por linea| 
| | |
| | |



## Referencias 
