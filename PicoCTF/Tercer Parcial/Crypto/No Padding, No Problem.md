## Objetivo
	Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 30048`.
## Solución
```
┌──(kali㉿kali)-[~]
└─$ touch spiderDance.py

spiderDance.py:
from pwn import *


def integer_to_bytes(integer, _bytes):
    output = bytearray()
    for byte in range(_bytes):
        output.append((integer >> (8 * (_bytes - 1 - byte))) & 255)
    return output


conn = remote('mercury.picoctf.net', 60368)
conn.recvuntil("n: ")
n = int(conn.recvline().decode('utf-8'))
conn.recvuntil("e: ")
e = int(conn.recvline().decode('utf-8'))
conn.recvuntil("ciphertext: ")
c = int(conn.recvline().decode('utf-8'))
evil = pow(2, e, n)
encrypted = str(evil * c)
conn.sendline(encrypted.encode('utf-8'))
conn.recvuntil("go: ")
p = int(conn.recvline().decode('utf-8')) // 2
print(bytes.fromhex(hex(p)[2:]).decode('utf-8'))

┌──(kali㉿kali)-[~]
└─$ python spiderDance.py 
[*] Checking for new versions of pwntools
    To disable this functionality, set the contents of /home/kali/.cache/.pwntools-cache-3.11/update to 'never' (old way).
    Or add the following lines to ~/.pwn.conf or ~/.config/pwn.conf (or /etc/pwn.conf system-wide):
        [update]
        interval=never
[*] You have the latest version of Pwntools (4.12.0)
[+] Opening connection to mercury.picoctf.net on port 30048: Done
/home/kali/spiderDance.py:12: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.recvuntil("n: ")
/home/kali/spiderDance.py:14: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.recvuntil("e: ")
/home/kali/spiderDance.py:16: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.recvuntil("ciphertext: ")
/home/kali/spiderDance.py:21: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  conn.recvuntil("go: ")
picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_5052620}
[*] Closed connection to mercury.picoctf.net port 30048
```
## Notas adicionales
## Referencias