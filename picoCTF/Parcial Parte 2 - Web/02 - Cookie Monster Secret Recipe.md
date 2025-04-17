## **Descripción**
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:57968/) and good luck
## Hints
1. Sometimes, the most important information is hidden in plain sight. Have you checked all parts of the webpage?
2. Cookies aren't just for eating - they're also used in web technologies!
3. Web browsers often have tools that can help you inspect various aspects of a webpage, including things you can't see directly.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer hay un ventana de inicio de sesión, donde se ingresa el usuario y contraseña, después de agregar datos aleatorios y tratar de ingresar esta nos manda a otra pagina donde nos dice que el login a sido denegado.
- Siguiendo las pistas que nos brindan, nos vamos a las herramientas de desarrollador al apartado de aplicaciones < storage < cookies.
- Estando las cookies nos damos cuenta de que hay una cookie llamada secret_recipe y value el cual contienen una cadena en hexadecimal.
- Solo queda extraer esa cadena y decodificarlo a texto, y con esto obtenemos la bandera.
![[02 - Cookie Monster Secret Recipe.png]]

```
cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzZFODFGQzFFfQ==
picoCTF{c00k1e_m0nster_l0ves_c00kies_6E81FC1E}
```

## **Notas adicionales**

## **Referencias**
1. https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnRqTURCck1XVmZiVEJ1YzNSbGNsOXNNSFpsYzE5ak1EQnJhV1Z6WHpaRk9ERkdRekZGZlE9PQ