## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solución
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt
kjIuqjobFBhKw9Mmfj2wAnWbXB2VxSfv
5Y76FifuxKStZi4CVovF2uPhgLrZnLzG
AiYd84lOOVTA4gqJPX7f6DH8eG3zwq1W
A16BW831T94qcsYcGDSkgzYhxnX2xUdK
vlsSKqk3yVx2PZxIkBuZPR3KKIf8hGi1
cEqNrEqHVIIi9fQKdcvAxaip1brmsSxT
FQIgwPiuPKftkFhIy9Nzm94sWdNGTlHd
P8jd7Kr8GXVKTLhe1Y7cVYAARwh4lN4A
Rlaj8VWIHkYsAg42TsFplgAd4ekjgR2X
365RauAVsFlxktPMpoLtIf1uxijU1TfV

...

b0XUx8jfeWYAUGlnOGGAyVRxdNziM4SF
mTYRseor14aRwbazgTmVVgM4mDOkZJJ4
euIPhAiMI8n0DxPCbaAhJ9RTBO3fX4UE
eJZcdtHKg9jLpvpK9v31Fj1opqlA1A9k
Dml3j9ydZQj13Q6xVRPHVuMhD9pt0NbT
qtUQnuIjoLTNwviHPE6yULyPEVUuag5K
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Notas adicionales
Usando sort en conjunto con uniq -u nos permite recuperar aquellas lineas que solo se repiten una sola vez
Si usamos -c con uniq nos permite ver la cantidad de repeticiones de cada string
## Referencias
- [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)