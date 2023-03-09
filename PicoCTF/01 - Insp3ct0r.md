# Insp3ct0r

## Descripcion
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670

## Pistas
- How do you inspect web code on a browser?
- There's 3 parts
## Solucion
```
Damos boton derecho en el link de la pagina en la seccion "How" le damos en inspeccionar  el codigo fuente y obtenemos la primera parte picoCTF{tru3_d3.
<link rel="stylesheet" type="text/css" href="[mycss.css](https://jupiter.challenges.picoctf.org/problem/9670/mycss.css)"> vamos a ese link mostrado en el html y obtenemos al segunda aprte de la bandera
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
por ultimo clickeamos <script type="application/javascript" src="[myjs.js](https://jupiter.challenges.picoctf.org/problem/9670/myjs.js)"></script>
y obtenemos la tercera parte de la bandera
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */
```

## Bandera

picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}

## Notas adicionales

## Referencias
