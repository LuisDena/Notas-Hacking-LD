# Level 22 -23
## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
## Datos de acceso al nivel
```bash
Usuario: bandit22
Contraseña: WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```
## Solución
```bash
Pass siguiente lvl:QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

-------------------------------------
bandit22@bandit:~$
bandit22@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ whoami
bandit22
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $(echo I am user &myname | md5sum | cut -d ' ' -f 1)
myname: command not found
I am user d41d8cd98f00b204e9800998ecf8427e
bandit22@bandit:~$ cat /tmp/d41d8cd98f00b204e9800998ecf8427e
cat: /tmp/d41d8cd98f00b204e9800998ecf8427e: No such file or directory
bandit22@bandit:~$ echo $(echo I am user &myname | md5sum | cut -d ' ' -f l)
cut: invalid field value ‘l’
Try 'cut --help' for more information.
myname: command not found
I am user
bandit22@bandit:~$ echo $(echo I am user &myname | md5sum | cut -d ' ' -f 1)
myname: command not found
I am user d41d8cd98f00b204e9800998ecf8427e
bandit22@bandit:~$ echo $(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit22@bandit:~$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
