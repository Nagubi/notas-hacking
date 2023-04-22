# Easy1

## Descripcion
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.
## Pistas
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
- Please use all caps for the message.
## Solucion
```
Abrimos el archivo viendo una matriz de letras ahora para solucionarlo usaremos la descripcion que nos dice la llave para este tipo de encriptacion conocido como Vigenere en este caso usaremos la herramienta usando cyberchef la llave sera SOLVECRYTPTO y UFJKXQZQUNB sera la entrada y asi obtenemos la bandera: CRYPTOISFUN
```

## Bandera

picoCTF{CRYPTOISFUN}

## Notas adicionales

## Referencias
- [Cyberchef](https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkI)