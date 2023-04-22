# Local Authority
## Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:51108/) and see what you can discover.

## Pistas
- How is the password checked on this website?
## Solucion
```
Ingresamos a la pagina web y le damos click derecho y le damos click en view page source luego ya viendo el codigo fuente lo unico destacable es login.php, intentamos acceder con cualquier usuario y contraseña y usuario y nos mandara a una pantalla de que es incorrecta por lo que repetimos el paso de ver el codigo fuente de la pagina ahora con el error viendo que a cambiado el codigo fuente vemos el archivo secure.js donde se encuentra la contraseña y el usuario para ingresar:
if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
usamos ese usuario y contraseña e ingresamos obteniendo la bandera:
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}

```

## Bandera

picoCTF{j5_15_7r4n5p4r3n7_05df90c8}

## Notas adicionales

## Referencias