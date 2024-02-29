## Objetivo
Run the Python script `code.py` in the same directory as `codebook.txt`.
## Solución
```
catnap-picoctf@webshell:~$ mkdir codigo
catnap-picoctf@webshell:~$ cd codigo/
catnap-picoctf@webshell:~/codigo$ wget https://artifacts.picoctf.net/c/3/code.py
--2024-02-28 04:03:36--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                                   100%[==================================================================================================================================>]   1.25K  --.-KB/s    in 0s      

2024-02-28 04:03:37 (810 MB/s) - 'code.py' saved [1278/1278]

catnap-picoctf@webshell:~/codigo$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2024-02-28 04:03:45--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                              100%[==================================================================================================================================>]      27  --.-KB/s    in 0s      

2024-02-28 04:03:45 (10.9 MB/s) - 'codebook.txt' saved [27/27]
catnap-picoctf@webshell:~/codigo$ python3 code.py 
picoCTF{c0d3b00k_455157_197a982c}
```
## Notas adicionales
## Referencias