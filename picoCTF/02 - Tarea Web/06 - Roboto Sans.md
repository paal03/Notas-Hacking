## **Descripción**
The flag is somewhere on this web application not necessarily on the website. Find it.
Additional details will be available after launching your challenge instance.
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Al observar el nombre del desafío, es posible que este tenga algo que ver con el archivo robots.txt.
- Empezamos yendo a robots.txt.
- Hay una cadena que está codificada en base64 y si la decodificamos en [base64decode](https://www.base64decode.org/) obtenemos una ruta que no debería estar en el archivo robots.txt: js/myfile.txt.
- Si dirigimos a esta ruta esta nos mostrara la bandera.

```
picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}
```

## **Notas adicionales**
Robots.txt es un archivo de texto creado para indicar a los robots web cómo rastrear las páginas de su sitio web. El archivo robots.txt puede indicar si ciertos agentes de usuario (software de rastreo web) pueden o no rastrear partes de un sitio web.
## **Referencias**
https://www.base64decode.org/
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YW5NdmJYbG1hV3hsTG5SNGRBPT0NCg&ieol=CRLF&oeol=CRLF
