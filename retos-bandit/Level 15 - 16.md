# Level 15 ->16
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
```bash
Usuario: bandit15
Contraseña:jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
## Solución
```bash
Pass siguiente lvl:JQttfApK4SeyHwDlI9SXGR50qclOAil1

bandit15@bandit:~$
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  5 14:21:56 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  5 14:21:56 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  5 14:20:56 2023 GMT; NotAfter: Sep  5 14:21:56 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIERT5t9zANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTA1MTQyMDU2WhcNMjMwOTA1MTQyMTU2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCm
wBiPjdh1RI2h6uD0NBu9weZgCFgUwOM5PTlJzrrbDIG6MojStI6UWFDOGJAGYk/O
3vOKI4XC1r51gsOG+JSQye+9XqlNKVidFm8muvoOQhtCb3vquFm1kn4B5ZlVFPE+
kwN9TB+Vv9vfwXI3HG7o5KBRBZRPKV1KNOU+x3jhjphuXbLOi0PeNHWAyEBHfNEX
Zrz+Zvun+kgq8CmGGp9oMYRfwjmvPaZYQtTH/JUmt7vbsXalAb6oaCHx36GeuEJH
lAoPkI++eVSLJQO7tdtMeNpYKttX1jIjVvMqAKf7Nhx91m7A1mBGjUw8FDjZjhjn
ynORJxJii0nCah3xomyHAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAx
ECelAuW6irw6S0/rR2vxrL9Oeej7SWiQ1CizTLew+HZRzRQmTwGqmYnSQnMUhCRT
u5vFwP6tnDrUXlSrazBnDve87BMzdECWhauErj9Pt40gLDuSgvLkZWl6P+f8Frb8
FkDUXuqxiq1vZxOcY0gSQpwvLeS06RMi546KNmDt4+Qfvqt4oXRL+882bqgoOqHQ
P/VsqO52CXoAe5rLuhyC/YVnWxIQnjE5EUYkXCd0Zdm7JOzuKbid7FGinAnpzfUz
vaG4FaUl1ITlxUE9xAWiDIDBYZuXUbj8CyipZm+v0ksNPqXYkh/PvK24fyaAeAUL
Yrmp3Qa25oeRjlPTmVTD
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
    Session-ID: 6D601A661D39A0A397A2B6D09CD8B1072800C7F3A09EA7FA8B8B5B0368A0D6E3
    Session-ID-ctx:
    Resumption PSK: 11325E9B52B1124BC6C752552DB206BC83B2BBF23ED14F5453C2B292EF84B7E12E0FF52BBC38EE9E4369533D6AE89B4E
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 0a 48 a5 32 54 0e cb 4c-36 de e2 24 47 c1 4f 66   .H.2T..L6..$G.Of
    0010 - 20 63 be 37 a2 c7 c7 20-e1 ae 27 87 fe 7a 7d 78    c.7... ..'..z}x
    0020 - 19 74 5d cf a2 2d b2 f8-61 a8 e0 96 43 d5 a7 04   .t]..-..a...C...
    0030 - d3 00 49 13 5a 70 83 d3-5c d4 a9 64 4f 56 52 6a   ..I.Zp..\..dOVRj
    0040 - 7a 2e c3 25 32 34 a1 40-75 60 05 b3 2a c3 0c 3c   z..%24.@u`..*..<
    0050 - 72 7f a8 9b 14 82 11 2d-c0 a0 1d 8e 52 bf 53 01   r......-....R.S.
    0060 - 4e 0d 7e e1 73 3a 37 80-c6 f9 71 65 be a8 f1 e5   N.~.s:7...qe....
    0070 - 01 27 58 14 5b 76 37 0a-91 02 91 e5 6c 40 2b 6e   .'X.[v7.....l@+n
    0080 - fb a2 e8 6f d1 ea 2a d8-7f 3f 8f 0b dc 53 44 08   ...o..*..?...SD.
    0090 - 91 f7 88 9e f2 dc f7 9d-aa 92 4f 30 81 ad 93 f6   ..........O0....
    00a0 - 6a ea 02 ba 02 f7 b3 76-ea 12 7f 29 4d 34 12 0e   j......v...)M4..
    00b0 - 18 07 98 f2 0e 2d fa 0f-6f 93 b7 dd 37 a1 fc 6d   .....-..o...7..m
    00c0 - 03 b8 d9 b9 08 c8 c1 b3-e1 1c ba 59 34 b5 bd 3c   ...........Y4..<

    Start Time: 1694021706
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
    Session-ID: 285D156402B9D0A7072A09E6C937018A31B4416840A35D2B43B98BACF2C2D671
    Session-ID-ctx:
    Resumption PSK: 22C067BD48F384F6BE3D1DDD846763E922CC6BD8D1E3BD1726509314929CA2E987D901A5C39EF20D8D949466D8D23775
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 0a 48 a5 32 54 0e cb 4c-36 de e2 24 47 c1 4f 66   .H.2T..L6..$G.Of
    0010 - ae 66 76 e5 05 38 4a 17-8f ea 64 ae 62 6d 7d 5e   .fv..8J...d.bm}^
    0020 - e7 d9 8d 5d 4d 4c ef a2-20 d2 da 2f 40 c7 8c f9   ...]ML.. ../@...
    0030 - bc a6 27 2f cf 57 69 0c-07 d4 44 15 c4 3e e3 32   ..'/.Wi...D..>.2
    0040 - 18 4e 3f 10 ed bd 1c 84-d4 cb b7 a6 fe 35 73 f6   .N?..........5s.
    0050 - 47 4c 77 d8 6d b3 84 4a-f7 d7 45 30 a4 b3 23 b5   GLw.m..J..E0..#.
    0060 - a4 82 1a 2d 00 39 21 57-8a 4b 98 69 0f 9c e6 3a   ...-.9!W.K.i...:
    0070 - dd 51 e8 ce 40 16 f8 f8-09 cc 2f e6 26 b7 b1 d2   .Q..@...../.&...
    0080 - 19 0a d3 b7 b8 16 d8 37-01 b0 78 3b 8a 87 8b b4   .......7..x;....
    0090 - 0d 8a 43 72 b2 ec 5e 0c-27 ed e1 99 bf 9c e0 42   ..Cr..^.'......B
    00a0 - c4 a5 34 80 32 99 cc 35-46 ce 35 6b 98 13 ff d4   ..4.2..5F.5k....
    00b0 - 59 56 b3 0d e7 3c 4d 58-bb 5d 17 4f 94 23 97 91   YV...<MX.].O.#..
    00c0 - 20 1b de 3d 9b 20 89 3a-4c 73 45 cb d6 a2 9b 4c    ..=. .:LsE....L

    Start Time: 1694021707
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|
| ssl | la que usan https |
| https | protocolo seguro
| openssl |  permite conectar si tiene ese protocolo|
| s_client | indicar soy cliente |
| - connect |  establecer conexión requiere indicar host y puerto
r
## Referencias 
- [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)