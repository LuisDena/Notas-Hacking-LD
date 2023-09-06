# Level 14 -> 15
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
```bash
Usuario:bandit14
Contraseña:fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
## Solución
```bash
Pass siguiente lvl:jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

bandit14@bandit:~$ nc -v localhost 30000
Connection to localhost (127.0.0.1) 30000 port [tcp/*] succeeded!
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| whois | en linux nos permite ver la ip y de quien es la ip|
| nc | herramienta netcat ára hacer conecciones remotas |
|-v | indicar el puerto|

## Referencias 
- [How the Internet works in 5 minutes (YouTube)](https://www.youtube.com/watch?v=7_LPdttKXPc) (Not completely accurate, but good enough for beginners)
- [IP Addresses](http://computer.howstuffworks.com/web-server5.htm)
- [IP Address on Wikipedia](https://en.wikipedia.org/wiki/IP_address)
- [Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)
- [Ports](http://computer.howstuffworks.com/web-server8.htm)
- [Port (computer networking) on Wikipedia](https://en.wikipedia.org/wiki/Port_(computer_networking))