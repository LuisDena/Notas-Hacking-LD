# c0rrupt
## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Pistas
P1: Try fixing the file header
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{c0rrupt10n_1847995}
-----------------------------------------------------------------------------------
lo descargamos y le hacemos una copia para trabajar con ese archivo

con hexeditor arreglamos en base a lo de la pagina 

descargamos pngcheck y vemos que un chunk esta dañado, lo cambiamos segun lo indicado en la pagina

reparamos todos los errores que nos marque el pngcheck

una vez reparada nos muestra la flag
picoCTF{c0rrupt10n_1847995}
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://en.wikipedia.org/wiki/List_of_file_signatures