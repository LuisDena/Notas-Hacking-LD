# asm2
## Objetivo
What does asm2(0x4,0x2d) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/ceac75672637589213b952abe32c84b3/test.S)
## Pistas
P1: assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:0xa3
---------------------------------------------------------------------------------------

┌──(kali㉿kali)-[~]
└─$ python3
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x4 <= 0x5fa1
True
>>> 0x2d + 0x1
46
>>> hex(0x2d + 0x1)
'0x2e'
>>> hex (0x4 + 0xd1)
'0xd5'
>>> hex (0xd5 <= 0x5fa1)
'0x1'
>>>  (0xd5 <= 0x5fa1)
  File "<stdin>", line 1
    (0xd5 <= 0x5fa1)
IndentationError: unexpected indent
>>> 0xd5 <= 0x5fa1
True
>>> int(0x5fa1 / 0xd1)
117
>>> int(0x2d)
45
>>> hex (45+117)
'0xa2'
>>> hex (45+118)
'0xa3'
>>> 
---------------------------------------------------------------------------------------
  GNU nano 7.2                                                                     test.S                                                                              
asm2:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   sub    esp,0x10
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]
        <+9>:   mov    DWORD PTR [ebp-0x4],eax
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]
        <+15>:  mov    DWORD PTR [ebp-0x8],eax
        <+18>:  jmp    0x50c <asm2+31>
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0xd1
        <+31>:  cmp    DWORD PTR [ebp-0x8],0x5fa1
        <+38>:  jle    0x501 <asm2+20>
        <+40>:  mov    eax,DWORD PTR [ebp-0x4]
        <+43>:  leave  
        <+44>:  ret    
----------------------------------------------------------------------------------------
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ file test.S          
test.S: ASCII text
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ cat test.S         
asm2:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   sub    esp,0x10
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]
        <+9>:   mov    DWORD PTR [ebp-0x4],eax
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]
        <+15>:  mov    DWORD PTR [ebp-0x8],eax
        <+18>:  jmp    0x50c <asm2+31>
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0xd1
        <+31>:  cmp    DWORD PTR [ebp-0x8],0x5fa1
        <+38>:  jle    0x501 <asm2+20>
        <+40>:  mov    eax,DWORD PTR [ebp-0x4]
        <+43>:  leave  
        <+44>:  ret    

                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ nano test.S   
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ nano test.S
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm2]
└─$ 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
