## **Descripción**
Run the Python script `code.py` in the same directory as `codebook.txt`.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Lo descomprimimos con unzip, aqui vamos a encontrar un archivo el cual al aparecer no tiene nada, para este reto al paracer haremos uso del control de versiones de git.
- Asi que hacemos uso de un git log para ver las confirmaciones previas, y ahi esta nuestra bandera

```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/GENERAL SKILLS/time machine]
└─$ ls
challenge.zip  drop-in

┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/GENERAL SKILLS/time machine]
└─$ cd drop-in      

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/time machine/drop-in]
└─$ ls
message.txt

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/time machine/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                                                                                                                                                                  
┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/time machine/drop-in]
└─$ git log             
commit 3339c144a0c78dc2fbd3403d2fb37d3830be5d94 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:22 2024 +0000

    picoCTF{t1m3m@ch1n3_d3161c0f}


```

## **Notas adicionales**


## **Referencias**
https://primer.picoctf.org/#_git_version_control