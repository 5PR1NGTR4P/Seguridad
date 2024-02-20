## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEIivS1jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC4
XC9dgne8ha9I/vXn4uTtObLhI/PPyLyl4jyDQPp61VtsEMcOb95KhXxdtQiDtzSD
3KXQVFLaPlVGKDWSR9nV+GoazSNPmNLH/IMVrUYxXjYikPxo1jjYKyuqfjV5bNm3
Hz6z4eDl7wNbPRaPAMPo0WU23m9M04bKQHLINfN7Abz3a+7ChLeICrWXiXp9mWfj
PY8cK7Vayz0eHU4Lg64q4jUaXQqZ/ta1RqZEwv7ZuTKctcazpK/u2+h4zvQCPyLh
uDjUXZTLlIuhfjyKUJLQsmYHAQprV6sY3ybFN32dW6MSE0/ApT6Th0LzKeaYxk5b
3NIeaYyPeKsjqFSwy+2zAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBQ
RXG1k+cB357X43fsiyaCQQh4RbWHOcg1jBes5eiC/H8MyC3ec1znXvOUfqJcWNQJ
9UJDMwbkpo+IcwJiOe9n/D3Zeypv1g+ta8KKLsQ+zcbp5RdltKy7GuO/s5WjVofE
/IHz/5g+IMoqqYLlquQ539CZykPMC9TB9uWfJj/i8faCox4gjtkSCri+27tUZuHi
eYR3zxY1ptsJti/pMaItC6Oc2/pSlotQ4fXdciLZYGXqlmSFBt8Y8/v1YkhME5gN
3HmBV/Zg1SghA57zYsbf3npvQwudr04f2iF493pe0VRN6DfiXTxWkJe1VKuyGHEr
Q4L4OdVlgMSeyYyKgFc7
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
    Session-ID: A27E150FBC333BFDFF0C9A1DD47F6A1045501662BC7849CC4CC2F59D7233925B
    Session-ID-ctx:
    Resumption PSK: FED0C5D2C2AEBE4C092620BD83CB76545CBD7BB70F94C78A01465BFCC6104A008EA9C25D1314280EDBB45EDBF8754567
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - 55 f5 20 99 af 60 ab 8e-a6 f8 62 84 41 cb 29 28   U. ..`....b.A.)(
    0020 - 74 65 f4 e5 9b d9 de aa-cb a7 fe 42 dc b0 fb 0b   te.........B....
    0030 - ef 31 cb d1 39 39 c2 91-cc de 1a 28 5c b8 ae 46   .1..99.....(\..F
    0040 - 37 9c d2 b5 97 c5 03 76-79 28 66 1c 6b 88 cb 9a   7......vy(f.k...
    0050 - a2 d2 04 e6 91 68 5a bb-0c 1b 0c 15 2a ba 90 6d   .....hZ.....*..m
    0060 - 56 e1 2b 0d 36 8a 2a 5d-e2 a5 79 20 05 66 3b 14   V.+.6.*]..y .f;.
    0070 - 3f 0c c4 ad db bb 01 b1-c9 7f 5c 5c e1 3a 3b 66   ?.........\\.:;f
    0080 - 2d 42 21 e2 56 36 7f 11-e7 a2 da 90 d8 37 2b ae   -B!.V6.......7+.
    0090 - f7 bf 49 e7 9a 2c 51 d1-2d e3 65 f9 1e d5 69 40   ..I..,Q.-.e...i@
    00a0 - 70 ff a8 24 b1 e8 25 09-83 d0 f1 5e 74 91 9b 44   p..$..%....^t..D
    00b0 - 9d b5 3c 4c 63 0e c9 bc-e5 32 70 06 62 00 b9 49   ..<Lc....2p.b..I
    00c0 - 1b fb ee d7 04 b7 6e 95-a1 04 45 b2 a0 04 fe 13   ......n...E.....

    Start Time: 1708457112
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
    Session-ID: C8E6CC91B2E8F23B2206E7E83FA27A0BE99CECE5B3B5E694BFF44390DBE72CFA
    Session-ID-ctx:
    Resumption PSK: 1BA0086EF8BFA8A51E28ADAD38554A2C9370DFA03BC310B6DD09C8B4BA254B4CDB297C349E707666FB682859C0EA99D2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - 45 c2 38 ee c1 4e 2f ae-b9 ce 37 f8 56 25 5f 2a   E.8..N/...7.V%_*
    0020 - 40 92 eb 95 1a 45 41 c8-d1 96 91 ac 2c d6 ee b4   @....EA.....,...
    0030 - 56 fe cd 20 58 fc 35 a1-1c ee 1f f6 1e 70 1c 03   V.. X.5......p..
    0040 - 99 3c f7 0f 4b 50 db 4c-8e eb 14 cf a9 ec f8 54   .<..KP.L.......T
    0050 - bd ca df 21 75 2d 75 63-15 37 8a e6 eb aa 39 a2   ...!u-uc.7....9.
    0060 - 9f b2 3c 36 0f f4 4b 15-b5 f6 2d 99 09 f8 82 e7   ..<6..K...-.....
    0070 - 73 98 16 f6 5e ab 1c f6-1b ec 99 ef 0e aa 26 88   s...^.........&.
    0080 - fc 82 b8 14 64 1c cf 0a-da d0 c2 c7 21 03 75 95   ....d.......!.u.
    0090 - 8a 75 cd 6d 55 b6 3e 43-b9 40 bc 21 30 13 dd 34   .u.mU.>C.@.!0..4
    00a0 - 56 17 8c 3d c9 35 c2 f6-91 ad d1 ce 50 75 0f 5d   V..=.5......Pu.]
    00b0 - 39 1f aa 86 d0 9b a1 2f-d5 86 63 e1 9e e9 c8 a3   9....../..c.....
    00c0 - 22 33 e4 ba 59 82 68 30-ca 08 83 e9 f2 45 19 14   "3..Y.h0.....E..

    Start Time: 1708457113
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
- [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)