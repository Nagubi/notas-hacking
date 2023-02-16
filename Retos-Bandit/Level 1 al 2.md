# Bandit Level 1 → Level 2
## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
## Solucion
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ 

```
## Notas adicionales
para buscar un archivo con '-' debe usarse primero un "./"
## Referencias
-   [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
-   [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](https://tldp.org/LDP/abs/html/special-chars.html)
