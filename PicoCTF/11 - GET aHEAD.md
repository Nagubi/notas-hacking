# GET aHEAD

## Descripcion
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Pistas
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses
## Solucion
```
Abrimos la herramienta de burpSuite pegando el siguiente link http://mercury.picoctf.net:45028/index.php? en la ventana de proxy en el boton open web browser y presionamos los botones de manera normal de la pagina de cambiar de color de rojo a azul despues de eso solo ocupamos irnos a HTTP history vemos un post le damos click y despues de seleccionarlo le damos click derecho y lo mandamos al repeater despues en el repeater le modificamos el texto de POST a HEAD y la respuesta es la bandera:
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8
```

## Bandera

picoCTF{r3j3ct_th3_du4l1ty_775f2530}

## Notas adicionales

## Referencias
[HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)