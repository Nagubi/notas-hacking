# Bandit Level 15 → Level 16
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solucion
```shell
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 06:19:29 2023 GMT; NotAfter: Feb 21 06:20:29 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEA7qUdzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMDYxOTI5WhcNMjMwMjIxMDYyMDI5WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDL
vM0gZzAHdXTeD5t4ruUJo/kRs4UAodA9XcqDhNtW464W0c55RqKLp921syy3Lvjr
8Q9WkqvCFX+efShMd8XnzbT/dyRrD+cZQnSiPJ3bwDdpwqfkl9h3mb609Kb5HI6R
JgogEyuRLJI+HKtr/wXHwo1vBZ0+yaPMX6sdkd6Hu5Ra0L5Q5+E5+3F/8QgvCeVE
hDRIOrh2a7jxykb8G6+xVC6jIZY0YfrZz6LrESyQau256pqyaQPqQoUWTlitxIql
Ym2Baw7vYDxmFZrvj0FkumC6NokX6K2G9bZ0DaKR/DspPdAC4oT81SawJvsBibdN
51VI6dxBn412ZS8bS155AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQA9
skxWNwZbedjaVTa5yMPUZQ4Nf5/LAAMtS5Q7mzGH5tdQsTGR0Z4n4eA4hzrmzHBF
MVRL5mR9n+sM5pIrKDa6f4zIc5ObxDyN19ie+3SFASCPz9tihK8Js2V8qsR6LHV1
pfD8DSG0hZPtUuK3Mfi+nWqQUFiiTGj30mb9vlS1sSWv5PGznou1gQ3ZfrDs7B4K
ZKZrllPIVV1CrlDw2Bv8Dc432LQuZAmKAjBd6FG0OAboU/WJMTwAfVjlKMtvC8tg
DZ3djSTprq6PrXlI0utw/MsMIh69b61BRXUuDvRxhU11SNmSI8aegjVL8KuK+Euh
sSLPTocV29SY1YXOwEQi
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
    Session-ID: 0FED1EEEBE7AEA69247568BBD64349BBA4DCBE608CFD36C17CCEC9ACB01706C7
    Session-ID-ctx: 
    Resumption PSK: 11627887FFC97218ECEAB79C1A5CF77BC8EBB6F37A9D3791B20A640989B7B7C71B748E999718861967E27E79C7E755CB
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 52 19 0d 6f 23 ec 15 76-56 b3 0e c6 14 8b 60 98   R..o#..vV.....`.
    0020 - 81 fd 14 fc 16 61 08 00-65 bb 24 78 97 f4 0a 86   .....a..e.$x....
    0030 - 5a 1a 32 2a 0c af df ef-1b 8e 94 96 a5 61 24 6e   Z.2*.........a$n
    0040 - b7 bd 7b 3c 75 80 50 c3-33 f7 16 77 02 39 c8 f3   ..{<u.P.3..w.9..
    0050 - 43 0e 9e 58 0b c8 18 74-76 81 91 81 b9 07 f6 7f   C..X...tv.......
    0060 - 84 b3 93 c2 7d 02 de 48-1f b2 07 f9 d7 6b 1d 18   ....}..H.....k..
    0070 - 2f b5 47 06 3e 44 96 6d-24 88 47 9c 03 a9 21 87   /.G.>D.m$.G...!.
    0080 - 93 53 75 c9 7d 33 2b 18-23 af 56 7f b7 31 61 d7   .Su.}3+.#.V..1a.
    0090 - 75 0c 00 c1 34 c3 1d 5e-7c 73 ce 66 93 a5 d7 8e   u...4..^|s.f....
    00a0 - 01 15 f8 54 a4 07 6b 81-6e 4e f4 b5 9c 6a b0 b1   ...T..k.nN...j..
    00b0 - 19 25 ab 21 4e 43 8d a8-bc 73 26 9c 3b 3b aa cf   .%.!NC...s&.;;..
    00c0 - 41 29 4b c3 b3 80 dc 25-77 be 29 85 6c f2 3f d8   A)K....%w.).l.?.

    Start Time: 1676992868
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
    Session-ID: 1E57A1C8F2A7F27748B50EAB4E37EE4BC35D8F62B30F414DAA771B94099C34A0
    Session-ID-ctx: 
    Resumption PSK: 0001E58F2A38D95589CFF78959710A16E3D5A31FD00C21EC2F27A5373433A10AC8EC0FEF80C337E6995504099586AD01
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 17 91 3e d5 b3 cc 18 51-c4 1f 0f f7 40 0b cc 5e   ..>....Q....@..^
    0020 - 3a 33 43 b7 06 cf 43 74-7f 6e f6 08 cc 16 9c 1e   :3C...Ct.n......
    0030 - 67 b6 75 c2 b1 fb 34 57-1a cd 04 c8 a9 77 25 4f   g.u...4W.....w%O
    0040 - d9 06 8e 9f 7b 77 49 51-a4 a6 c3 fa 86 1b 98 6b   ....{wIQ.......k
    0050 - ff dd 8c b3 f5 67 e1 c8-02 51 7f 93 57 af b5 a4   .....g...Q..W...
    0060 - a1 83 7b ce c4 2b 59 3c-49 ff 5b 4b cb 13 d6 96   ..{..+Y<I.[K....
    0070 - e4 5f a4 f5 d6 08 d3 af-ce 32 94 2a b6 0f a8 3e   ._.......2.*...>
    0080 - 92 e3 b3 8c a6 59 5d f7-38 39 91 8d b9 26 4a 59   .....Y].89...&JY
    0090 - d3 4b 59 5c 51 e5 fe 41-0e 13 2f 47 10 f2 b6 1e   .KY\Q..A../G....
    00a0 - 2e df a8 a5 9c c3 b3 18-b1 e3 7a 85 cc 28 d0 9d   ..........z..(..
    00b0 - 8f b7 a1 78 c8 23 fd fe-1e e9 0c 90 19 12 1b 67   ...x.#.........g
    00c0 - bc 2e c3 5c f8 8b a4 60-8e 53 19 a0 48 87 e6 fa   ...\...`.S..H...

    Start Time: 1676992868
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

```
## Notas adicionales


## Referencias
-   [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
-   [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)
