## **Descripción**
Can you get the flag?Go to this [website](http://saturn.picoctf.net:61826/) and see what you can discover.
## Hints
1. Do you know how to modify cookies?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- El desafío nos da una página web que tiene un botón **Continuar como invitado.**
- Cuando hacemos clic en **Continuar como invitado** , nos aparecerá un mensaje de error que dice _"Lo sentimos, pero no tenemos servicios para invitados en este momento_
- Como lo sugiere el nombre del desafío, la solución probablemente implique cambiar el valor de una cookie.
- Tenemos una cookie llamada 'isAdmin' la cual tiene un valor 0, lo cual indica que somo invitados, si cambiamos este valor por 1, nos tratara como 'admin'.
- Hacemos este cambio y actualizamos la pagina, ahora nos mostrar la bandera.

![[Pasted image 20250405232205.png]]

```
picoCTF{gr4d3_A_c00k13_65fd1e1a}
```

## **Notas adicionales**
Para modificar una cookie se puede hacer desde las herramientas de inspeccionar, podemos instalar una extensión que nos ayude a realizar esta accion. 
También podemos usar una terminal y colocar lo siguiente.
```
curl -s http://saturn.picoctf.net:52021/check.php --cookie "isAdmin=1" | grep -oE "picoCTF{.*}"
```
## **Referencias**
https://www.elespanol.com/omicrono/software/20170511/editar-cookies-propio-navegador-web/215229260_0.html