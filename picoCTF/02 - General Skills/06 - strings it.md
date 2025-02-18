## **Descripción**
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el file que nos dan con wget.
- Hacemos uso del comando strings para filtrar solo las cadenas legibles y además le pasamos un grep para filtrar la salida y obtener la bandera.

```
┌──(kali㉿kali)-[~/Documents/General Skills/Strings it ]
└─$ strings strings | grep pico              
picoCTF{5tRIng5_1T_d66c7bb7}


```

## **Notas adicionales**
El comando «strings» es una herramienta muy útil en Linux que permite extraer cadenas de texto legibles de archivos binarios. Esto resulta especialmente útil para analizar archivos ejecutables, bibliotecas compartidas o cualquier otro archivo que contenga texto legible incrustado. El comando «strings» forma parte de la mayoría de las distribuciones de Linux y se puede utilizar de manera rápida y sencilla desde la línea de comandos.
## **Referencias**
https://infolinux.es/comando-strings-de-linux-obten-cadenas-de-texto-de-archivos-article-about-linux-command-strings-retrieve-text-strings-from-files/