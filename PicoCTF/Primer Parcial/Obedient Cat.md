## Objetivo
This file has a flag in plain sight (aka "in-the-clear").
## Solución
```
catnap-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag
--2024-02-27 18:27:17--  https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                      100%[==================================================================================================================================>]      34  --.-KB/s    in 0s      

2024-02-27 18:27:17 (12.6 MB/s) - 'flag' saved [34/34]
          
catnap-picoctf@webshell:~$ cat 
.bash_logout  .bashrc       .profile      .wget-hsts    README.txt    flag          
catnap-picoctf@webshell:~$ cat flag 
picoCTF{s4n1ty_v3r1f13d_28e8376d}
```
## Notas adicionales
wget nos permite descargar archivos
## Referencias