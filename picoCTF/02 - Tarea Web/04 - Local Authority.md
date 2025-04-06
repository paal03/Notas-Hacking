## **Descripción**
Can you get the flag?
Additional details will be available after launching your challenge instance.
## Hints
1. How is the password checked on this website?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al ingresar al sitio web, lo único que vemos es una página de inicio de sesión, donde tenemos que ingresar un usuario y contraseña.
- Al inspeccionar la pagina no se muestra nada, sin embargo si tratamos de iniciar sesión, aunque no tengamos idea la contraseña, esta nos llevara a otra pagina donde nos mostrara que las credenciales son incorrectas y que no pudimos iniciar sesión
- Pero si inspeccionamos esas misma pagina nos daremos cuenta que se encuentra un archivo llamado secure.js, al ver este nos damos cuenta de que ahí esta las credenciales que necesitamos para iniciar sesión de manera correcta.
- Al volver iniciar sesión con las credenciales que obtuvimos, nos podemos logear y nos mustran la bandera.

![[Pasted image 20250405231336.png]]
```
picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
```

## **Notas adicionales**

## **Referencias**