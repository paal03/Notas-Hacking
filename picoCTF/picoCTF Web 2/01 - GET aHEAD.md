## **Descripción**
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:53554/](http://mercury.picoctf.net:53554/)
## Hints
1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Este sitio web tiene 2 botónes que puedes presionar para cambiar el color del fondo.
- Hacemos clic en ambos botones y analizamos todo el tráfico capturado hasta el momento en la herramienta burpsuite.
- El nombre del desafío, " **Get aHEAD** ", parece ser una pista, ya que **HEAD** es uno de los métodos HTTP conocidos que podemos probar en cualquier solicitud capturada. Cambiamos el método de GET a HEAD .
- Con esto obtenemos la siguiente bandera
 
```
picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
```

## **Notas adicionales**
HTTP define un conjunto de **métodos de petición** para indicar la acción que se desea realizar para un recurso determinado. Aunque estos también pueden ser sustantivos, estos métodos de solicitud a veces son llamados _HTTP verbs_.
## **Referencias**
https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods