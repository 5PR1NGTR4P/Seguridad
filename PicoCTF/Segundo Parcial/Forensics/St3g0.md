## Objetivo
Download this image and find the flag.
- [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)
## Solución
```
┌──(kali㉿kali)-[~/parcial2/tiburon]
└─$ zsteg -a pico.flag.png | grep pico  
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a1062667}$t3g0"
```
## Notas adicionales
## Referencias