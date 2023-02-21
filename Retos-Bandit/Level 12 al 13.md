# Bandit Level 12 → Level 13
## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de acceso al nivel
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solucion
```shell
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt |zcat| file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat| file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat| file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat|tar xO| file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat|tar xO|tar xO| file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat|tar xO|tar xO|bzcat| file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat|tar xO|tar xO|bzcat|tar xO| file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Wed Jan 11 19:18:38 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt |zcat|bzcat|zcat|tar xO|tar xO|bzcat|tar xO|zcat| file -
/dev/stdin: ASCII text
> xxd -r data.txt |zcat|bzcat|zcat|tar xO|tar xO|bzcat|tar xO|zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales
| Comando | *descripcion*|
|---------------------|---------------------------|
|Hex dump  | este último es un enlace simbólico del primero, muestra los ficheros en formato ASCII, octal, decimal y hexadecimal|

| ext|comp| desc| *ver en consola*|
|-----|------|----------|---------------------------|
| .gz|gzip| gzip -d (gunzip)| zcat|
| .bz2|bzip2| bzip2 -d (bunzip2)| bzcat|
| .tar|tar| tar xf| tar XO|
## Referencias
[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)
