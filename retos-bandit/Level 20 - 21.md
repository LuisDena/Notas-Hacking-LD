# Level 20 -> 21
## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel
```bash
Usuario: bandit20
Contraseña: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
## Solución
```bash
Pass siguiente lvl: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
------------------------------
bandit20@bandit:~$ jobs
bandit20@bandit:~$ nc -lnvp 5050 <<< "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" &
[1] 2322854
bandit20@bandit:~$ Listening on 0.0.0.0 5050
ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit21 bandit20 15600 Apr 23 18:04 suconnect
bandit20@bandit:~$ ./suconnect 5050
Connection received on 127.0.0.1 60634
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+  Done                    nc -lnvp 5050 <<< "VxCazJaVykI6W36BkBU0mJTCM8rR95XT"
```
## Notas Adicionales
misma logica que el anterior.

abrir puerto para que se pueda conectar y mandar la pass

| Comando  | Descripción | 
|------------|--------------|
| & | mandarlo a segundo plano |
| bg | mandarlo abackground

## Referencias 
