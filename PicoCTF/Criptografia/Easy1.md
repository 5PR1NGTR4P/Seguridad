## Objetivo
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.
## Solución
```
Utilizamos vigenere con cyberchef para resolver el mensaje:

UFJKXQZQUNB
SOLVECRYPTO
	 |
	 v
CRYPTOISFUN

picoCTF{CRYPTOISFUN}
```
## Notas adicionales
## Referencias
- https://gchq.github.io/CyberChef/#recipe=Vigenère_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkI