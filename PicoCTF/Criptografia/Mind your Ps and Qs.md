## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values)
## Solución
```
Decrypt my super sick RSA:
c: 240986837130071017759137533082982207147971245672412893755780400885108149004760496
n: 831416828080417866340504968188990032810316193533653516022175784399720141076262857
e: 65537

Usamos un decriptador online:
picoCTF{sma11_N_n0_g0od_23540368}

Otra forma:
┌──(kali㉿kali)-[~]
└─$ wget https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values
--2024-04-16 14:13:17--  https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 205 [application/octet-stream]
Saving to: ‘values’

values             100%[===============>]     205  --.-KB/s    in 0s      

2024-04-16 14:13:23 (423 MB/s) - ‘values’ saved [205/205]

                                                                           
┌──(kali㉿kali)-[~]
└─$ cat values          
Decrypt my super sick RSA:
c: 240986837130071017759137533082982207147971245672412893755780400885108149004760496
n: 831416828080417866340504968188990032810316193533653516022175784399720141076262857
e: 65537                                                                           
┌──(kali㉿kali)-[~]
└─$ python3           
Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> p=  1593021310640923782355996681284584012117
>>> q=  521911930824021492581321351826927897005221
>>> e=
KeyboardInterrupt
>>> e=65537
>>> c=240986837130071017759137533082982207147971245672412893755780400885108149004760496
>>> n=831416828080417866340504968188990032810316193533653516022175784399720141076262857
>>> tn = (p-1)*(q-1)
>>> d=pow(e,-1,tn)
>>> m=pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639592405461024281868413
>>> bytes.fromhex( hex(m)[2:] )
b'picoCTF{sma11_N_n0_g0od_23540368}'
>>> 

```
## Notas adicionales
## Referencias
https://www.dcode.fr/rsa-cipher