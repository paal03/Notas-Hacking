## **Descripción**
Help us test the form by submiting the username as `test` and password as `test!`
Additional details will be available after launching your challenge instance.
## Hints
1. any redirections?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- La pagina nos muestra una ventana de login, donde se pide un usuario y contraseña, la cual el reto no brinda.
- Cuando hacemos login nos redirecciona a otra pagina, después de inspeccionar la pagina, no encontramos nada interesante.
- Siguiendo la pista parece que en algún punto hay alguna redirección.
- Haremos uso de un proxy y de burp suite para ver el flujo de las solicitudes.
- Ahora volvemos hacer el mismo paso de login.
- Nos damos cuenta de que se redirecciona 2 veces a destinos distintos, esto antes de llegar realmente a la pagina de /home.
- En estas rutas parece ver cadenas en hexadecimal, las capturamos y las decodificamos a texto.
- Con esto podemos obtener la bandera, la cual esta dividida en 2 partes.

![[06 - findme.png]]

```
picoCTF{proxies_all_the_way_25bbae9a}
```

## **Notas adicionales**
Un **proxy** es básicamente un **intermediario** entre dos partes que quieren comunicarse, generalmente entre tu dispositivo (como tu computadora o teléfono) y los servidores de internet. Es como un "puente" que se encuentra entre tú y la web, y todo el tráfico de datos pasa por él.
## **Referencias**
1. 