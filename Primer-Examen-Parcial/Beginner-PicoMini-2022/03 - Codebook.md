# Codebook
## Descripcion
Run the Python script `code.py` in the same directory as `codebook.txt`.
-   [Download code.py](https://artifacts.picoctf.net/c/100/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/100/codebook.txt)

## Pistas
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion
Este codigo lo analizamos en visual studio code y nos damos cuenta que la bandera la obtiene
con el archivo de texto ejecutamos el script junto el archivo de texto en el mismo directorio
y obtenemos la bandera
```shell
C:\Users\Nagubi\Downloads> & C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
```

## Bandera

picoCTF{c0d3b00k_455157_d9aa2df2}

## Notas adicionales

## Referencias 