## Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:56615/) out.
## Solución
```
Primero entramos a robots.txt y encontraremos un mensaje codificado en hexadecimal que al descifrarlo nos dara otra url js/myfile.txt:
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
```
## Notas adicionales
## Referencias
- https://gchq.github.io/CyberChef/#recipe=From_Quoted_Printable()From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=DQphbk12YlhsbWFXeGxMblI0ZEE9PQ&ieol=CRLF&oeol=VT