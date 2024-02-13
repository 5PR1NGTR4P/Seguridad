## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solución
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ cat data.txt | grep ====
grep: (standard input): binary file matches
bandit9@bandit:~$ strings data.txt | grep ====
x]T========== theG)"
========== passwordk^
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas adicionales
strings nos permite encontrar cadenas de texto en archivos binarios
## Referencias
- https://es.wikipedia.org/wiki/Strings_(Unix)#:~:text=strings%20es%20un%20programa%20de,objeto%20y%20volcados%20de%20memoria.