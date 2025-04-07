## **Descripción**
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Hints
1. What is a hex editor?
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos dan con wget y lo guardamos en una carpeta.
- Lo primero es abrir la imagen en busca de algo, al parecer no hay nada a simple vista.
- Podemos usar un editor hexadecimal, para hacer un volcado de la imagen y ver el contenido, después podemos buscar la cadena pico, y así poder encontrar la bandera.
- También podemos usar el comando **'strings'**, para extraer las cadenas de texto de la imagen, y podemos filtrar la salida con **'grep pico'.**
- strings garden.jpg | grep pico

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Glory of the garden]
└─$ strings garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```

## **Notas adicionales**
El comando «strings» es una herramienta muy útil en Linux que _permite extraer cadenas de texto legibles de archivos binarios_.
El comando grep facilita _te permite buscar palabras o cadenas de texto en archivos_ o en la entrada estándar de la terminal.
## **Referencias**
1. https://infolinux.es/comando-strings-de-linux-obten-cadenas-de-texto-de-archivos-article-about-linux-command-strings-retrieve-text-strings-from-files/
2. https://www.hostinger.com/mx/tutoriales/comando-grep-linux