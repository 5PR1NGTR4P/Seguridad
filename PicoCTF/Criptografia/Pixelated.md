## Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/6e4afb967ef8c865f79f3a8cd7767cca/scrambled2.png)
## Solución
```
imagenes.py:
import numpy as np
from PIL import Image

# Open images
im1 = Image.open("scrambled1.png")
im2 = Image.open("scrambled2.png")

# Make into Numpy arrays
im1np = np.array(im1)
im2np = np.array(im2)

# Add images
result = im2np + im1np
# Convert back to PIL image and save
Image.fromarray(result).save('result.png')

──(kali㉿kali)-[~/cososososo]
└─$ open result.png

picoCTF{0542dc1d}
```
## Notas adicionales
## Referencias