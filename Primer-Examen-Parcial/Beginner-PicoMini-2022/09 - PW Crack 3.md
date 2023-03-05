# PW Crack 3
## Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/25/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/25/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/25/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Pistas
- To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
- To exit `bvi` type `:q` and press enter.
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
Analizamos el Script en visual studio Code notando que se encuentran 7 claves en la linea 44
intentamos todas para ver cual es la correcta y obtener la bandera
```shell
C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/level3.py
Please enter correct password for flag: 8799
That password is incorrect
PS C:\Users\Nagubi\Downloads> & C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/level3.py
Please enter correct password for flag: d3ab& C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/level3.py
That password is incorrect
PS C:\Users\Nagubi\Downloads> & C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/level3.py
Please enter correct password for flag: 1ea2    
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```

## Bandera

picoCTF{m45h_fl1ng1ng_6f98a49f}

## Notas adicionales
No hay necesidad de usar el hash.bin ya que realmente son muy pocas contraseñas.
## Referencias 