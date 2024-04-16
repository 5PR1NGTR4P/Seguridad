## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
```
num.py:
numeros= open("message.txt").read().split()
modulos=[]

for numero in numeros:
	modulos.append(int(numero)%37)

bandera=""

for modulo in modulos:
	if modulo>=0 and modulo<=25:
		c=chr(modulo+65)
		bandera=bandera+c
	elif modulo>=26 and modulo<=35:
		digito=modulo-26
		bandera=bandera+str(digito)
	else:
		bandera=bandera+"_";

print(bandera)

┌──(kali㉿kali)-[~]
└─$ python num.py
R0UND_N_R0UND_ADD17EC2

picoCTF{R0UND_N_R0UND_ADD17EC2}
```
## Notas adicionales
## Referencias