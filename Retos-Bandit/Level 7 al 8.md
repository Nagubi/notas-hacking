# Bandit Level 7 → Level 8
## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de acceso al nivel
bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
## Solucion
```
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$
```
## Notas adicionales
| Comando | descripcion|
|---------------------|---------------------------|
|grep  | filtra la salida para mostrar solo las lineas que coinciden con un patron|
|wc | cuenta las lineas, palabras y caracteres de un archivo de texto|


## Referencias
