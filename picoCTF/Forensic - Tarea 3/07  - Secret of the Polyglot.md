## **Descripción**
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
## Hints
1. This problem can be solved by just opening the file in different ways
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de un archivo en pdf.
- Lo abrimos y nos da una mitad de lo que parece ser la bandera.
- Realizamos un volcado hexadecimal y observamos los datos, al parecer hay algo raro con los encabezados, al analizar un poco nos damos cuenta de que tiene la estructura de un png.
- Ahora copiamos este mismo pdf y le cambiamos la extensión a png, además de cambiarle el nombre para no confundirnos.
- Ahora solo basta con abrir el png, y esto nos mostrara la otra mitad de la bandera.
- Solo queda juntar ambas mitades y tendremos la bandera completa.


```
1n_pn9_&_pdf_7f9bccd1}
```

## **Notas adicionales**

## **Referencias**