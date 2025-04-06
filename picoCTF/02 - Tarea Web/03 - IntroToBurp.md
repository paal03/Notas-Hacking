## **Descripción**
Additional details will be available after launching your challenge instance.
## Hints
1. Try using burpsuite to intercept request to capture the flag.
2. Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer tenemos que hacer un tipo de formulario y iniciar sesión, después de esto nos lleva otra pagina donde tenemos que ingresar un tipo de contraseña para autenticarnos.
- Con la ayuda de burp suite vamos capturar esta solicitud, esta solicitud tiene el método **POST** y, en general, se espera el cuerpo en la solicitud POST, podemos intentar generar una respuesta eliminando **otp=0000** del cuerpo de la solicitud por completo.
- Si dejamos otp vacío y enviamos la solicitud vacía, esta nos devuelve la bandera.

```
picoCTF{#0TP_Bypvss_SuCc3$S_2e80f1fd}
```

## **Notas adicionales**

## **Referencias**