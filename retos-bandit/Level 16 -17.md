# Level 16 -> 17
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
```bash
Usuario: bandit16
Contraseña: JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
## Solución
```bash
Pass siguiente lvl:

private key:

--------------------------------------
bandit16@bandit:~$ nmap localhost -p 31000-32000
Starting Nmap 7.80 ( https://nmap.org ) at 2023-09-13 16:20 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.05 seconds

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep 12 19:28:37 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep 12 19:28:37 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep 12 19:27:37 2023 GMT; NotAfter: Sep 12 19:28:37 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEG0BsVDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTEyMTkyNzM3WhcNMjMwOTEyMTkyODM3WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCZ
UxuYBHOC1cImS+smCpNf/KLX5cINzvBHS5Q9vhOKwtTH2+XbP4oEmVJZi/3JYiKz
pjLWLHQ1RUvyZfgWd9TTYKsdQTwLPOVnbPBYSPxQ0ldiL/ShKGfJbBgg48gXwAVN
9TkHbasY+fED+5ZdNijL1oDdawN5kyqrNFC+y8EAIoy1hxMWLWnsUWpCwUu15Yv+
tRktkAKbKzxkLzf5pZapx0voSCJJtjrKkp8Vgwrp4VJpZKe6SzwDQoZldH5eVicl
Hnii4uBJD/w0+W41lp6MVUt4aiLT1EKSuetmaOSCWgFmKYxtI3rvF06yyh3X1Aq/
HGbxxECGCN8GRHAOZvMFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBx
jVQ/R9YfVw9NpY4D636lio5z6My2qR3Vm2Ef+s/iYyNjjIJlYybp87znYWPsnsnI
H14GtLrn4Q5yAnQeZLhEP/kh+P2tHm2kPEXQiUF0St6NkMcwrCFg5FTC5WCL77kP
scevmIbhi8McjEFY4EWEh4o2kslskd8v7ILUGe5gcyntBVC1SrO1pflz+M58djZn
sfGodUvs3yNlHNqpmkbHA7uFnXU8WdDGJzr0KPjmG7tphYiRTUlv7G5AjqrsP6ts
yaqv6EdwogT3e09bc3Tt4TCZkyoUUeE6prhO1d3tP8+IpwtG+0YqOLjaZl7e2UXI
5B1Zk8452tK/oSSc52TD
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 4CE5710EEB32F21F3EEE063CDB2536E32186DFB1ECFC3661C970ED2C29CD6FE8
    Session-ID-ctx:
    Resumption PSK: A486E2FD5C7A42CD92025DA59BEDAF58C98AAD7C384C8EF92EA21D6EE6F2CDECCAA8ABBDAE042B31A6960D10FFC450B7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 8a 53 79 53 f7 5d bc c9-dd 02 bc 88 5e 20 c6 eb   .SyS.]......^ ..
    0010 - d1 f0 48 82 0f 43 90 e4-d3 72 c7 d3 75 9b d8 a3   ..H..C...r..u...
    0020 - b1 e0 c7 72 9f d6 eb 70-ba 92 ee d6 9c 8c 65 fe   ...r...p......e.
    0030 - 48 64 39 10 42 b6 3f 8b-88 39 d7 ad e2 73 b8 74   Hd9.B.?..9...s.t
    0040 - a5 cf ab fd db fa e3 e1-a2 62 ac 65 22 f8 7f 57   .........b.e"..W
    0050 - 98 d3 1f 33 7d 44 27 9a-ba 6b 4a 7c fa 66 9e 2a   ...3}D'..kJ|.f.*
    0060 - ee 03 1c fa 89 c7 2a 3d-7a d9 f1 5b 83 81 f3 71   ......*=z..[...q
    0070 - a2 f9 bf 27 a9 73 cb 97-47 da 09 ca 36 c2 da 2c   ...'.s..G...6..,
    0080 - e8 31 ae 49 2f f6 d4 9b-a1 a6 b4 92 36 ba 11 23   .1.I/.......6..#
    0090 - 46 6b 93 98 63 1b 5d 0e-93 9f d6 ce 0b b5 81 6b   Fk..c.]........k
    00a0 - 80 bb 09 d4 6e 0c 80 76-13 58 93 fd 32 27 bf 49   ....n..v.X..2'.I
    00b0 - 00 57 c2 16 b1 55 32 a2-fd b0 e2 ae 7f 73 59 5d   .W...U2......sY]
    00c0 - 0f 5a ca a1 c1 85 7b 90-4d 5f 8e 49 76 7a 1c da   .Z....{.M_.Ivz..

    Start Time: 1694622258
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 987DDCB5598439B724BC35EF565DDA6CA73EB66AC862C11016221C177E02FC9D
    Session-ID-ctx:
    Resumption PSK: 5B0374213750877C4229944C42F50EB72D94B952B273C5EB50376B2F8B178725ABA6270AD2FFDBBA8074B074861019D4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 8a 53 79 53 f7 5d bc c9-dd 02 bc 88 5e 20 c6 eb   .SyS.]......^ ..
    0010 - 88 e7 30 41 d4 bf 71 5c-1a 91 54 fa e1 f2 71 5c   ..0A..q\..T...q\
    0020 - 4f 10 d5 3e 1a e5 a1 e8-3d 37 46 88 94 8c b8 75   O..>....=7F....u
    0030 - 31 31 22 46 c8 7e 1c 15-7f 9f 0d db 4a 49 90 9d   11"F.~......JI..
    0040 - d9 ba 57 bd fb 57 e2 b5-02 41 a3 79 91 69 d1 68   ..W..W...A.y.i.h
    0050 - c0 0f b6 94 e8 2c a5 69-0d 5c da 69 72 10 f0 76   .....,.i.\.ir..v
    0060 - 15 59 91 3a 57 42 a0 4a-ea ae ae 1d 12 82 56 68   .Y.:WB.J......Vh
    0070 - 58 c2 d6 8f 27 53 00 cd-10 50 f9 81 92 28 35 62   X...'S...P...(5b
    0080 - cf df 68 41 ea de 30 24-b2 c0 45 a2 dc c4 e0 8e   ..hA..0$..E.....
    0090 - 04 58 f5 04 74 48 df 08-55 9d 38 c8 66 a8 e0 c9   .X..tH..U.8.f...
    00a0 - ad d3 01 ef 5d 8e 33 e8-aa 59 7b cb 67 03 10 a5   ....].3..Y{.g...
    00b0 - c2 6e df 5d 5b c7 b0 7f-5a cd 57 19 88 59 73 97   .n.][...Z.W..Ys.
    00c0 - a4 ed e0 9d af 92 14 cf-ad a8 20 81 56 da 2d 0b   .......... .V.-.

    Start Time: 1694622258
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

guardar llave 

```
## Notas Adicionales

Todas las maquinas linux tienen puertos abiertos
(depende cuales segun la funcion)

nmap herremianeta de codigo abierto util para escanear puertos (hacerlo a maquinas conocidas)

| Comando  | Descripción | 
|------------|--------------|
| nmap | para abrir lista de comandosn |
|nmap localhots |ver mis puertos |
| nmap localchots rangoInicial-rangofin | escanear un rango |
| -sV | |
| openssl s_clinet -connect localhost:31046 | meterse por ssl|




## Referencias 
https://en.wikipedia.org/wiki/Port_scanner