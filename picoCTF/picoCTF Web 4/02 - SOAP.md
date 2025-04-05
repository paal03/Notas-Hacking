## **Descripción**
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

Additional details will be available after launching your challenge instance.
## Hints
1. XML external entity Injection
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- La pagina inicialmente no contiene nada especial esto tras inspeccionarla, lo unico que podemos saber es que hay 3 botones los cuales al presionar estos nos devuelven distintas etiquetas.
- Como la pista del reto nos hace mención de usar un ataque o inyección XML, entonces haremos uso de burpsuit.
- Al interceptar la solicitud al activar el botón, se reveló una etiqueta XML.
- Para manipular la entrada XML, envié la solicitud interceptada a la herramienta Repeater en Burp Suite.
- Después de enviarlo al repetidor, puedo ver una etiqueta de identificación que parece ser la identificación de lo que sea que haya en los datos.
- Ahora intentaremos agregar lo siguiente:
`<?xml version="1.0"?>`
`<!DOCTYPE data [`
`<!ELEMENT data (#ANY)>`
`<!ENTITY file SYSTEM "file:///etc/passwd">`
`]>`
`<data>&file;</data>`
- Al ejecutarse, la respuesta confirmó la explotación, mostrando la bandera buscada en la línea final.

![[Pasted image 20250402124439.png]]
- 
```
picoCTF{XML_3xtern@l_3nt1t1ty_4dbeb2ed}
```

## **Notas adicionales**
El ataque de entidad externa XML, o simplemente ataque XXE, es un tipo de ataque contra una aplicación que analiza la entrada XML. Este ataque se produce cuando un analizador XML débilmente configurado procesa la entrada XML que contiene una referencia a una entidad externa.

## **Referencias**
[PayloadsAllTheThings/XXE Injection/README.md at master · swisskyrepo/PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/XXE%20Injection/README.md)