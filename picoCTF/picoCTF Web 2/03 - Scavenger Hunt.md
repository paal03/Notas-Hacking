## **Descripción**
There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?
## Hints
1. You should have enough hints to find the files, don't run a brute forcer.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- Inspeccione el elemento o abra el código fuente de la página y encontrará la primera parte de la bandera en el archivo html.
- Navega hasta `mycss.css`y encontrarás la segunda parte de la bandera.
- Luego, vaya al `myjs.js`archivo y encontrará una sugerencia que le pregunta cómo evitar que Google indexe el sitio.
- La respuesta es agregar un `robots.txt`archivo que especifica el [comportamiento de ciertos agentes de usuario](https://moz.com/learn/seo/robotstxt) .
- El `.htaccess`archivo administra la configuración del servidor Apache.
- En Mac, este `.DS_Store`archivo es un archivo oculto que almacena la configuración del escritorio (iconos, fondo, etc.).
- La bandera esta dividida en 5 partes si las unimos todas con la anterior.
- Obtenemos la siguiente bandera

```
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}

```

## **Notas adicionales**

## **Referencias**
https://httpd.apache.org/docs/2.4/es/howto/
https://en.wikipedia.org/wiki/.DS_Store
