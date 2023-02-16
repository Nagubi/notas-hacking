# Bandit Level 8 → Level 9
## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso al nivel
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solucion
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wx data.txt
wx: command not found
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$ 
```
## Notas adicionales
| Comando | descripcion|
|---------------------|---------------------------|
|sort  | ordena las lineas de texto|
|-uniq -u | Muestra los unicos|
|-uniq -c | Cuenta repetidos|
|-uniq -d | Muestra los repetidos|

## Referencias
- [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)
