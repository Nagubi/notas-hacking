# shark on wire 2

## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Pistas
- Try using a tool like Wireshark
- What are streams?
## Solucion
```
Descargamos el archivo de la pagina capture.pcap la terminacion nos dice que es un archivo que se puede abrir en la herramienta de Wireshark buscamos entre los UDP sin exito hasta que encontramos uno que dice star copiamos esa ip en el filtro ip.addr == 10.0.0.66 vemos que el primer numero del puerto no cambia pero los demas si cambiamos a un convertidor de codigos ASCII a caracteres usando los numeros que cambian obtemos la bandera picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

## Bandera

picoCTF{p1LLf3r3d_data_v1a_st3g0}

## Notas adicionales

## Referencias
