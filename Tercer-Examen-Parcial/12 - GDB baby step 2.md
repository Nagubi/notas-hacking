# GDB baby step 1

## Descripcion
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Debug [this](https://artifacts.picoctf.net/c/520/debugger0_b).
## Pistas
- You could calculate `eax` yourself, or you could set a breakpoint for after the calculcation and inspect `eax` to let the program do the heavy-lifting for you.
## Solucion
```
Descargamos el archivo y analizamos el codigo ensamblador con gdb:
(gdb) disassemble main
Dump of assembler code for function main:
  <+0>:     endbr64
  <+4>:     push   %rbp
  <+5>:     mov    %rsp,%rbp
  <+8>:     mov    %edi,-0x14(%rbp)
  <+11>:    mov    %rsi,-0x20(%rbp)
  <+15>:    movl   $0x1e0da,-0x4(%rbp) // [rbp-0x4]= 0x1e0da
  <+22>:    movl   $0x25f,-0xc(%rbp) // [rbp-0xc]= 0x25f
  <+29>:    movl   $0x0,-0x8(%rbp) // [rbp-0x8]= 0x0
  <+36>:    jmp    0x401136 <main+48> //salta a la linea 48
  <+38>:    mov    -0x8(%rbp),%eax //eax=[rbp-0x8]=0x0
  <+41>:    add    %eax,-0x4(%rbp) //[rbp-0x4]= 0x1e0da + eax
  <+44>:    addl   $0x1,-0x8(%rbp) //[rbp-0x8] se le suma 1=0x1
  <+48>:    mov    -0x8(%rbp),%eax // eax= [rbp-0x8]
  <+51>:    cmp    -0xc(%rbp),%eax //compara si eax es menor [rbp-0xc] esto debido a jl
  <+54>:    jl     0x40112c <main+38> //regresa a la linea 38
  <+56>:    mov    -0x4(%rbp),%eax
  <+59>:    pop    %rbp
  <+60>:    ret

End of assembler dump.

Analizando el codigo nos damos cuenta que para que se acabe el codigo deben pasar 607 veces pero no es tan facil como sumarlo a [rbp-0x4] ya que la primera vez suma 1 la segunda 2 y asi hasta 607 por lo que usamos la formula de gauss s=((1+606)/2)*606 dandonos 183921 le sumamos el valor de [rbp-0x4] en decimal que es 123098 obteniendo el numero de la bandera el cual es 307019
```

## Bandera

picoCTF{307019}

## Notas adicionales

## Referencias
- [HEXtoDEC](https://www.rapidtables.com/convert/number/hex-to-decimal.html)