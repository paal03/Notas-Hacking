## **Descripción**
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Descargaremos la imagen con la liga que nos dan.
- Ahora descomprimimos el archivo zip.
- Primero usamos mmls para ver la estructura.
- Ahora con este información, podemos ver el tamaño de las particiones.
- Ahora con esto podremos listar los nombres y directorios de dicha partición.
- Después de navegar en el disco, encontramos el inodo número 472 contiene la carpeta `root`, lo cual parece un buen comienzo. Por lo tanto, busca su contenido usando el `fls`comando una vez más, pero ahora también usamos el número de inodo.
- Encontramos flag.txt.enc en el inodo 1782. En el inodo 1876 también hay un flag.txt, pero como tiene un asterisco, ya está eliminado. 
- Ahora bien, como la `.enc`extensión "file" significa que el archivo está cifrado, debemos encontrar la manera de descifrarlo también.
- Para encontrar la clave, la encontraremos usando openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k.
- Ahora que tenemos el archivo decodificado, solo queda ver el archivo decodificado y de esta manera obtendremos la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationorchid]
└─$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40C77D04187F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationorchid]
└─$ ls
disk.flag.img  flag.txt  flag.txt.enc

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationorchid]
└─$ cat flag.txt 
picoCTF{h4un71ng_p457_1d02081e}                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationorchid]
└─$ cat flag.txt.enc 
Salted__S�+%���+�O��k�ђ(A����c��
                                @]ԣ
L�ޢȤ7� ���؎$�'%                                                                                                                                                                                                                  

```

## **Notas adicionales**

## **Referencias**