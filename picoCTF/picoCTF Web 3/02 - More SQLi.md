## **Descripción**
There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?
## Hints
1. You should have enough hints to find the files, don't run a brute forcer.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer tenemos que iniciar sesion con un usuario y contraseña que claramente no conocemos.
- Así que tenemos que usar SQLI para omitir el inicio de sesión del usuario.
- Nombre de usuario: cualquier  
  Contraseña: ' o 1=1 --
- Después de iniciar sesión, aparece nuevamente una barra de búsqueda para buscar ciudades.
- Después de recibir la pista, podemos ver que la base de datos es 'SQLiLite': 'UNION SELECT nombre, sql, nulo de sqlite_master;--
- La carga útil para mirar el archivo de bandera es 'UNION SELECT bandera, nulo, nulo de more_table;--
- 

```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8b7cc2a}
```

## **Notas adicionales**

## **Referencias**
https://www.checkpoint.com/es/cyber-hub/cyber-security/what-is-cyber-attack/what-is-sql-injection-sqli/
https://www.prisma.io/dataguide/sqlite/basic-select
