# asm3
## Objetivo
What does asm3(0xd73346ed,0xd48672ae,0xd3c8b139) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/17c5620fcffa388fe518d31cb4dd99a0/test.S)

## Pistas
P1: more(?) [registers](https://wiki.skullsecurity.org/index.php?title=Registers)


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:0xC36B
-----------------------------------------------------------------------------------
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ cd ..  
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2]
└─$ cd asm3
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm3]
└─$ file test.S 
test.S: ASCII text
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm3]
└─$ cat test.S  
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0xa]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xc]
        <+15>:  add    ah,BYTE PTR [ebp+0xd]
        <+18>:  xor    ax,WORD PTR [ebp+0x10]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret    

                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm3]
└─$ nano test.S 
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm3]
└─$ 
-----------------------------------------------------------------------------------
Registers
|   |   |   |   |   |
|---|---|---|---|---|
|EAX|0x0000C36B||EBX|0x00000000|
|ECX|0x00000000||EDX|0x00000000|
|ESI|0x00000000||EDI|0x00000000|
|EBP|0x00000000||ESP|0x000203F0|
|EIP|0x00020438|Ln 21, Col 10|   |   |

|   |   |   |   |   |
|---|---|---|---|---|
|Flags|   |   |   |   |
|Carry|0||Dir|0|
|Int|0||Overflow|0|
|Sign|1||Zero|0|

-----------------------------------------------------------------------------------
start:
	push 0xd3c8b139
	push 0xd48672ae
	push 0xd73346ed 
	call asm3


asm3:
         push   ebp
         mov    ebp,esp

         xor    eax,eax
         mov    ah,BYTE PTR [ebp+0xa]
         shl    ax,0x10
         sub    al,BYTE PTR [ebp+0xc]
         add    ah,BYTE PTR [ebp+0xd]
         xor    ax,WORD PTR [ebp+0x10]
         nop

         pop    ebp
         ret    
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://carlosrafaelgn.com.br/Asm86/