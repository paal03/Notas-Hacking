## **Descripción**
Can you get the flag?
Additional details will be available after launching your challenge instance.
Try [here](http://titan.picoctf.net:62577/) to find the flag
## Hints
1.  Try using burpsuite to intercept request to capture the flag.
2. Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Este reto es muy sencillo de resolver solo basta con ver el código fuente de la pagina y encontramos la bandera.

```
picoCTF{1n5p3t0r_0f_h7ml_1fd8425b}
```

## **Notas adicionales**

## **Referencias**