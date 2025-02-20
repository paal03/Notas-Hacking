## **Descripción**
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
- Este al ejecutar el script nos pregunta por una contraseña a cual aun no sabemos.
- Hacemos un cat al código y podemos observa que hay una array con las posibles passwords.
- Podemos ingresar cada uno, de forma manual, hasta encontrar la correcta, o podemos hacer uso de un ciclo para meter todas la passwords de forma automática.
- Volvemos a correr el programa modificado y nos da la bandera

```
┌──(kali㉿kali)-[~/Documents/PWCRACK3]
└─$ python level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}

```

## **Notas adicionales**
## **Referencias**
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)