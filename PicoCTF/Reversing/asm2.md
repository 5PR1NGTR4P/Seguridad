## Objetivo
What does asm2(0xb,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/717467c8c8b4332ea5873ad8fe7b2dad/test.S)
## Solución
```
d=46
e=11
while e <=25587:
	d++
	e+=128
print(d)
hex(d)
0xf6
```
## Notas adicionales
## Referencias
- https://m0v-f0rward.medium.com/solving-asm1-and-asm2-from-picoctf-8cd915faf637