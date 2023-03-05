# PW Crack 2
## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level2.flag.txt.enc) in the same directory too.

## Pistas
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
Analizamos el Script en visual studio Code notando que la clave se encuentra encriptada en hexadecimal por lo que creamos un programa que imprima esto en ASCII y asi obtener la bandera
```shell
C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```

## Bandera

picoCTF{tr45h_51ng1ng_489dea9a}

## Notas adicionales
La clave tambien se puede obtener con CyberChef pero es un proceso mas lento.
## Referencias 