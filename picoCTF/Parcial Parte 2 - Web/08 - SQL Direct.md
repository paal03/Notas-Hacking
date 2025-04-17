## **Descripción**
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Hints
1. What does a SQL database contain?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos conectaremos a la máquina virtual Kali Linux y ejecutaremos el comando
psql -h saturn.picoctf.net -p 61772 -U postgres pico
- Ejecutaremos el comando para obtener ayuda con los comandos psql.
- Ejecute el comando para ver 'lista de bases de datos'.
- Observamos que tenemos una tabla llamada "pico". Ejecutemos el comando "list tables".
- Hemos encontrado una columna llamada "flags". Accedamos a ella con el comando:
- Haciendo esto ultimo, llegamos a la bandera.

```
└─$ psql -h saturn.picoctf.net -p 55978 -U postgres pico

Password for user postgres: 
psql (17.4 (Debian 17.4-1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \?
pico=# \l
                                                    List of databases
   Name    |  Owner   | Encoding | Locale Provider |  Collate   |   Ctype    | Locale | ICU Rules |   Access privileges   
-----------+----------+----------+-----------------+------------+------------+--------+-----------+-----------------------
 pico      | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |        |           | 
 postgres  | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |        |           | 
 template0 | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |        |           | =c/postgres          +
           |          |          |                 |            |            |        |           | postgres=CTc/postgres
 template1 | postgres | UTF8     | libc            | en_US.utf8 | en_US.utf8 |        |           | =c/postgres          +
           |          |          |                 |            |            |        |           | postgres=CTc/postgres
(4 rows)

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)


picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
```

## **Notas adicionales**

## **Referencias**
1. 