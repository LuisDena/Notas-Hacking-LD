# Mr-Worldwide
## Objetivo
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?
## Pistas


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{KODIAK_ALASKA}
-----------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/4]
└─$ wget https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt
--2023-11-13 16:58:02--  https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 278 [application/octet-stream]
Saving to: ‘message.txt’

message.txt                  100%[==============================================>]     278  --.-KB/s    in 0s      

2023-11-13 16:58:03 (3.61 MB/s) - ‘message.txt’ saved [278/278]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/4]
└─$ cat message.txt 
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-1/4]
└─$ 

------------------------------------------------------------------------------------
Entramos a todas las coordenadas en maps lo que nos da (ubicaciones en ingles)
picoCTF{
(35.028309, 135.753082)         K yoto, Japon
(46.469391, 30.740883)          O desa, Ucrania
(39.758949, -84.191605)         D ayton, OH
(41.015137, 28.979530)          I stanbul, Turquía
(24.466667, 54.366669)          A bu Dhabi, Emiratos Arabes
(3.140853, 101.693207)          K uala Lumpur, Malasia
_
(9.005401, 38.763611)           A ddis Ababa, Etiopia
(-3.989038, -79.203560)         L oja, Ecuador
(52.377956, 4.897070)           A msterdam, Paises Bajos
(41.085651, -73.858467)         S leepy Hollow, NY
(57.790001, -152.407227)        K odiak, Ak
(31.205753, 29.924526)          A lexandria, Egipto
}          
por lo que la bandera es 

picoCTF{KODIAK_ALASKA}

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
