# where are the robots

## Descripcion
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/56830/` ([link](https://jupiter.challenges.picoctf.org/problem/56830/)) or http://jupiter.challenges.picoctf.org:56830
## Pistas
- What part of the website could tell you where the creator doesn't want you to look?
## Solucion
```
Para la solucion agregamos robots.txt al final del link quedandonos: https://jupiter.challenges.picoctf.org/problem/56830/robots.txt 
nos encontramos lo siguiente:
User-agent: *
Disallow: /1bb4c.html
reemplazamos robots.txt por /1bb4c.html quedando 
https://jupiter.challenges.picoctf.org/problem/56830/1bb4c.html y en esa liga obtenemos la bandera
Guess you found the robots  
picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}
```

## Bandera

picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}

## Notas adicionales

## Referencias
