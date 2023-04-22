# Forbidden Paths
## Descripcion
Can you get the flag?Here's the [website](http://saturn.picoctf.net:55287/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Pistas

## Solucion
```
Ingresamos a la pagina web y le damos click derecho y le damos click en view page source luego ya viendo el codigo fuente no observamos nada intentamos ingresar de distintas maneras sin exito hasta que colocamos ../../../../flag.txt para subir de directorio obteniendo la bandera:
picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}

```

## Bandera

picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}

## Notas adicionales

## Referencias