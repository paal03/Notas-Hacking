## **Descripción**
Do you know how to use the web inspector?
Additional details will be available after launching your challenge instance.
## Hints
1. Use the web inspector on other files included by the web page.
2. The flag may or may not be encoded
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
-  Al ingresar al sitio web, lo único que vemos es una página con algo de texto .
- Solo basta con navegar un poco en la pagina y ir inspeccionando cada lugar al cual accedemos.
- Cuando ingresamos a la "seccion about me" de la pagina, esta contiene algo interesante, al parecer hay una cadena la cual podría ser la bandera.
- Usamos un decodificador de base 64 y esta nos devolverá la bandera.
![[10 - WebDecode.png]]

```
cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMTBmOTM3NmZ9
picoCTF{web_succ3ssfully_d3c0ded_10f9376f}
```

## **Notas adicionales**

## **Referencias**