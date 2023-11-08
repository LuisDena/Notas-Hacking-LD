# asm1
## Objetivo
What does asm1(0x2e0) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/f1c2358ff7d1e9386e41552c549cf2f6/test.S)
## Pistas
P1: assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)


## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: 0x2d6
--------------------------------------------------------------------------------------
>>> 0x2e0 > 0x3fb
False
>>> 0x2e0 != 0x280
True
>>> hex(0x2e0 - 0xa)
'0x2d6'
>>> 
---------------------------------------------------------------------------------------
  GNU nano 7.2                                                                     test.S *                                                                            
asm1:(0x2e0)
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp

        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3fb
...     <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x280
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0xa
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0xa
        <+35>:  jmp    0x529 <asm1+60>
...     <+37>:  cmp    DWORD PTR [ebp+0x8],0x559
        <+44>:  jne    0x523 <asm1+54>
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]
...     <+49>:  sub    eax,0xa
        <+52>:  jmp    0x529 <asm1+60>
        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0xa
        <+60>:  pop    ebp
        <+61>:  ret    

----------------------------------------------------------------------------------------
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm1]
└─$ ls -la 
total 12
drwxr-xr-x 2 kali kali 4096 Nov  8 11:01 .
drwxr-xr-x 5 kali kali 4096 Nov  8 11:02 ..
-rw-r--r-- 1 kali kali  638 Oct 26  2020 test.S
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm1]
└─$ file test.S          
test.S: ASCII text
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/reversing-2/asm1]
└─$ cat test.S                
asm1:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3fb
        <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x280
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0xa
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0xa
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x559
        <+44>:  jne    0x523 <asm1+54>
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]
        <+49>:  sub    eax,0xa

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.cs.virginia.edu/~evans/cs216/guides/x86.html