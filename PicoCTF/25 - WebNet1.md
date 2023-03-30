# WebNet1

## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Pistas
- Try using a tool like Wireshark
- How can you decrypt the TLS stream?
## Solucion
```
Descargamos el archivo de la pagina capture.pcap la terminacion nos dice que es un archivo que se puede abrir en la herramienta de Wireshark ademas de una llave la cual usaremos agregandola en la ventana de preferencias en RSA keys de WireShark despues abrimos la capture.pcap y ahora con la llave tendriamos permiso para accesar observamos todo y vemos protocolos HTTP los revisamos e intentamos lo del ejercicio anterior dandonos  Pico-Flag: picoCTF{this.is.not.your.flag.anymore} por lo que tenemos que intentar algo distinto en este caso hacemos un follow TLS al GET despues de el HTTP bajamos hasta encontrar la bandera picoCTF{honey.roasted.peanuts}......
```

## Bandera

picoCTF{honey.roasted.peanuts}

## Notas adicionales

## Referencias