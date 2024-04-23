## Objetivo
What does asm1(0x8be) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/66c927e32f3d7be7a62d13a7c2250943/test.S)
## Solución
```
PILA    
000 alta

[ebp]< esp < ebp
[ret]< ebp + 0x4
[0x8be]< ebb + 0x8
[eax] < 0x8be 


>>> 0x8be != 0x8be
False
>>> hex(0x8be-0x3)
'0x8bb'
```
## Notas adicionales
## Referencias
