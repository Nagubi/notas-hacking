# vault-door-4
## Descripcion
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/834acd392e0964a41f05790655a994b9/VaultDoor4.java)

## Pistas
- Use a search engine to find an "ASCII table".
- You will also need to know the difference between octal, decimal, and hexadecimal numbers.

## Solucion
``
```
 byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0146, 064 ,
            'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' ,
     


usamos varios convertidores el primero es de decimal a ascii el segundo es de hexadecimal a ascii el tercero es de octal a ascii y el ultimo ya se encuentra por lo que solo lo juntamos y obtenemos la bandera:
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}

```


## Bandera
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}

## Notas adicionales

## Referencias
- [hexa to ascii](https://www.branah.com/ascii-converter)
- [octal to ascii](https://www.browserling.com/tools/octal-to-text)