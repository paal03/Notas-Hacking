## **Descripción**
RED, RED, RED, RED. Download the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
## Hints
1. Red?Ged?Bed?Aed?
2. The picture seems pure, but is it though?
3. Check whatever Facebook is called now.
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de una imagen, al abrirla solo muestra una simple imagen pero nada interesante.
- Ahora nos guiamos un poco con las pistas.
- Al parecer tiene que ver con la esteganografía.
- Para realizar una inspección a png que nos da, haremos uso de zsteg -a rojo.png.
- Esto analizaría el png y nos arrojaría los datos ocultos, después de ejecutar el comandos nos devuelve una serie de datos.
- Los analizamos y rápidamente nos damos cuenta de que hay cadenas en hexadecimal.
- Extraemos la cadena y la decodificamos, y esto nos la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/RED]
└─$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== | base64 -d  

picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_} 

```

## **Notas adicionales**

## **Referencias**