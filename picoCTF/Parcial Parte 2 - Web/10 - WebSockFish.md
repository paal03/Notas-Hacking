## **Descripción**

## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- La pagina parece mostrar un tablero de ajedrez en el cual podemos jugar.
- Para resolver este reto tendremos que analizar el código fuente de la pagina.
- En algún punto nos damos cuenta de que del siguiente fragmento sendMessage(message);
- Este nos envía un mensaje en pantalla con los números de movimientos que hacemos .
- Vamos a usar la consola de la herramienta de desarrolladores para resolver el reto.
- Lo que haremos será modificar el valor que se envía a través de esta función sendMessage(message);
- Cuando se envia el mensaje tenemos 2 variables eval(cliente) y  mate(servidor).
- La estructura del mensaje que se envia es el siguiente message = "mate o (eval) " + parseInt(splitString[9]);
- Trataremos de modificar este mensaje.
- Después de realizar pruebas nos damos cuenta de que podemos hacer  sendMessage(eval -100); y con esto podremos obtener la bandera.

```
	picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_a2a9bbe9}
```

## **Notas adicionales**
WebSocket es un protocolo de red que permite la comunicación en tiempo real entre un navegador y un servidor web. Es una tecnología que permite enviar mensajes y recibir respuestas sin tener que consultar al servidor para cada respuesta. 

## **Referencias**
