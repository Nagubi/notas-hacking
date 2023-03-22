# shark on wire 1

## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Pistas
- Try using a tool like Wireshark
- What are streams?
## Solucion
```
Descargamos el archivo de la pagina capture.pcap la terminacion nos dice que es un archivo que se puede abrir en la herramienta de Wireshark agregamos en display filter udp.stream eq 6 vemos que son UDP de longitud 1 le damos un follow udp y obtenemos la bandera picoCTF{StaT31355_636f6e6e}
```

## Bandera

picoCTF{StaT31355_636f6e6e}

## Notas adicionales

## Referencias
