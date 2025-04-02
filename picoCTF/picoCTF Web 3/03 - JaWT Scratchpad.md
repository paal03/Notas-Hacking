## **Descripción**
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090
## Hints
1. What is that cookie?.
2. Have you heard of JWT?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
-  La primera pista que se proporciona, es que hay una _'cookie'_ que tiene algo que ver con la solución a este desafío, por lo que **inspecciono las _'cookies'_**.
- Decodifico la _'cookie'_ indicada anteriormente (jwt) en una pagina web https://jwt.io/#debugger
- Se debe crackear la contraseña secreta para obtener una firma JWT válida.
- Usaremos  'John the Ripper' para esto.
- Parece ser que **la contraseña secreta para obtener una firma JWT válida** es "ilovepico".
- Por lo tanto, cambio el nombre de usuario de "john" a "admin", incluyo como contraseña secreta: ilovepico
- Ahora solo queda copiar JWT (JSON Web Token) así codificado, se pega en la _'cookie'_ indicada anteriormente la grabo y esta vez al volver a cargar la página puedo ver la flag
- 
```
picoCTF{jawt_was_just_what_you_thought_9ed4519dee8140de7a186a5df5a08d6e}.

```

## **Notas adicionales**

## **Referencias**
https://jwt.io/introduction/
https://jwt.io/#debugger
https://github.com/MarcoLugo/jwt2jtr
