## **Descripción**
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Descargaremos la imagen con la liga que nos dan.
- Ahora descomprimimos el archivo zip.
- Primero usamos mmls para ver la estructura.
- Ahora con este información, podemos ver el tamaño de las particiones.
- Nos conectamos al servidor mencionado con NC.
- Ya solo basta con introducir la respuesta a la pregunta que nos hacen.
- Con esto nos darán la bandera.

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Sleuthkit tools]
└─$ mmls -M disk.img            
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Sleuthkit tools]
└─$ nc saturn.picoctf.net 49222
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
picoCTF{mm15_f7w!}

```

## **Notas adicionales**

## **Referencias**