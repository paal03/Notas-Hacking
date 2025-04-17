## **Descripción**
Why search for the flag when I can make a bookmarklet to print it for me?
Additional details will be available after launching your challenge instance.
## Hints
1. A bookmarklet is a bookmark that runs JavaScript instead of loading a webpage.
2. What happens when you click a bookmarklet?
3. Web browsers have other ways to run JavaScript too.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- En este caso hay una caja de texto la cual contiene un código en javascript, al parecer tenemos que crear un boomarklet.
- Creamos un nuevo marklet y le agregamos el código que nos dan en el url que nos piden en la creación de la misma.
- Ahora solo basta con abrir este bookmarklet y nos dara la bandera.
- También podemos ir a la consola de las herramientas de desarrollador y colocar ahí el script y este nos dará la bandera.

```
picoCTF{p@g3_turn3r_0c0d211f}
```

## **Notas adicionales**
En esencia, un bookmarklet es un marcador que contiene un pequeño script de JavaScript que, al hacer clic en él, realiza una acción específica en la página web que estás visualizando. Por ejemplo, un bookmarklet podría resaltar texto, cambiar el diseño de la página, o incluso ejecutar una búsqueda en línea basándose en el texto seleccionado.
## **Referencias**
