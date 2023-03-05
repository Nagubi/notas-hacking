# fixme1.py
## Descripcion
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/37/fixme1.py)

## Pistas
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge
## Solucion
Este codigo lo analizamos en visual studio code y nos damos cuenta que se presenta
un error de identacion en la linea 20 del script en el printf de la bandera
```shell
C:\Users\Nagubi> & C:/Users/Nagubi/anaconda3/python.exe c:/Users/Nagubi/Downloads/fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

## Bandera

picoCTF{1nd3nt1ty_cr1515_6a476c8f}

## Notas adicionales

## Referencias 
