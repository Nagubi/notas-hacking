# WebNet0

## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Pistas
- Try using a tool like Wireshark
- How can you decrypt the TLS stream?
## Solucion
```
Descargamos el archivo de la pagina capture.pcap la terminacion nos dice que es un archivo que se puede abrir en la herramienta de Wireshark ademas de una llave la cual usaremos agregandola en la ventana de preferencias en RSA keys de WireShark despues abrimos la capture.pcap y ahora con la llave tendriamos permiso para accesar observamos todo y vemos protocolos HTTP los revisamos y encontramos la bandera en uno de longitud 1299 pico-flag: picoCTF{nongshim.shrimp.crackers}\r\n
```

## Bandera

picoCTF{nongshim.shrimp.crackers}

## Notas adicionales

## Referencias
