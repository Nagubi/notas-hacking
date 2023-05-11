# reverse_cipher
## Descripcion
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.

## Pistas
- objdump and Gihdra are some tools that could assist with this
## Solucion
``
```
Usamos el codigo del video el cual es:
cifrado = open('rev_this','r').read()

print (cifrado)

flag = ''

for i in range (8, len(cifrado)-1):
        if i &  1 == 0:
                flag += chr( ord(cifrado[i]) - 5 )
        else:
                flag += chr( ord(cifrado[i]) +2 )

print (flag)

obteniendo la bandera:
r3v3rs312528e05

```


## Bandera
picoCTF{r3v3rs312528e05}

## Notas adicionales

## Referencias
