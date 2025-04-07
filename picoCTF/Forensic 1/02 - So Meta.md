## **Descripción**
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
## Hints
1. What does meta mean in the context of files?
2. Ever heard of metadata?
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos dan con wget y lo guardamos en una carpeta.
- Lo primero es abrir la imagen en busca de algo, al parecer no hay nada a simple vista.
- La pista nos hablan sobre los metadatos.
- Para ver los metadatos de cualquier cosa podemos usar la herramienta exiftool, esta nos permitirá ver los metadatos de la imagen, en este caso podremos ver la bandera.
		exiftool pico_img.png  

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/So meta]
└─$ exiftool pico_img.png  
ExifTool Version Number         : 13.10
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2020:10:26 14:38:23-04:00
File Access Date/Time           : 2025:04:07 13:35:43-04:00
File Inode Change Date/Time     : 2025:04:07 13:35:35-04:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Warning                         : [minor] Text/EXIF chunk(s) found after PNG IDAT (may be ignored by some readers)
Artist                          : picoCTF{s0_m3ta_d8944929}
Image Size                      : 600x600
Megapixels                      : 0.360



		picoCTF{s0_m3ta_d8944929}

```

## **Notas adicionales**
Los metadatos son información adicional sobre otros datos.
Exiftool es una herramienta de línea de comandos_ la cual nos permite analizar los metadatos de diversos formatos de archivos.
## **Referencias**
1. https://www.welivesecurity.com/la-es/2022/12/19/metadatos-fotos-podrian-mostrar-mas/
2. https://duriva.com/exiftool-guia-para-el-analisis-forense-de-metadatos-de-fotos-y-archivos/