## Objetivo
A message has come in but it seems to be all scrambled. Luckily it seems to have the key at the beginning. Can you crack this substitution cipher? Download the message [here](https://artifacts.picoctf.net/c/152/message.txt).
## Solución
```
Usamos cyberchef con las letras del principio:

Hereupon Legrand arose, with a grave and stately air, and brought me the beetle
from a glass case in which it was enclosed. It was a beautiful scarabaeus, and, at
that time, unknown to naturalists—of course a great prize in a scientific point
of view. There were two round black spots near one extremity of the back, and a
long one near the other. The scales were exceedingly hard and glossy, with all the
appearance of burnished gold. The weight of the insect was very remarkable, and,
taking all things into consideration, I could hardly blame Jupiter for his opinion
respecting it.

The flag is: picoCTF{5UB5717U710N_3V0LU710N_59533A2E}
```
## Notas adicionales
## Referencias
- https://gchq.github.io/CyberChef/#recipe=Substitute('DECKFMYIQJRWTZPXGNABUSOLVH','ABCDEFGHIJKLMNOPQRSTUVWXYZ',true)&input=SWZuZnV4cHogV2Z5bmR6ayBkbnBhZiwgb3FiaSBkIHluZHNmIGR6ayBhYmRiZnd2IGRxbiwgZHprIGVucHV5aWIgdGYgYmlmIGVmZmJ3ZgptbnB0IGQgeXdkYWEgY2RhZiBxeiBvaXFjaSBxYiBvZGEgZnpjd3BhZmsuIFFiIG9kYSBkIGVmZHVicW11dyBhY2RuZGVkZnVhLCBkemssIGRiCmJpZGIgYnF0ZiwgdXpyenBveiBicCB6ZGJ1bmR3cWFiYeKAlHBtIGNwdW5hZiBkIHluZmRiIHhucWhmIHF6IGQgYWNxZnpicW1xYyB4cHF6YgpwbSBzcWZvLiBCaWZuZiBvZm5mIGJvcCBucHV6ayBld2RjciBheHBiYSB6ZmRuIHB6ZiBmbGJuZnRxYnYgcG0gYmlmIGVkY3IsIGR6ayBkCndwenkgcHpmIHpmZG4gYmlmIHBiaWZuLiBCaWYgYWNkd2ZhIG9mbmYgZmxjZmZrcXp5d3YgaWRuayBkemsgeXdwYWF2LCBvcWJpIGR3dyBiaWYKZHh4ZmRuZHpjZiBwbSBldW56cWFpZmsgeXB3ay4gQmlmIG9mcXlpYiBwbSBiaWYgcXphZmNiIG9kYSBzZm52IG5mdGRucmRld2YsIGR6aywKYmRycXp5IGR3dyBiaXF6eWEgcXpicCBjcHphcWtmbmRicXB6LCBRIGNwdXdrIGlkbmt3diBld2R0ZiBKdXhxYmZuIG1wbiBpcWEgcHhxenFwegpuZmF4ZmNicXp5IHFiLgoKQmlmIG13ZHkgcWE6IHhxY3BDQk17NVVFNTcxN1U3MTBaXzNTMFdVNzEwWl81OTUzM0QyRn0&oenc=65001