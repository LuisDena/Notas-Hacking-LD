# runme.py
## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Pistas
P1: If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
P2: To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
P3: Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
P4: Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{run_s4n1ty_run}
------------------------------------------------
dena-picoctf@webshell:~$ mkdir rmp
dena-picoctf@webshell:~$ cd rmp/
dena-picoctf@webshell:~/rmp$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-09-27 16:22:39--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                100%[============================>]     270  --.-KB/s    in 0s      

2023-09-27 16:22:39 (89.6 MB/s) - 'runme.py' saved [270/270]

dena-picoctf@webshell:~/rmp$ python runme.py 
picoCTF{run_s4n1ty_run}
dena-picoctf@webshell:~/rmp$ ^C
dena-picoctf@webshell:~/rmp$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



