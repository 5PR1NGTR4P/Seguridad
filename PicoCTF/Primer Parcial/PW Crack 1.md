## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.
## Solución
```
catnap-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.py
--2024-03-03 04:52:54--  https://artifacts.picoctf.net/c/10/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                                 100%[==================================================================================================================================>]     876  --.-KB/s    in 0s      

2024-03-03 04:52:54 (397 MB/s) - 'level1.py' saved [876/876]

catnap-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
--2024-03-03 04:53:06--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                       100%[==================================================================================================================================>]      30  --.-KB/s    in 0s      

2024-03-03 04:53:06 (13.5 MB/s) - 'level1.flag.txt.enc' saved [30/30]

catnap-picoctf@webshell:~$ level1.py
-bash: level1.py: command not found
catnap-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: level.flag.txt.enc
That password is incorrect
catnap-picoctf@webshell:~$ cat level1.
level1.flag.txt.enc  level1.py            
catnap-picoctf@webshell:~$ cat level1.flag.txt.enc 
FPR
   umw
iK
_i
  UDcatnap-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: FPR
   umw
iK
_iThat password is incorrect
catnap-picoctf@webshell:~$    umw
-bash: umw: command not found
catnap-picoctf@webshell:~$ iK
-bash: iK: command not found
catnap-picoctf@webshell:~$ nano level1.py 
catnap-picoctf@webshell:~$ python level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
```
## Notas adicionales
## Referencias