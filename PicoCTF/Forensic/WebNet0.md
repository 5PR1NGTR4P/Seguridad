## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
```
Cargamos la llave en el protocolo para que desencripte la informacion y finalmente solo seguimos el stream:

picoCTF{nongshim.shrimp.crackers}

Otra forma seria usando este comando:
ssldump -r capture.pcap -k picopico.key -d | grep pico -A3
```
## Notas adicionales
## Referencias