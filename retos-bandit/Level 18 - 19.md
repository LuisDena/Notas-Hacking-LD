# Level 18 ->19
## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso al nivel
```bash
Usuario: bandit18
Contraseña: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
## Solución
```bash
Pass siguiente lvl:awhqfNnAbc1naukrpqDYcF95h7HoMTrC
------------------------------------------
C:\Users\LuisD\OneDrive\Escritorio\IS_MAT_7\NotasHacking\retos-bandit>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

C:\Users\LuisD\OneDrive\Escritorio\IS_MAT_7\NotasHacking\retos-bandit>
--------------------------------- solucion 2
C:\Users\LuisD\OneDrive\Escritorio\IS_MAT_7\NotasHacking\retos-bandit>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
id
uid=11018(bandit18) gid=11018(bandit18) groups=11018(bandit18)
ls -la
total 24
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r-----  1 bandit19 bandit18 3794 Apr 23 18:04 .bashrc
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
-rw-r-----  1 bandit19 bandit18   33 Apr 23 18:04 readme
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
