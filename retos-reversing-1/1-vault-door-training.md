# vault-door-training
## Objetivo
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: [VaultDoorTraining.java](https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java)
## Pistas
P1: The password is revealed in the program's source code.

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{w4rm1ng_Up_w1tH_jAv4_be8d9806f18}
---------------------------------------------------------------------
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ wget https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java     
--2023-11-04 17:05:57--  https://jupiter.challenges.picoctf.org/static/a4a1ca9c54d8fac9404f9cbc50d9751a/VaultDoorTraining.java
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 943 [application/octet-stream]
Saving to: ‘VaultDoorTraining.java’

VaultDoorTraining.java       100%[==============================================>]     943  --.-KB/s    in 0s      

2023-11-04 17:05:58 (3.63 MB/s) - ‘VaultDoorTraining.java’ saved [943/943]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ ls -la
total 12
drwxr-xr-x 2 kali kali 4096 Nov  4 17:05 .
drwxr-xr-x 3 kali kali 4096 Nov  4 15:54 ..
-rw-r--r-- 1 kali kali  943 Oct 26  2020 VaultDoorTraining.java
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ cat VaultDoorTraining.java                        
import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
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

    // The password is below. Is it safe to put the password in the source code?
    // What if somebody stole our source code? Then they would know what our
    // password is. Hmm... I will think of some ways to improve the security
    // on the other doors.
    //
    // -Minion #9567
    public boolean checkPassword(String password) {
        return password.equals("w4rm1ng_Up_w1tH_jAv4_be8d9806f18");
    }
}
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ java --version     
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
openjdk 17.0.9-ea 2023-10-17
OpenJDK Runtime Environment (build 17.0.9-ea+4-Debian-1)
OpenJDK 64-Bit Server VM (build 17.0.9-ea+4-Debian-1, mixed mode, sharing)
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ javac --version
Command 'javac' not found, did you mean:
  command 'javagc' from deb libbpf-tools
  command 'javacc' from deb javacc
Try: sudo apt install <deb name>
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ javac --version                          
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
javac 17.0.9
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ javac VaultDoorTraining.java 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ ls -la
total 16
drwxr-xr-x 2 kali kali 4096 Nov  4 17:17 .
drwxr-xr-x 3 kali kali 4096 Nov  4 15:54 ..
-rw-r--r-- 1 kali kali 1106 Nov  4 17:17 VaultDoorTraining.class
-rw-r--r-- 1 kali kali  943 Oct 26  2020 VaultDoorTraining.java
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ java VaultDoorTraining.class             
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Error: Could not find or load main class VaultDoorTraining.class
Caused by: java.lang.ClassNotFoundException: VaultDoorTraining.class
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ java VaultDoorTraining      
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{ashdjashd}
Access denied!
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ java VaultDoorTraining
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{w4rm1ng_Up_w1tH_jAv4_be8d9806f18}
Access granted.
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/1]
└─$ 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
