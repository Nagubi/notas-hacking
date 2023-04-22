# Lookey here
## Descripcion
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/125/anthem.flag.txt).
## Pistas
- Download the file and search for the flag based on the known prefix.
## Solucion
```
nagubi-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/125/anthem.flag.txt
--2023-04-20 15:04:44--  https://artifacts.picoctf.net/c/125/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.6, 108.156.172.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: 'anthem.flag.txt'

anthem.flag.txt     100%[==================>] 106.12K  --.-KB/s    in 0.05s   

2023-04-20 15:04:44 (1.90 MB/s) - 'anthem.flag.txt' saved [108668/108668]

nagubi-picoctf@webshell:~$ grep pico anthem.flag.txt 
      we think that the men of picoCTF{gr3p_15_@w3s0m3_58f5c024}
nagubi-picoctf@webshell:~$ 
```

## Bandera

picoCTF{gr3p_15_@w3s0m3_58f5c024}

## Notas adicionales

## Referencias
