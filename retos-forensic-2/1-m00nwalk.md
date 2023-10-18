# m00nwalk
## Objetivo
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.
## Pistas
P1: How did pictures from the moon landing get sent back to Earth?
P2: What is the CMU mascot?, that might help select a RX option

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{beep_boop_im_in_space}
-------------------------------------------------------------------------
instalamos el sstv decoder en linux
┌──(kali㉿kali)-[~/Downloads/forensic2]
└─$ sstv -d message.wav -o img.jpg
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                                    [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/forensic2]
└─$ open img.jpg 



luego vemos la imagen la volteamos y escribimos la flag encontrada en la imagen
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://github.com/colaclanth/sstv