## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solución
```
┌──(kali㉿kali)-[~/tercerReich]
└─$ nano utf.py                
                                                                           
┌──(kali㉿kali)-[~/tercerReich]
└─$ wget https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc                
--2024-05-12 01:17:18--  https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 57 [application/octet-stream]
Saving to: ‘enc’

enc                100%[===============>]      57  --.-KB/s    in 0s      

2024-05-12 01:17:18 (132 MB/s) - ‘enc’ saved [57/57]

                                                                           
┌──(kali㉿kali)-[~/tercerReich]
└─$ python utf.py     
Flag: picoCTF{16_bits_inst34d_of_8_26684c20}

```
## Notas adicionales
## Referencias