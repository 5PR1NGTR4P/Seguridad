## Objetivo
We found this [file](https://mercury.picoctf.net/static/d0129ad98ba9258ab59e7700a1b18c14/tunn3l_v1s10n). Recover the flag.
## Solución
```
                                                                             
┌──(kali㉿kali)-[~/forensic3/tunel]
└─$ hexeditor tunn3l_v1s10n 
                                                                             
┌──(kali㉿kali)-[~/forensic3/tunel]
└─$ open tunn3l_v1s10n 
                                                                             
┌──(kali㉿kali)-[~/forensic3/tunel]
└─$ exiftool tunn3l_v1s10n 
ExifTool Version Number         : 12.67
File Name                       : tunn3l_v1s10n
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2024:03:21 14:43:42-04:00
File Access Date/Time           : 2024:03:21 14:43:58-04:00
File Inode Change Date/Time     : 2024:03:21 14:43:42-04:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                             
┌──(kali㉿kali)-[~/forensic3/tunel]
└─$ hexeditor tunn3l_v1s10n 
                                                                             
┌──(kali㉿kali)-[~/forensic3/tunel]
└─$ open tunn3l_v1s10n 

picoCTF{qu1t3_a_v13w_2020}
```
## Notas adicionales
## Referencias
- https://en.wikipedia.org/wiki/BMP_file_format