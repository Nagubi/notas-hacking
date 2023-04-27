# Pixelated

## Descripcion
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)
## Pistas
- [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
- Think of different ways you can "stack" images
## Solucion
```
Descargamos las imagenes y ejecutamos el codigo siguiente de python:
from PIL import Image # pip install Pillow img1 = Image.open("scrambled1.png") pixels1 = img1.load() img2 = Image.open("scrambled2.png") pixels2 = img2.load() flag = Image.new("RGB" ,img1.size) flagpix = flag.load() for row in range(img1.size[1]): for col in range(img1.size[0]): flagpix[col,row]=( (pixels1[col,row][0]+pixels2[col,row][0])%256, (pixels1[col,row][1]+pixels2[col,row][1])%256, (pixels1[col,row][2]+pixels2[col,row][2])%256) flag.save("flag.png")
la bandera esta dentro de una imagen y la bandera es:
picoCTF{2a4d45c7}

```

## Bandera

picoCTF{sma11_N_n0_g0od_73918962}

## Notas adicionales

## Referencias
