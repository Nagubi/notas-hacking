# Magikarp Ground Mission
## Descripcion
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `ee388b88`

Additional details will be available after launching your challenge instance.
## Pistas
- Finding a cheatsheet for bash would be really helpful!
## Solucion
```bash
nagubi-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 49393
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  dev   instructions-to-3of3.txt  media  proc  sbin  tmp
bin            etc   lib                       mnt    root  srv   usr
boot           home  lib64                     opt    run   sys   var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
3ca613a1}
```
Unimos los resultados de leer los archivos de texto y obtenemos la siguiente bandera:
picoCTF{xxsh_0ut_0f_\/\/4t3r_3ca613a1}.

## Bandera

picoCTF{xxsh_0ut_0f_\/\/4t3r_3ca613a1}

## Notas adicionales

## Referencias

