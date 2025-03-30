## **Descripción**
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` ([link](https://jupiter.challenges.picoctf.org/problem/17682/)) or http://jupiter.challenges.picoctf.org:17682
## Hints

## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista
- Al inspeccionar la pagina nos damos cuenta de que el error esta en que la contraseña la dejaron en el lado del cliente.
- Al inspeccionar el elemento o ver el código fuente de la página, podemos ver claramente que hay un script en el HTML del sitio que descompone la contraseña en subcadenas. 
- Al comparar las subcadenas con los índices proporcionados, obtenemos la contraseña, que es la bandera.

```
picoCTF{no_clients_plz_b706c5}
```

## **Notas adicionales**
Podemos hacer uso de un string en la terminal para extraer todas la cadenas, aqui se mostraran las que estan en base64 y los ordenamos conforme fueron llegando.

## **Referencias**
- https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers/User-Agent