# ASCII FTW
## Objetivo
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/508/asciiftw).
## Pistas
P1: The combined range of hex-ascii for English alphabets and numerical digits is from 30 to 7A.
P2: Online hex-ascii converters can be helpful.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:
--------------------------------------------------------------------------------------

void main(void)

{
  long lVar1;
  long in_FS_OFFSET;
  
  lVar1 = *(long *)(in_FS_OFFSET + 0x28);
  printf("The flag starts with %x\n",0x70);
  if (lVar1 != *(long *)(in_FS_OFFSET + 0x28)) {
                    /* WARNING: Subroutine does not return */
    __stack_chk_fail();
  }
  return;
}

--------------------------------------------------------------------------------------
lo abrimos con ghidra y analizamos lo que nos indica 
7069636f4354467b41534349495f49535f454153595f38393630463041467d
y descifrandolo 
picoCTF{ASCII_IS_EASY_8960F0AF}


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NzA2OTYzNmY0MzU0NDY3YjQxNTM0MzQ5NDk1ZjQ5NTM1ZjQ1NDE1MzU5NWYzODM5MzYzMDQ2MzA0MTQ2N2Q