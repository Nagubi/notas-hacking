# Bandit Level 32 → Level 33
## Objetivo
After all this `git` stuff its time for another escape. Good luck!

## Datos de acceso al nivel
bandit32
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y


## Solucion
```shell
>> ls
sh: 1: LS: not found
>> $0
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ whoami
bandit33
$ cat /etc/bandit\_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
        

```
Accedemos al bandit33 para verificar la contraseña
```bash
bandit33@bandit:~$ ls
README.txt
bandit33@bandit:~$ cat README.txt 
Congratulations on solving the last level of this game!

At this moment, there are no more levels to play in this game. However, we are constantly working
on new levels and will most likely expand this game with more levels soon.
Keep an eye out for an announcement on our usual communication channels!
In the meantime, you could play some of our other wargames.

If you have an idea for an awesome new level, please let us know!      

```
## Notas adicionales
Linux tiene variables llamadas variables locales (válidas en el shell actual), variables de shell (configuradas por shell) y variables de entorno (válidas en todo el sistema). Estas variables tienen sus nombres solo en mayúsculas. Se definen escribiendo VAR_NAME=var_value en la línea de comando. Para ver el contenido de una variable, puede escribir echo $VAR_NAME.
## Referencias
- [mayadev](https://mayadevbe.me/posts/overthewire/bandit/level33/)