## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
catnap-picoctf@webshell:~$ mkdir 333
catnap-picoctf@webshell:~$ cd 333
catnap-picoctf@webshell:~/333$ wget https://artifacts.picoctf.net/c/16/level3.py
--2024-03-03 04:59:45--  https://artifacts.picoctf.net/c/16/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                                 100%[==================================================================================================================================>]   1.31K  --.-KB/s    in 0s      

2024-03-03 04:59:46 (75.8 MB/s) - 'level3.py' saved [1337/1337]

catnap-picoctf@webshell:~/333$ wget https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
--2024-03-03 04:59:52--  https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                                       100%[==================================================================================================================================>]      31  --.-KB/s    in 0s      

2024-03-03 04:59:52 (1.53 MB/s) - 'level3.flag.txt.enc' saved [31/31]

catnap-picoctf@webshell:~/333$ wget https://artifacts.picoctf.net/c/16/level3.hash.bin
--2024-03-03 04:59:58--  https://artifacts.picoctf.net/c/16/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                           100%[==================================================================================================================================>]      16  --.-KB/s    in 0s      

2024-03-03 04:59:58 (7.77 MB/s) - 'level3.hash.bin' saved [16/16]

catnap-picoctf@webshell:~/333$ nano level3.py 
catnap-picoctf@webshell:~/333$ pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
-bash: pos_pw_list: command not found
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: 6997
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: 3ac8
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: f0ac
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: 4b17
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: ec27
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: 4e66    
That password is incorrect
catnap-picoctf@webshell:~/333$ python level3.py 
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
```
## Notas adicionales
## Referencias