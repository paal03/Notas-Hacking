## **Descripción**
I made a cool website where you can announce whatever you want! Try it out!
Additional details will be available after launching your challenge instance.
## Hints
1. Server Side Template Injection
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer tendremos que hacer una inyección SSTI, esta consiste en Un ataque de inyección de plantilla del lado del servidor.
- Para saber de que tipo de plantilla utilizamos cierto criterio que es ingresar parámetros, para este caso utilizamos {{7*7}} en este caso esto funciona para plantillas twing en python.
- Una vez detectada la plantilla procedemos a buscar payloads que nos permitan vulnerar el sistema.
- Para este caso vamos a utilizar lo siguiente: 
	- {{ config.__class__.__init__.__globals__['os'].popen('COMANDOS QUE SE REQUIREN').read() }}
- Este código evalúa la expresión dentro de una plantilla, accede al objeto `config`, luego accede a la clase de `config`, y ejecuta un comando del sistema operativo. La salida de este comando se lee y se muestra en la plantilla.

 ```
# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_ae48ad61}
```

## **Notas adicionales**
La inyección de plantilla del lado del servidor es cuando un atacante puede usar la sintaxis de plantilla nativa para inyectar una carga maliciosa en una plantilla, que luego se ejecuta en el lado del servidor
## **Referencias**
1. https://portswigger.net/web-security/server-side-template-injection