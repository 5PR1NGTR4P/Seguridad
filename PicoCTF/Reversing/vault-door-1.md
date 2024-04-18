## Objetivo
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)
## Solución
```
Recuperamos la bandera de la funcion checkPassword:
d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4

picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4}

Otra forma:
cat flag | sort | awk '{print $3}' | tr -d "'" | tr -d "\n"
```
## Notas adicionales
## Referencias