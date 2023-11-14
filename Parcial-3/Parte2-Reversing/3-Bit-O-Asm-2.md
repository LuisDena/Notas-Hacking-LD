# Bit-O-Asm-2
## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Pistas
P1: `PTR`'s or 'pointers', reference a location in memory where values can be stored.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{654874}
--------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/3]
└─$ wget https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
--2023-11-13 19:13:49--  https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.103, 18.154.144.104, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘disassembler-dump0_b.txt’

disassembler-dump0_b.txt     100%[==============================================>]     270  --.-KB/s    in 0s      

2023-11-13 19:13:49 (116 MB/s) - ‘disassembler-dump0_b.txt’ saved [270/270]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/3]
└─$ cat disassembler-dump0_b.txt             
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/3]
└─$ cat disassembler-dump0_b.txt | grep eax 
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/3]
└─$ python3 
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int("0x9fe1a",16))
654874
>>> 
KeyboardInterrupt
>>> quit()
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/Parcial-3/Parte-2/3]
└─$                                             

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
