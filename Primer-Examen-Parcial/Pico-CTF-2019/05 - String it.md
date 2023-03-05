# Strings it
## Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

## Pistas
[strings](https://linux.die.net/man/1/strings)
## Solucion
```
┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
strings
                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ strings strings | grep picoCTF                  
picoCTF{5tRIng5_1T_7f766a23}

```

## Bandera

picoCTF{5tRIng5_1T_7f766a23}

## Notas adicionales

## Referencias
-   [strings](https://linux.die.net/man/1/strings)
