## **Descripción**

## Hints
1. Try using a tool like Wireshark
2. What are streams?
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos dan con wget y lo guardamos en una carpeta.
- Al parecer se trata de una captura de paquetes, lo podemos analizar usando wireshark.
- Podemos usar el filtro Follow UDP -> steam, para seguir el flujo de datos.
- Al hacer esto podemos encontrar la bandera en el steam 6.

```
picoCTF{StaT31355_636f6e6e}
```

## **Notas adicionales**
Steam se puede referir a la comunicación entre el cliente y los servidores de Steam a través de internet
## **Referencias**
