## **Descripción**
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/6353/` ([link](https://jupiter.challenges.picoctf.org/problem/6353/)) or http://jupiter.challenges.picoctf.org:6353
## Hints
1. What is obfuscation?
## **Solución** 
Para este reto haremos lo siguiente:
-  Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista
- Al inspeccionar la pagina nos damos cuenta de que el error esta en que la contraseña la dejaron en el lado del cliente pero en este caso, este en ofuscación de javascript.
- El propósito del código es verificar una contraseña ingresada por el usuario mediante una función llamada `verify()`. Si la contraseña es correcta, muestra una alerta con el mensaje `"Password Verified"`. Si es incorrecta, muestra una alerta con el mensaje `"Incorrect password"`
- Sin embargo, observamos que la matriz al principio contiene algunas cadenas, incluyendo algunas que podrían formar parte de la bandera, como `'picoCTF'`y `'not_this'`. Excluyendo las cadenas error.success/html, nos quedan `'picoCTF{'`, `'not_this'`, `'_again_3'`, y `'39d025}'`. Intentamos ensamblar estas piezas y obtenemos la bandera.

`picoCTF{not_this_again_39d025}`
- Con esto obtenemos la siguiente bandera
 ![[Pasted image 20250330134255.png]]
```
picoCTF{not_this_again_39d025}

```

## **Notas adicionales**
El código ofuscado ==es un código fuente que ha sido modificado para que sea más difícil de entender y manipular==. Esto se hace sin alterar la funcionalidad del programa.
## **Referencias**
https://beautifier.io/