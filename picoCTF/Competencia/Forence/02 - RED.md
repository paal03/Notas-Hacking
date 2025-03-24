## **Descripción**
RED, RED, RED, REDDownload the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
## Hints
1. The picture seems pure, but is it though?.
2. Red?Ged?Bed?Aed?
3. Check whatever Facebook is called now.
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo con wget, este se trata de un png.
- Lo abrimos y parece ser solo una png en rojo.
- Verificamos la estructura del png con un volcado hexadecimal y al parecer, los encabezados estan bien.
- Checamos los metadatos del png con(exiftool) y vemos un texto extraño, entonces trataremos hacer uso de herramientas de estenografía para descartar que haya texto escondido en el png.
- Haremos uso de la herramienta zsteg.
- Con esto encontramos un texto en base64
- Lo decodificamos y nos da la bandera.
```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE]
└─$ zsteg red.png 
meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="                                                                                                                                                                                         
b1,rgba,msb,xy      .. file: OpenPGP Public Key
b2,g,lsb,xy         .. text: "ET@UETPETUUT@TUUTD@PDUDDDPE"
b2,rgb,lsb,xy       .. file: OpenPGP Secret Key
b2,bgr,msb,xy       .. file: OpenPGP Public Key
b2,rgba,lsb,xy      .. file: OpenPGP Secret Key
b2,rgba,msb,xy      .. text: "CIkiiiII"
b2,abgr,lsb,xy      .. file: OpenPGP Secret Key
b2,abgr,msb,xy      .. text: "iiiaakikk"
b3,rgba,msb,xy      .. text: "#wb#wp#7p"
b3,abgr,msb,xy      .. text: "7r'wb#7p"
b4,b,lsb,xy         .. file: 0421 Alliant compact executable not stripped


picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

```

## **Notas adicionales**
zsteg: Detectar datos ocultos en formato stegano en PNG y BMP

## **Referencias**
https://github.com/zed-0xff/zsteg
