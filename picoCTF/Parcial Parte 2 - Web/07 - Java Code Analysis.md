## **Descripción**
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!
Additional details will be available after launching your challenge instance.
## Hints
1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4. Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- La pagina es una biblioteca digital, nos muestra una ventana de login, donde se pide un usuario y contraseña, la cual el reto no brinda.
- Al parecer al hacer login, solo podemos acceder a ciertos libros(los gratuitos.)
- Para este reto nuestro objetivo es pasar de un usuario común al administrador para poder ver el libro que contiene la bandera.
- Tambien nos brindan el codigo fuente de toda la pagina.
- Entonces comenzamos analizando el código siguiendo las sugerencias.
- La sugerencia dice analizar la “clave secreta” JWT codificada en algún lugar de la parte de contenedor, seguridad o servicios en el código fuente.
- Depues de analizar un poco nos encontramos con la firma que es '1234'.
- Podemos utilizar el sitio web [**jwt.io**](https://jwt.io/) para decodificar y codificar tokens JWT.
- Capturamos los tokens con las herramientas de desarrollador: Aplication < storage < local storage.
- Los llevamos a https://jwt.io/ y cambiamos los campos de ID de usuario y correo electrónico, id de usuario: Admin, email: admin, userID: 2 y la firma: 1234.
- Modificando estos valores tendremos listo nuestro nuevo token.
- Con nuestro nuevo token JWT, deberíamos poder reemplazar esto fácilmente inspeccionando la página: Aplication < storage < local storage
- Una vez hecho esto solo queda refrescar nuevamente la pagina.

![[07 - Java Code Analysis.png]]

```
picoCTF{w34k_jwt_n0t_g00d_d7c2e335}
```

## **Notas adicionales**
JSON Web Token (JWT) es un estándar abierto que permite compartir información de forma segura entre dos partes. Se basa en objetos JSON y se utiliza para autenticar usuarios y autorizar el acceso a aplicaciones
## **Referencias**
1. https://jwt.io/