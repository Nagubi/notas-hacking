# SQLLite // pendiente por mantenimiento
## Descripcion
Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 49583 -U postgres pico`Password is `postgres`
## Pistas
- What does a SQL database contain?
## Solucion
```
nagubi-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 49583 -U postgres picoPassword for user postgres: 
psql (14.5 (Ubuntu 14.5-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 

```

## Bandera

picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}

## Notas adicionales

## Referencias
- [Postgres tutorial](https://www.postgresqltutorial.com/postgresql-administration/postgresql-show-tables/#:~:text=Use%20the%20%5Cdt%20or%20%5Cdt%2B,from%20the%20pg_catalog.pg_tables%20catalog.)