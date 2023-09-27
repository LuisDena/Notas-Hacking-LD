# Tab-tab-attack
## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip)

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}
---------------------------------------------------------
dena-picoctf@webshell:~$ ls 
Addadshashanammu  README.txt
dena-picoctf@webshell:~$ 
dena-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
dena-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelka
shishi/Onnissiralis/Ularradallaku$ ls -la
total 12
drwxr-xr-x 2 dena-picoctf dena-picoctf   35 Mar 16  2021 .
drwxr-xr-x 3 dena-picoctf dena-picoctf   27 Mar 16  2021 ..
-rwxr-xr-x 1 dena-picoctf dena-picoctf 8320 Mar 16  2021 fang-of-haynekhtnamet
dena-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelka
shishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}
dena-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelka
shishi/Onnissiralis/Ularradallaku$ ^C
dena-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelka
shishi/Onnissiralis/Ularradallaku$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|


## Referencias 
