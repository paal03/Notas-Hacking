## **Descripción**
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 7480`.
## **Solución** 
Para este reto haremos uso del comando nc(netcat).
- Nos conectaremos al puerto 7480 del servidor jupiter.challenges.picoctf.org
- Usamos el comando nc para conectarnos de manera remota de la siguiente manera: 
`nc [-options] hostname port[s] [ports]` |` nc jupiter.challenges.picoctf.org 7480 `
- Para este reto vaciamos el contenido que nos manda el puerto a un archivo llamado flag.txt
	 de la siguiente manera:

```
└─$ nc jupiter.challenges.picoctf.org 7480 > flag.txt
```

Después de ello solo hacemos uso de grep para filtrar la salida y obtener la bandera:

```
└─$ cat flag.txt | grep pico
picoCTF{digital_plumb3r_06e9d954}

```

## **Notas adicionales**
- Es comun el uso de pipe ' | ' ' para enviar la salida estandar a otro destino como un programa o archivo.
## **Referencias**
- https://www.linfo.org/pipes.html