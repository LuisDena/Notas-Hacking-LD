# vault-door-5
## Objetivo
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java)
## Pistas
P1: You may find an encoder/decoder tool helpful, such as https://encoding.tools/
P2: Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.
## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl: picoCTF{c0nv3rt1ng_fr0m_ba5e_64_e3152bf4}
-------------------------------------------------------------------------------------
┌──(kali㉿kali)-[~/Downloads/reversing-1]
└─$ mkdir 5
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1]
└─$ cd 5 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/5]
└─$ wget https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java
--2023-11-04 18:00:44--  https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1847 (1.8K) [application/octet-stream]
Saving to: ‘VaultDoor5.java’

VaultDoor5.java              100%[==============================================>]   1.80K  --.-KB/s    in 0s      

2023-11-04 18:00:45 (8.89 MB/s) - ‘VaultDoor5.java’ saved [1847/1847]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/5]
└─$ cat VaultDoor5.java 
import java.net.URLDecoder;
import java.util.*;

class VaultDoor5 {
    public static void main(String args[]) {
        VaultDoor5 vaultDoor = new VaultDoor5();
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

    // Minion #7781 used base 8 and base 16, but this is base 64, which is
    // like... eight times stronger, right? Riiigghtt? Well thats what my twin
    // brother Minion #2415 says, anyway.
    //
    // -Minion #2414
    public String base64Encode(byte[] input) {
        return Base64.getEncoder().encodeToString(input);
    }

    // URL encoding is meant for web pages, so any double agent spies who steal
    // our source code will think this is a web site or something, defintely not
    // vault door! Oh wait, should I have not said that in a source code
    // comment?
    //
    // -Minion #2415
    public String urlEncode(byte[] input) {
        StringBuffer buf = new StringBuffer();
        for (int i=0; i<input.length; i++) {
            buf.append(String.format("%%%2x", input[i]));
        }
        return buf.toString();
    }

    public boolean checkPassword(String password) {
        String urlEncoded = urlEncode(password.getBytes());
        String base64Encoded = base64Encode(urlEncoded.getBytes());
        String expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm"
                        + "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2"
                        + "JTM0JTVmJTY1JTMzJTMxJTM1JTMyJTYyJTY2JTM0";
        return base64Encoded.equals(expected);
    }
}
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/5]
└─$ code .             
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/reversing-1/5]
└─$ 
-----------------------------------Segunda forma ---------------------------------
──(kali㉿kali)-[~/Downloads/reversing-1/5]
└─$ python3       
Python 3.11.5 (main, Aug 29 2023, 15:31:31) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from base64 import b64decode 
>>> from urllib.parse import unquote
>>> 
>>> cad = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVmJTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTY1JTMzJTMxJTM1JTMyJTYyJTY2JTM0"
>>> 
>>> cad = b64.decode(cad)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'b64' is not defined
>>> cad = b64decode(cad)
>>> cad
b'%63%30%6e%76%33%72%74%31%6e%67%5f%66%72%30%6d%5f%62%61%35%65%5f%36%34%5f%65%33%31%35%32%62%66%34'
>>> cad = unquote(cad)
>>> cad
'c0nv3rt1ng_fr0m_ba5e_64_e3152bf4'
>>> 


```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
https://www.w3schools.com/tags/ref_urlencode.ASP
https://gchq.github.io/CyberChef/#recipe=URL_Decode()From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm1KVFkySlRjeUpUTXdKVFprSlRWbUpUWXlKVFl4SlRNMUpUWTFKVFZtSlRNMkpUTTBKVFZtSlRZMUpUTXpKVE14SlRNMUpUTXlKVFl5SlRZMkpUTTA