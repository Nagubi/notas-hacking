#  GDB Test Drive
## Descripcion
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/86/gdbme).Here's the test drive instructions:

-   `$ chmod +x gdbme`
-   `$ gdb gdbme`
-   `(gdb) layout asm`
-   `(gdb) break *(main+99)`
-   `(gdb) run`
-   `(gdb) jump *(main+104)`

## Pistas


## Solucion
``
```
Seguimos las instrucciones que se nos dan y obtenemos la bandera:
picoCTF{d3bugg3r_dr1v3_72bd8355}

```


## Bandera
picoCTF{d3bugg3r_dr1v3_72bd8355}

## Notas adicionales

## Referencias
