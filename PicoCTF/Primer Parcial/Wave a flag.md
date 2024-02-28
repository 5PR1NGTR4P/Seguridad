## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...
## Solución
```
catnap-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
--2024-02-27 18:35:18--  https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                      100%[==================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2024-02-27 18:35:18 (350 MB/s) - 'warm' saved [10936/10936]

catnap-picoctf@webshell:~$ ls
README.txt  flag  warm
catnap-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=985d9586d46e8651ab66c2fbb5a5473492466aa3, with debug_info, not stripped
catnap-picoctf@webshell:~$ ./warm 
-bash: ./warm: Permission denied
catnap-picoctf@webshell:~$ chmod +x warm 
catnap-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
catnap-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
```
## Notas adicionales
chmod cambia los permisos de archivo
## Referencias