## **Descripción**
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/149ab4b27d16922142a1e8381677d76f/cat.jpg)
## Hints
1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de una imagen, al abrirla solo muestra una simple imagen pero nada interesante.
- Lo primero que hacemos es proceder a ver los metadatos con el comando exiftool.
- Esto nos mostrará los metadatos de la imagen.
- Si inspeccionamos un poco nos damos cuenta de que en una parte se encuentra una cadena que parece estar en hexadecimal.
- Procedemos a decodificar esta cadena y nos brinda la bandera.

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/information]
└─$ exiftool cat.jpg     
ExifTool Version Number         : 13.10
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2021:03:15 14:24:46-04:00
File Access Date/Time           : 2025:05:11 19:48:16-04:00
File Inode Change Date/Time     : 2025:05:11 19:48:08-04:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1

cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9

picoCTF{the_m3tadata_1s_modified}
```

## **Notas adicionales**

## **Referencias**