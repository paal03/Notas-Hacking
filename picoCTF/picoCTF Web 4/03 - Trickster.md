## **Descripción**
I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:55783/)!
## Hints

## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al parecer en la pagina podemos cargar algún tipo de archivo en este caso un PNG.
- Usamos robots.txt, y al parecer esta 2 rutas una la cual nos lleva a la ruta donde se guardan os archivos cargados y otra con las instrucciones la cual a ir ahi esta nos da el siguiente texto- %%Let's create a web app for PNG Images processing.
	It needs to:
	Allow users to upload PNG images
	look for ".png" extension in the submitted files
	make sure the magic bytes match (not sure what this is exactly but wikipedia says that the first few bytes contain 'PNG' in hexadecimal: "50 4E 47" )
	after validation, store the uploaded files so that the admin can retrieve them later and do the necessary processing. %%
- Al parecer la validación de que efectivamente sea un png no se realiza de manera correcta, por lo que cargaremos una webshell en php añadiendo la extensión png.
- Creamos el nuestro webshell y lo cargamos en la pagina, esta se sube de manera correcta.
- Luego fui a /uploads/webshell.png.php y obtuve una interfaz de línea de comandos para ejecutar comandos.
- Desde este punto, podemos buscar la bandera en el sistema como queramos.

![[Pasted image 20250405162931.png]] 
```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_3f706222}
```

## **Notas adicionales**
Un webshell es un script malicioso que permite a los atacantes comprometer servidores web y lanzar ataques adicionales. Se puede usar para: Exfiltrar y recopilar información y credenciales sensibles, Subir malware, Desfigurar sitios web.
## **Referencias**
https://gist.github.com/joswr1ght/22f40787de19d80d110b37fb79ac3985
