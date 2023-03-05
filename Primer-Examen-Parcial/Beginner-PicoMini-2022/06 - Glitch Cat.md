# Glitch Cat
## Descripcion
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 65353`

## Pistas
- ASCII is one of the most common encodings used in programming
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.
## Solucion
Creamos un script en phyton que nos permita imprimir el resultado del netcat lo que nos da la bandera
```shell
nagubi-picoctf@webshell:~$ nc saturn.picoctf.net 65353
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
```

## Bandera

picoCTF{gl17ch_m3_n07_9c42a45d}

## Notas adicionales

## Referencias 