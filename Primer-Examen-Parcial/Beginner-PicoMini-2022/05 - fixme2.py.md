# fixme2.py
## Descripcion
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/66/fixme2.py)

## Pistas
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge
## Solucion
Este codigo lo analizamos en visual studio code y nos damos cuenta que se presenta
un error en la linea 22 del script usando "=" en vez de == .
```shell
C:\Users\Nagubi> & C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```

## Bandera

picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

## Notas adicionales

## Referencias 
