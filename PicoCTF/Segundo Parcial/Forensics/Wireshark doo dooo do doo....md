## Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/d6f9aa16d2a2c51d2e431e658d87af9e/shark1.pcapng).
## Solución
```
Seguimos el stream de http y vemos un texto parecido al formato de la bandera:
Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}

Aplicamos descifrado Rot 13:
The flag is picoCTF{p33kab00_1_s33_u_deadbeef}
```
## Notas adicionales
## Referencias
- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=R3VyIHN5bnQgdmYgY3ZwYlBHU3tjMzN4bm8wMF8xX2YzM19oX3FybnFvcnJzfQ