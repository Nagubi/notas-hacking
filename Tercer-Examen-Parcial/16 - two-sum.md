#  two-sum

## Descripcion
Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 51261`. [Source](https://artifacts.picoctf.net/c/456/flag.c
## Pistas
- Integer overflow
- Not necessarily a math problem
## Solucion
```
viendo el codigo vemos que es un numero positivo y entero por lo que agregamos el entero mas grande posible y el menor numero positivo sin contar al 0 obteniendo la bandera:
echo -e "2147483647\n1" | nc saturn.picoctf.net 51261
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}


```

## Bandera

picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}

## Notas adicionales

## Referencias
- [WriteUp](https://github.com/snwau/picoCTF-2023-Writeup/blob/main/Binary%20Exploitation/two-sum/two-sum.md)