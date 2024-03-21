## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!
## Solución
```
┌──(kali㉿kali)-[~/forest]
└─$ wget https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
--2024-03-19 14:31:31--  https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2976 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt      100%[================>]   2.91K  --.-KB/s    in 0s      

2024-03-19 14:31:31 (78.9 MB/s) - ‘whitepages.txt’ saved [2976/2976]

                                                                             
┌──(kali㉿kali)-[~/forest]
└─$ file whitepages.txt                     
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
                                                                             
┌──(kali㉿kali)-[~/forest]
└─$ mousepad whitepages.txt 
                                                                             
┌──(kali㉿kali)-[~/forest]
└─$ sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'
00001010000010010000100101110000011010010110001101101111010000110101010001000110000010100000101000001001000010010101001101000101010001010010000001010000010101010100001001001100010010010100001100100000010100100100010101000011010011110101001001000100010100110010000000100110001000000100001001000001010000110100101101000111010100100100111101010101010011100100010000100000010100100100010101010000010011110101001001010100000010100000100100001001001101010011000000110000001100000010000001000110011011110111001001100010011001010111001100100000010000010111011001100101001011000010000001010000011010010111010001110100011100110110001001110101011100100110011101101000001011000010000001010000010000010010000000110001001101010011001000110001001100110000101000001001000010010111000001101001011000110110111101000011010101000100011001111011011011100110111101110100010111110110000101101100011011000101111101110011011100000110000101100011011001010111001101011111011000010111001001100101010111110110001101110010011001010110000101110100011001010110010001011111011001010111000101110101011000010110110001011111001101110011000100110000001100000011100000110110001100000110001000110000011001100110000100110111001101110011100101100001001101010110001001100100001110000110001101100101001100100011100101100110001100100011010001100110001101010011100000110110011001000110001101111101000010100000100100001001

picoCTF

		SEE PUBLIC RECORDS & BACKGROUND REPORT
		5000 Forbes Ave, Pittsburgh, PA 15213
		picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}
```
## Notas adicionales
## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDAwMDEwMTAwMDAwMTAwMTAwMDAxMDAxMDExMTAwMDAwMTEwMTAwMTAxMTAwMDExMDExMDExMTEwMTAwMDAxMTAxMDEwMTAwMDEwMDAxMTAwMDAwMTAxMDAwMDAxMDEwMDAwMDEwMDEwMDAwMTAwMTAxMDEwMDExMDEwMDAxMDEwMTAwMDEwMTAwMTAwMDAwMDEwMTAwMDAwMTAxMDEwMTAxMDAwMDEwMDEwMDExMDAwMTAwMTAwMTAxMDAwMDExMDAxMDAwMDAwMTAxMDAxMDAxMDAwMTAxMDEwMDAwMTEwMTAwMTExMTAxMDEwMDEwMDEwMDAxMDAwMTAxMDAxMTAwMTAwMDAwMDAxMDAxMTAwMDEwMDAwMDAxMDAwMDEwMDEwMDAwMDEwMTAwMDAxMTAxMDAxMDExMDEwMDAxMTEwMTAxMDAxMDAxMDAxMTExMDEwMTAxMDEwMTAwMTExMDAxMDAwMTAwMDAxMDAwMDAwMTAxMDAxMDAxMDAwMTAxMDEwMTAwMDAwMTAwMTExMTAxMDEwMDEwMDEwMTAxMDAwMDAwMTAxMDAwMDAxMDAxMDAwMDEwMDEwMDExMDEwMTAwMTEwMDAwMDAxMTAwMDAwMDExMDAwMDAwMTAwMDAwMDEwMDAxMTAwMTEwMTExMTAxMTEwMDEwMDExMDAwMTAwMTEwMDEwMTAxMTEwMDExMDAxMDAwMDAwMTAwMDAwMTAxMTEwMTEwMDExMDAxMDEwMDEwMTEwMDAwMTAwMDAwMDEwMTAwMDAwMTEwMTAwMTAxMTEwMTAwMDExMTAxMDAwMTExMDAxMTAxMTAwMDEwMDExMTAxMDEwMTExMDAxMDAxMTAwMTExMDExMDEwMDAwMDEwMTEwMDAwMTAwMDAwMDEwMTAwMDAwMTAwMDAwMTAwMTAwMDAwMDAxMTAwMDEwMDExMDEwMTAwMTEwMDEwMDAxMTAwMDEwMDExMDAxMTAwMDAxMDEwMDAwMDEwMDEwMDAwMTAwMTAxMTEwMDAwMDExMDEwMDEwMTEwMDAxMTAxMTAxMTExMDEwMDAwMTEwMTAxMDEwMDAxMDAwMTEwMDExMTEwMTEwMTEwMTExMDAxMTAxMTExMDExMTAxMDAwMTAxMTExMTAxMTAwMDAxMDExMDExMDAwMTEwMTEwMDAxMDExMTExMDExMTAwMTEwMTExMDAwMDAxMTAwMDAxMDExMDAwMTEwMTEwMDEwMTAxMTEwMDExMDEwMTExMTEwMTEwMDAwMTAxMTEwMDEwMDExMDAxMDEwMTAxMTExMTAxMTAwMDExMDExMTAwMTAwMTEwMDEwMTAxMTAwMDAxMDExMTAxMDAwMTEwMDEwMTAxMTAwMTAwMDEwMTExMTEwMTEwMDEwMTAxMTEwMDAxMDExMTAxMDEwMTEwMDAwMTAxMTAxMTAwMDEwMTExMTEwMDExMDExMTAwMTEwMDAxMDAxMTAwMDAwMDExMDAwMDAwMTExMDAwMDAxMTAxMTAwMDExMDAwMDAxMTAwMDEwMDAxMTAwMDAwMTEwMDExMDAxMTAwMDAxMDAxMTAxMTEwMDExMDExMTAwMTExMDAxMDExMDAwMDEwMDExMDEwMTAxMTAwMDEwMDExMDAxMDAwMDExMTAwMDAxMTAwMDExMDExMDAxMDEwMDExMDAxMDAwMTExMDAxMDExMDAxMTAwMDExMDAxMDAwMTEwMTAwMDExMDAxMTAwMDExMDEwMTAwMTExMDAwMDAxMTAxMTAwMTEwMDEwMDAxMTAwMDExMDExMTExMDEwMDAwMTAxMDAwMDAxMDAxMDAwMDEwMDEg