# Roboto Sans
## Descripcion
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:61304/) out.
## Pistas

## Solucion
```
Ingresamos a la pagina web y viendo la pista de roboto me supongo se refiere a robots.txt un archivo que contienen muchas paginas web por lo que lo agregamos al final del enlace obteniendo lo siguiente:
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
vemos que esta en base 64 por lo que en cyberchef lo desiframos dandonos : js/myfile.txt agregamos esa extension al link original obteniendo la bandera:
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}

```

## Bandera

picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}

## Notas adicionales

## Referencias
- [Cyberchef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=CmFuTXZiWGxtYVd4bExuUjRkQT09Cgo)