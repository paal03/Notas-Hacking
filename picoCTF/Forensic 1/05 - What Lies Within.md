## **Descripción**
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
## Hints
1. There is data encoded somewhere... there might be an online decoder.
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos dan con wget y lo guardamos en una carpeta.
- Al parecer se trata de una imagen png, usamos strings y  grep para filtrar las cadenas de texto de la imagen, sin embargo no parece haber nada.
- Ahora como no parce haber nada interesante a simple vista, tal vez haya datos ocultos.
- Haremos uso de una herramienta de esteganografía llamda zsteg esta nos dara los datos ocultos dentro de la imagen.
- Tambien podemos usar zsteg junto con grep para filtar los datos.
- Esto nos dara la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/What Lies Within]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
```

## **Notas adicionales**
La esteganografía **es la práctica de ocultar información dentro de otro mensaje u objeto físico para evitar su detección**. Se puede usar para ocultar casi cualquier tipo de contenido digital, ya sea texto, imágenes, videos o audios. Luego, dichos datos ocultos se extraen en destino.
## **Referencias**
https://latam.kaspersky.com/resource-center/definitions/what-is-steganography#:~:text=La%20esteganograf%C3%ADa%20es%20la%20pr%C3%A1ctica,ocultos%20se%20extraen%20en%20destino.