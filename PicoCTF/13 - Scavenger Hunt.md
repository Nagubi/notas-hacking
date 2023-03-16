# Scavenger Hunt

## Descripcion
There is some interesting information hidden around this site [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/). Can you find it?
## Pistas
- You should have enough hints to find the files, don't run a brute forcer.
## Solucion
```
Abrimos el link http://mercury.picoctf.net:5080/ e ingresamos despues le damos click a analizar el codigo de la pagina obteniendo la primera parte de la bandera:
<!-- Here's the first part of the flag: picoCTF{t -->
despues dando click en el archivo mi css obtenemos la segunda parte:
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
agregamos al final de la pagina robots.txt obteniendo la tercera parte:
# Part 3: t_0f_pl4c
agregamos al final de la pagina .htaccess obteniendo la cuarte parte:
# Part 4: 3s_2_lO0k
por ultimo  al final de la pagina ponemos .DS_Store obteniendo la ultima parte:
Congrats! You completed the scavenger hunt. Part 5: _35844447}
unimos todo obteniendo la bandera: picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}
```

## Bandera

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}

## Notas adicionales

## Referencias
