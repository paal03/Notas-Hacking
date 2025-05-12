## **Descripción**
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- 


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Sleuthkit apprentice]
└─$ icat -o 0000360448 disk.flag.img -r 2371
picoCTF{by73_5urf3r_2f22df38}

```

## **Notas adicionales**

## **Referencias**