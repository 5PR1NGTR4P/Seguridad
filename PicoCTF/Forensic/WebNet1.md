## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
```
Cargamos la llave en el protocolo para que desencripte la informacion y finalmente solo seguimos el stream y encontramos la bandera dentro de la imagen:

picoCTF{honey.roasted.peanuts}

Otra forma seria exportar la imagen y aplicarle este comando:
strings -n 10 vulture.jpg | grep pico
```
## Notas adicionales
## Referencias