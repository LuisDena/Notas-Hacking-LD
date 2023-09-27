# Strings-it 
## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
## Pistas
P1:[strings](https://linux.die.net/man/1/strings)

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución

```bash
Pass siguiente lvl: picoCTF{5tRIng5_1T_d66c7bb7}
----------------------------
dena-picoctf@webshell:~/stringsit$ cat strings | strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}
dena-picoctf@webshell:~/stringsit$ 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
