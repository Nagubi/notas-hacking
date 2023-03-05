# Bandit Level 30 → Level 31
## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
bandit30
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
## Solucion
```shell
bandit30@bandit:~$ mkdir /tmp/nagubi30
bandit30@bandit:~$ cd /tmp/nagubi30
bandit30@bandit:/tmp/nagubi30$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
bandit30@bandit:/tmp/nagubi30$ cd repo/
bandit30@bandit:/tmp/nagubi30/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  5 22:32 .
drwxrwxr-x 3 bandit30 bandit30 4096 Mar  5 22:32 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Mar  5 22:32 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Mar  5 22:32 README.md
bandit30@bandit:/tmp/nagubi30/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/nagubi30/repo$ git tag
secret
bandit30@bandit:/tmp/nagubi30/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt

```
## Notas adicionales
_git clone_ es una utilidad de línea de comandos de Git que se utiliza para fijar como objetivo un repositorio y crear una copia de él.
## Referencias
- [mayadevbe](https://mayadevbe.me/posts/overthewire/bandit/level31/)