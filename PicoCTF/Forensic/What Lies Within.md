## Objetivo
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Solución
```
Ingresamos la imagen en el decodificador online y nos arroja la bandera:
picoCTF{h1d1ng_1n_th3_b1t5}

O podemos usar zsteg:

┌──(kali㉿kali)-[~/picoCTF/WLW]
└─$ zsteg -a buildings.png | grep "pico"
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

```
## Notas adicionales
## Referencias
https://stylesuxx.github.io/steganography/