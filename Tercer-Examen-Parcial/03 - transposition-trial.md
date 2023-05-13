# transposition-trial

## Descripcion
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).
## Pistas
- Split the message up into blocks of 3 and see how the first block is scrambled
## Solucion
```
Descargamos y abrimos el archivo txt dandonos cuenta que esta encripado con una traslacion de 3 por lo que buscamos una pagina la cual nos ayude a desencriptar la traslacion encontrando la bandera:
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}
```

## Bandera

picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

## Notas adicionales

## Referencias
- [Transposition Cipher Solver](https://tholman.com/other/transposition/)