# Safe Opener 2
## Descripcion
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

## Pistas
- Download and try to decompile the file.
## Solucion
``
```
Descargamos el archivo y vemos la extension .class lo que nos indica que se refiere a java buscamos un deocmpilador de java ingresamos el archivo y encontramos la bandera:
 final String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}";

```


## Bandera
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}

## Notas adicionales

## Referencias
- [decompiler java](http://www.javadecompilers.com/result)