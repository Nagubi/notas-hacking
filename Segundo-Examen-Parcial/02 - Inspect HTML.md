# Inspect HTML
## Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:55825/) and see what you can discover.

## Pistas
- What is the web inspector in web browsers?
## Solucion
```
Ingresamos a la pagina web y le damos click derecho y le damos click en view page source luego ya viendo el codigo fuente observando hasta abajo vemos un comentario el cual es la bandera:
<p> Source: Wikipedia on Histiaeus </p>

<!--picoCTF{1n5p3t0r_0f_h7ml_8113f7e2}-->

</body>

```

## Bandera

picoCTF{1n5p3t0r_0f_h7ml_8113f7e2}

## Notas adicionales

## Referencias