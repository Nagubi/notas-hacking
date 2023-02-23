# Bandit Level 16 → Level 17
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso al nivel
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solucion
```shell
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 14:29 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000099s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.11 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
...
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
    Session-ID: 682F83BD2C8D939A9D161CBEFDCFAC7FEE72B057AEE1609D25D418811F4CF44C
    Session-ID-ctx: 
    Resumption PSK: 2FF4764644B931D5E022B6F108BF394CDDFBD35062F2A6123D5CF2654BCC8424E21FCE2C36B1B452E0F8962A9BD20E2B
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 8e 8a ea cd 9f 1a 29 9b-77 96 09 e8 50 9c 4c ad   ......).w...P.L.
    0020 - 93 a7 f4 03 6a f2 d8 b8-c7 a3 89 08 3e 31 7d 13   ....j.......>1}.
    0030 - cf 99 52 8e 47 fa 03 25-79 f8 66 d3 57 6d 29 74   ..R.G..%y.f.Wm)t
    0040 - 30 a4 2d ef f4 47 18 bb-89 02 8d 30 59 47 15 43   0.-..G.....0YG.C
    0050 - f9 93 cd b8 e3 27 08 97-4d 33 11 93 4d 31 a0 85   .....'..M3..M1..
    0060 - 4e 97 ef e4 56 55 55 f4-a8 71 83 f8 32 e9 ad 44   N...VUU..q..2..D
    0070 - 82 19 e1 d9 64 9f cd de-04 7b c8 c9 83 2c a7 e0   ....d....{...,..
    0080 - 96 6f 23 cf 84 23 fb b1-2c a0 7f af dc 6a 1e f9   .o#..#..,....j..
    0090 - 27 c0 05 5c ce dd e0 a0-de fc 19 e2 42 37 74 34   '..\........B7t4
    00a0 - 2f f5 fa 2b 97 da a0 f8-47 d6 b9 21 5d 53 25 e3   /..+....G..!]S%.
    00b0 - 9f c6 4f b7 8e 2d e5 4b-7b 36 35 72 d9 6b 8e c8   ..O..-.K{65r.k..
    00c0 - 88 cb 4b 38 8d e1 3a fe-ba 30 d1 31 40 b1 69 f5   ..K8..:..0.1@.i.

    Start Time: 1677162596
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
    Session-ID: 66651428022CC40E8F3FC89E68D81519E8F7CF3AF1D48BE18E5C231E40CB056A
    Session-ID-ctx: 
    Resumption PSK: 21387D5E38F8455F41D0DD64229F1D508C08AAC0D2F7D2331A0596CFE0242D3DAEF0C97A958A37E5015217B1E50601D4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 19 79 b0 e0 91 48 75 10-53 66 8d 53 df 96 59 58   .y...Hu.Sf.S..YX
    0020 - 16 97 a3 17 eb 15 26 76-ad 6b 62 63 44 58 06 b7   ......&v.kbcDX..
    0030 - 0c 9a c7 7e f9 dd ed 90-85 56 ec a6 d2 cf c8 64   ...~.....V.....d
    0040 - b8 ac 0a 09 69 2d ad 6d-24 b2 97 ce f3 36 d0 5f   ....i-.m$....6._
    0050 - 1f 13 a5 ea a0 ec 02 8b-26 2b 18 95 49 9f 0d f1   ........&+..I...
    0060 - 5b c7 d0 54 ea 80 20 14-93 c7 7d 88 ed 31 df 5f   [..T.. ...}..1._
    0070 - 4d 8c 3a 9c f6 2a c6 33-e7 ea 89 0b 8a 40 f3 57   M.:..*.3.....@.W
    0080 - dc 1c 5f 23 37 5d 3b 20-99 50 c6 91 21 f9 19 fb   .._#7]; .P..!...
    0090 - f7 5e 73 91 ef e4 18 da-ab 0e 32 fc 7c d1 0c d8   .^s.......2.|...
    00a0 - f5 c3 0b 1e 36 34 a0 99-f6 f7 ed e2 41 64 17 c4   ....64......Ad..
    00b0 - df d6 7d 8c 79 b1 ba 06-f5 69 fe ae 3e 16 88 e8   ..}.y....i..>...
    00c0 - 2f b4 07 78 12 35 bd 20-96 65 db 1c 21 e6 ef 4f   /..x.5. .e..!..O

    Start Time: 1677162596
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

closed
bandit16@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
                                                                             
┌──(kali㉿kali)-[~]
└─$ nano otrallave.txt
                                                                             
┌──(kali㉿kali)-[~]
└─$ chmod 600 otrallave.txt
                                                                             
                                                                             
┌──(kali㉿kali)-[~]
└─$ ssh -i otrallave.txt  bandit17@bandit.labs.overthewire.org -p 2220
 
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ exit
```
## Notas adicionales
Reemplaza la dirección IP con la dirección IP del sistema que está probando. Este es el formato básico para Nmap

## Referencias
-  [Port scanner on Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)
