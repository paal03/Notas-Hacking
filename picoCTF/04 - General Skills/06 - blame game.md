## **Descripción**
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/158/challenge.zip)

## Hints
- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## **Solución** 
Para este reto haremos lo siguiente:
-  Primero descargamos el archivo con el enlace que nos dan con wget.
- Lo descomprimimos con unzip, aqui vamos a encontrar un archivo el cual al aparecer no tiene nada, para este reto al paracer haremos uso del control de versiones de git.
- Asi que hacemos uso de un git log message.py para ver las confirmaciones previas, y ahi esta nuestra bandera.

```
┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Blame Game/drop-in]
└─$ ls
message.py

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Blame Game/drop-in]
└─$ cat message.py 
print("Hello, World!"

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Blame Game/drop-in]
└─$ git log message.py
commit 8c83358c32daee3f8b597d2b853c1d1966b23f0a
Author: picoCTF{@sk_th3_1nt3rn_2c6bf174} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:11 2024 +0000

    optimize file size of prod code

commit caa945839a2fc0fb52584b559b4e89ac7c46bf54
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:11 2024 +0000

    create top secret project


						picoCTF{@sk_th3_1nt3rn_2c6bf174}

```

## **Notas adicionales**


## **Referencias**
https://primer.picoctf.org/#_git_version_control