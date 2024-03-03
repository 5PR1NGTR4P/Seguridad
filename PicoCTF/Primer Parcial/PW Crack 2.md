## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Solución
```
catnap-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.py
--2024-03-03 04:57:02--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                                 100%[==================================================================================================================================>]     914  --.-KB/s    in 0s      

2024-03-03 04:57:02 (445 MB/s) - 'level2.py' saved [914/914]

catnap-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2024-03-03 04:57:11--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                                       100%[==================================================================================================================================>]      31  --.-KB/s    in 0s      

2024-03-03 04:57:12 (1.06 MB/s) - 'level2.flag.txt.enc' saved [31/31]

catnap-picoctf@webshell:~$ nano level2.py 
catnap-picoctf@webshell:~$ python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)')
chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)
>>> print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
39ce
>>> 
KeyboardInterrupt
>>> exit()
catnap-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
## Notas adicionales
## Referencias