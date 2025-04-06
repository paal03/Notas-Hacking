## **Descripción**
We have several pages hidden. Can you find the one with the flag?
Additional details will be available after launching your challenge instance.
## Hints
1. folders folders folders
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Se supone que para este reto vamos a navegar entra varias carpetas para encontrar la bandera.
- Si inspeccionamos la pagina, y analisamos un poco no damos cuenta de que hay una carpeta llamada secrets/, donde se alamcena el directorio donde estamos inicialmente.
- Si colocamos este directorio en la url <http://saturn.picoctf.net:54447/secret/>.
- Luego volvemos hacer lo mismo aqui y nos encontramos de que hay otra carpeta llamada hidden/, tambien colocamos este directorio <http://saturn.picoctf.net:54447/secret/hidden/>.
- Repetimos el mismo paso, y encontramos otro directorio llamado superhiden/, tambien lo colacamos en el url quedando de esta manera <http://saturn.picoctf.net:54447/secret/hidden/superhidden/>
- Al paracer este ultimo nos lleva a la bandera, si inspeccionamos la pagina nos daremos cuenta de que la bandera esta ahí.
![[Pasted image 20250406110049.png]]

```
picoCTF{succ3ss_@h3n1c@10n_51b260fe}
```

## **Notas adicionales**

## **Referencias**