#  Bandit Level 0 → Level 1 
## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel
bandit0
bandit0
## Solucion
```
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$
```
## Notas adicionales
ls, listar archivos
cat , emitir el contenido de un archivo en la línea de comandos
## Referencias


