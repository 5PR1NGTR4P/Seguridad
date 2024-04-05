## Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:50920/) and see what you can discover.
## Solución
```
Entramos al javascript y podemos visualizar la funcion que valida el login:
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}

Asi que solo utilizamos esas credenciales para acceder:
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
```
## Notas adicionales
## Referencias