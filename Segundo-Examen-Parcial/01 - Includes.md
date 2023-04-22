# Includes
## Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:56469/) and see what you can discover.

## Pistas
- Is there more code than what the inspector initially shows?
## Solucion
```
Ingresamos a la pagina web y le damos click derecho y le damos click en view page source luego ya viendo el codigo fuente de la pagina abrimos el archivo style.css obteniendo la primera parte de la bandera:
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */
despues vemos el archivo script.js obteniendo la segunda parte de la bandera:
function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_b8f4b022}
lo juntamos y tenemos la bandera:
picoCTF{1nclu51v17y_1of2_f7w_2of2_b8f4b022}

```

## Bandera

picoCTF{1nclu51v17y_1of2_f7w_2of2_b8f4b022}

## Notas adicionales

## Referencias