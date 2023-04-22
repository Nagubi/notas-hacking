# Wireshark doo dooo do doo..
## Descripcion
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ae5b2bc07928fca272ff3900dc9a6cef/shark1.pcapng).
## Pistas

## Solucion
```
Vemos que la mayoria de los mensajes estan encriptados encontramos uno que no lo esta y le damos un follow como http stream quedandonos arriba en filtros: tcp.stream eq 5 le damos click a los archivos siguiendolos como http hasta que vemos  en uno cvpbPGS{c33xno00_1_f33_h_qrnqorrs} lo que posiblemente sea la bandera codificada la decodificamos con cyberchef con ret13 obteniendo la bandera picoCTF{p33kab00_1_s33_u_deadbeef}
```

## Bandera

picoCTF{p33kab00_1_s33_u_deadbeef}

## Notas adicionales

## Referencias
- [Cyberchef](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tjMzN4bm8wMF8xX2YzM19oX3FybnFvcnJzfQ0K)