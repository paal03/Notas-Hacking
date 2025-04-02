## **Descripción**
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Hints
1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Lo único interesante que encontramos es lo siguiente:`Hi. I tried adding my favorite Irish person, Conan O'Brien. But I keep getting something called a SQL Error`que el sitio utiliza una base de datos SQL.
- Entonces utilizaremos una inyección SQL, haremos lo siguiente en cierto punto de la pagina hay un recuadro de input pero esta oculto, podemos empezar por habilitar este y que sea visible
- Ahora en el usuario ingresaremos lo siguiente admin'- y en la contraseña no importa lo que coloquemos .
- Al hacer esto nos deja entrar al sitio y nos muestra la bandera.
- Al parecer en la pagina no se esta validando correctamente la contraseña.

```
picoCTF{s0m3_SQL_fb3fe2ad}
```

## **Notas adicionales**

## **Referencias**
