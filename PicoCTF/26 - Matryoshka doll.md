# Matryoshka doll

## Descripcion
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Pistas
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}
## Solucion
```
Descargamos el archivo de la pagina en kali despues usamos el comando binwalk -e dolls.jpg nos movemos a la carpeta que nos da y asi hasta llegar a flag.txt reemplazamos los caracteres que dividen para obtener la bandera picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}
```

## Bandera

picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}

## Notas adicionales

## Referencias