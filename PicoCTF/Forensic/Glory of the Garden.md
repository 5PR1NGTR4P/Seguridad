## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Solución
```
┌──(kali㉿kali)-[~]
└─$ mkdir picoCTF                                   
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ cd picoCTF 
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/picoCTF]
└─$ mkdir Jardin
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/picoCTF]
└─$ cd Jardin  
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/picoCTF/Jardin]
└─$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2024-03-12 14:15:19--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg                                                 100%[========================================================================================================================================>]   2.19M  3.10MB/s    in 0.7s    

2024-03-12 14:15:20 (3.10 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

┌──(kali㉿kali)-[~/picoCTF/Jardin]
└─$ strings garden.jpg | grep "pico"
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```
## Notas adicionales
También podemos usar hexeditor para buscar la bandera
## Referencias
