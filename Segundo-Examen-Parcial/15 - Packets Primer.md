# Packets Primer
## Descripcion
Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/195/network-dump.flag.pcap)
## Pistas
- Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.
## Solucion
```
Abrimos el archivo con wireshark y vemos que un TCP contiene la bandera la copiamos en texto:
'Îs'¯9EpPÂ@@Ñ³

¾n#('ìÔ·½&¼öu
ÏéehðñÃp i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ b 9 d 5 3 7 6 5 }
la reordenamos y obtenemos la bandera:
picoCTF{p4ck37_5h4rk_b9d53765}
```

## Bandera

picoCTF{p4ck37_5h4rk_b9d53765}

## Notas adicionales

## Referencias
