## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.
## Solución
```
Usamos ghidra para entender el codigo desensamblado:

creamos un archivo python para reversear la bandera:
d= open("rev_this").read()
bandera=""
for j in range(8,23):
	if j & 1 == 0:
		bandera+=chr(ord(d[j])-5)
	else:
		bandera+=chr(ord(d[j])+2)
print(bandera)

┌──(kali㉿kali)-[~/gdb]
└─$ python banderosa.py 
r3v3rs312528e05

picoCTF{r3v3rs312528e05}
```
## Notas adicionales
## Referencias