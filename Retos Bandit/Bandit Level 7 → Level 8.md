## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt
gallop  hu3ZhCrGRvfaO5jsY6ttvApzVCA2Hjvs
Aurelia's       ikl4F3cK5m6Cl6HAxva6zUAVJhI2Cvc6
stoicism        JiW9ts44udf20bJHe8H5dS1c99Muwz42
embodies        vWheZcAsQHZNnerI3ViW8wqOKIx0kbgR
Plato   dW2U8E5FfuAvNLdGDupP8GAxr922ZV0x
cultivation     A90E75jvWbEKrijFxM4GxqHEw8c8U2Bf
stable  omR4PHolFwbI0IEJsanveA21yWvFy8a7
bedspread       VlBFxuEDi3phEpljbKbahRJvJxfh3k9M
oppressing      hQTiEm5XF3cUQSEiBjh7sekemLOKBrcJ
darnedest       9O2zdCLKVoW5u34P9T7EKTZXcMRE6xh5

...

fantasying      ZH4NahCM83A2vkjtzg6qrU4KaJ5lvvyV
Leonidas        Fl7NKnhFBepqm0wjfk8y3ZUHf5q4XG51
Lithuanians     5KtYth9tFsyTw4mmPqsFZoAbwuoD362D
Blanchard       vpib3VZxQEoUInEzRwQHUY6vI2ooyyZq
posterior       VdcFhA1HDNyjoJHfWm6XB5qpSxRHnElv
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Notas adicionales
Grep nos permite recuperar un renglón de un texto usando una palabra clave
head muestra las primeras lineas de un archivo
tail muestra las ultimas lineas de un archivo
wc cuenta las lineas de un archivo
## Referencias