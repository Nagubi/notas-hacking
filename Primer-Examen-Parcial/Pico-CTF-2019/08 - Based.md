# Based

## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

## Pistas
- It might help to have multiple windows open.
- I hear python can convert things.
## Solucion
Las conversiones fueron realizadas en cyberchef
```
nagubi-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
lizard
Please give the 01101100 01101001 01111010 01100001 01110010 01100100 as a word.
...
you have 45 seconds.....

Input:
lizard
Please give me the  164 141 142 154 145 as a word.
Input:
table
Please give me the 636f6e7461696e6572 as a word.
Input:
container
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
```

## Bandera

picoCTF{learning_about_converting_values_b375bb16}

## Notas adicionales

## Referencias
- [Cyberchef](https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')From_Base64('A-Za-z0-9%2B/%3D',true,false/disabled)From_Binary('None',8/disabled)From_Octal('Space'/disabled)&input=NjM2ZjZlNzQ2MTY5NmU2NTcy)

