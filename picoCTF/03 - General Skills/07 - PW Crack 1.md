## **Descripción**
Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag in the same directory too.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
- Este al ejecutar el script nos pregunta por una contraseña a cual aun no sabemos.
- Hacemos un cat al código y podemos observa que ahí esta el password en una condicion if.
- Volvemos a correr el programa, nos pide el password, lo ingresamos y nos da la bandera.

```
┌──(kali㉿kali)-[~/Documents/PWCRACK]
└─$ python level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}

```

## **Notas adicionales**

## **Referencias**