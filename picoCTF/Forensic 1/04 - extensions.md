## **Descripción**
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Hints
1. How do operating systems know what kind of file it is? (It's not just the ending!
2. Make sure to submit the flag as picoCTF{XXXXX}
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos dan con wget y lo guardamos en una carpeta.
- A simple vista se puede observar de que se trata de un archivo de texto por la extensión.
- Se recomienda utilizar el comando file para conocer el tipo de archivo exacto.
- En este caso si utilizamos este comando, podemos ver de que el archivo no es un txt, sino un png
- Así que lo que haremos será guardar el archivo nuevamente con una nueva extensión la cual será .png.
- Al abrir el png esta nos mostrara la bandera.

```
picoCTF{now_you_know_about_extensions}
```

## **Notas adicionales**
El comando `file` es una herramienta en sistemas Unix y Linux que se utiliza para determinar el tipo de archivo de un archivo o para identificar su contenido. Puedes pensar en él como una herramienta que «lee» el archivo y ofrece información sobre su naturaleza, como si es un archivo de texto, una imagen, un archivo ejecutable, un archivo comprimido, etc.
## **Referencias**
https://www.iespai.com/2023/09/07/el-comando-file/#google_vignette