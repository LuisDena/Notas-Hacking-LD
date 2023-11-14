# Bit-O-Asm-1
## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
## Pistas
P1: As with most assembly, there is a lot of noise in the instruction dump. Find the one line that pertains to this question and don't second guess yourself!


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{48}
------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/2]
└─$ wget https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
--2023-11-13 19:11:13--  https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.103, 18.154.144.85, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 209 [application/octet-stream]
Saving to: ‘disassembler-dump0_a.txt’

disassembler-dump0_a.txt     100%[==============================================>]     209  --.-KB/s    in 0s      

2023-11-13 19:11:13 (56.3 MB/s) - ‘disassembler-dump0_a.txt’ saved [209/209]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/2]
└─$ cat disassembler-dump0_a.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/2]
└─$ cat disassembler-dump0_a.txt | grep "eax"
<+15>:    mov    eax,0x30
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/2]
└─$ pyhton3       
Command 'pyhton3' not found, did you mean:
  command 'python3' from deb python3-minimal
Try: sudo apt install <deb name>
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/2]
└─$ python3       
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int("0x30",16))
48
>>> 

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
