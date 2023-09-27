# glitch-cat
## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 55826`
## Pistas
P1: ASCII is one of the most common encodings used in programming
P2: We know that the glitch output is valid Python, somehow!
P3: Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{gl17ch_m3_n07_9c42a45d}
---------------------------------------------------
dena-picoctf@webshell:~$ mkdir glitchcat
mkdir: cannot create directory 'glitchcat': File exists
dena-picoctf@webshell:~$ cd glitchcat/
dena-picoctf@webshell:~/glitchcat$ nc saturn.picoctf.net 55826
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
^C
dena-picoctf@webshell:~/glitchcat$ vim script.py
dena-picoctf@webshell:~/glitchcat$ nano script.py^C
dena-picoctf@webshell:~/glitchcat$ vim script.py
dena-picoctf@webshell:~/glitchcat$ nano script.py
dena-picoctf@webshell:~/glitchcat$ nano script.py
dena-picoctf@webshell:~/glitchcat$ 
dena-picoctf@webshell:~/glitchcat$ nano script.py 
dena-picoctf@webshell:~/glitchcat$ nano script.py 
dena-picoctf@webshell:~/glitchcat$ python3 script.py 
  File "/home/dena-picoctf/glitchcat/script.py", line 2
    + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) 
IndentationError: unexpected indent
dena-picoctf@webshell:~/glitchcat$ nano script.py 
dena-picoctf@webshell:~/glitchcat$ python3 script.py 
picoCTF{gl17ch_m3_n07_9c42a45d}
dena-picoctf@webshell:~/glitchcat$ 
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 



