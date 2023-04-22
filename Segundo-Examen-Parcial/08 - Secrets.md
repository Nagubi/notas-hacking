# Secrets
## Descripcion
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:65352/).
## Pistas
- folders folders folders
## Solucion
```
Ingresamos a la pagina web y le damos click derecho y le damos click en view page source luego ya viendo el codigo fuente vemos src="secret/assets/DX1KYM.jpg" le damos click y nos manda a la imagen recortamos hasta secret/ lo que nos manda a un gif de que estamos cerca abrimos el codigo fuente encontrando href=hidden/file.css lo abrimos y no nos lleva a nada por lo que quitamos file.css llevandonos a otra pagina volvemos a revisar el codigo fuente y vemos superhidden/xdfgwd.html por lo que lo agregamos y nos manda error por lo que quitamos dejando superhidden/ y la pagina indica que hemos encontrado la bandera pero no podemos verla le damos a analizar el codigo fuente y obtenemos la bandera: "flag">picoCTF{succ3ss_@h3n1c@10n_790d2615}</h3>

```

## Bandera

picoCTF{succ3ss_@h3n1c@10n_790d2615}

## Notas adicionales

## Referencias