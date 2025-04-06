## **Descripción**
Can you login to this website?
Additional details will be available after launching your challenge instance.
## Hints
1. `admin` is the user you want to login as.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer este reto esta relacionado con una inyeccion sql.
- Al ingresar al sitio web, lo único que vemos es una página de inicio de sesión, donde tenemos que ingresar un usuario y contraseña.
- Si ingresamos un usuario y contraseña aleatorio este nos devuelve lo que parece ser la consulta SQL.
- Ahora si el sistema no valida adecuadamente las entradas del usuario, podríamos intentar inyectar código malicioso en el campo `username` o `password`. Por ejemplo, podría intentar algo como esto:
	- **Username**: `' OR 1=1 --`
	- **Password**: (cualquier valor)

- Esto generaría la consulta 
	- `SELECT * FROM users WHERE name='' OR 1=1 --' AND password='cualquier_valor`
	- - **name='' OR 1=1**: La parte OR 1=1 es siempre verdadera, lo que significa que la condición de la consulta será siempre válida, sin importar el valor del campo name.`
	- -- : Es un comentario en SQL, lo que hace que el resto de la consulta sea ignorado. Esto elimina la necesidad de verificar la contraseña.
Entonces si ingresamos esto nos direccionara en una pagina donde nos muestran la bandera.

![[08 - SQLiLite.png]]

```
picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}
```

## **Notas adicionales**

## **Referencias**