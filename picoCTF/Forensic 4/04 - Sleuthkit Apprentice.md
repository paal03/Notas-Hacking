## **Descripción**
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Descargaremos la imagen con la liga que nos dan.
- Ahora descomprimimos el archivo zip.
- Primero usamos mmls para ver la estructura.
- Ahora con este información, podemos ver el tamaño de las particiones.
- Ahora con esto podremos listar los nombres y directorios de dicha partición.
- Después de navegar hasta la ruta indicada, usaremos icat para visualizar el contenido de ese sector de la partición donde se encontrara la bandera.
- Con esto obtendremos la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Sleuthkit apprentice]
└─$ icat -o 0000360448 disk.flag.img -r 2371
picoCTF{by73_5urf3r_2f22df38}

```

## **Notas adicionales**

## **Referencias**