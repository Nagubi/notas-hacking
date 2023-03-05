# First Grep

## Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Pistas
- grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)
## Solucion
Se uso el equivalente a grep en c
```
C:\Users\Nagubi>cd Downloads

C:\Users\Nagubi\Downloads>findstr /i /r /c:"^picoCTF" file
picoCTF{grep_is_good_to_find_things_5af9d829}

C:\Users\Nagubi\Downloads>

```

## Bandera

picoCTF{grep_is_good_to_find_things_5af9d829}

## Notas adicionales

## Referencias
-  [Grep tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)
- [Equivalente Grep](https://www.shellhacks.com/windows-grep-equivalent-cmd-powershell/)
