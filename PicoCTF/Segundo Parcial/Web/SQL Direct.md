## Objetivo
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Solución
```
catnap-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 55982 -U postgres pico
Password for user postgres: 
psql (14.11 (Ubuntu 14.11-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# c
pico-# a
pico-# ls
pico-# help
Use \? for help or press control-C to clear the input buffer.
pico-# \?
pico-# select
pico-# select *
pico-# \?
pico-# \g select
ERROR:  syntax error at or near "c"
LINE 1: c
        ^
pico=# \g select *
\g: extra argument "*" ignored
ERROR:  syntax error at or near "c"
LINE 1: c
        ^
pico=# \g select; 
ERROR:  syntax error at or near "c"
LINE 1: c
        ^
pico=# \g select;
ERROR:  syntax error at or near "c"
LINE 1: c
        ^
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from public.flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
```
## Notas adicionales
## Referencias