# vault-door-3
## Objetivo
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java)
## Pistas
P1: Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}
---------------------------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ wget https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java
--2023-11-04 17:34:21--  https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1474 (1.4K) [application/octet-stream]
Saving to: ‘VaultDoor3.java’

VaultDoor3.java              100%[==============================================>]   1.44K  --.-KB/s    in 0s      

2023-11-04 17:34:22 (11.9 MB/s) - ‘VaultDoor3.java’ saved [1474/1474]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ ls -la                        
total 12
drwxr-xr-x 2 kali kali 4096 Nov  4 17:34 .
drwxr-xr-x 5 kali kali 4096 Nov  4 17:34 ..
-rw-r--r-- 1 kali kali 1474 Oct 26  2020 VaultDoor3.java
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ cat VaultDoor3.java                                              
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm18g947_u_4_m9r54f");
    }
}
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ 
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ javac VaultDoor3.java 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ java VaultDoor3      
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}
Access granted.
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/3]
└─$ 

---------------------------------------------------------------------------------------
java script

permitir pegar  

Uncaught SyntaxError: unexpected token: identifier

debugger eval code:1:10  

var password = "jU5t_a_sna_3lpm18g947_u_4_m9r54f";  

undefined  

var buffer = Array(32);  

undefined  

for (i=0; i<8; i++) { buffer[i] = password.charAt(i); } for (; i<16; i++) { buffer[i] = password.charAt(23-i);…  

"g"  

buffer.join("")

"jU5t_a_s1mpl3_an4gr4m_4_u_79958f"

```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
