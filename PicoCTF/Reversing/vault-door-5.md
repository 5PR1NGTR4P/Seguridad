## Objetivo
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/9505cca05dc00fecead41106370ee619/VaultDoor5.java)
## Solución
```
Usamos cyberchef para quitarle el base 64 y posteriormente hacerle url decode:

c0nv3rt1ng_fr0m_ba5e_64_84fd5095

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_84fd5095}
```
## Notas adicionales
## Referencias
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm0NCkpUWTJKVGN5SlRNd0pUWmtKVFZtSlRZeUpUWXhKVE0xSlRZMUpUVm1KVE0yDQpKVE0wSlRWbUpUTTRKVE0wSlRZMkpUWTBKVE0xSlRNd0pUTTVKVE0x&ieol=CRLF&oeol=CRLF
