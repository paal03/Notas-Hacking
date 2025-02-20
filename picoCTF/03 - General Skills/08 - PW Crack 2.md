## **Descripción**
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
-  Este al ejecutar el script nos pregunta por una contraseña a cual aun no sabemos.
- Hacemos un cat al código y podemos observa que ahí esta el password en una condicion if.
- En esta ocacion el password esta en formato diferente, al paracer esta en hexadecimal, usamos cybercef para realizar la conversion y obtenemos lo siguiente:
- HEXA ---- 33 39 63 65        =        Text -------- 39ce 
- Volvemos a correr el programa, nos pide el password, lo ingresamos y nos da la bandera.

```
┌──(kali㉿kali)-[~/Documents/PWCRACK2]
└─$ python level2.py        
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}

```

## **Notas adicionales**

## **Referencias**
https://gchq.github.io/CyberChef/#recipe=From_Hex('Space')&input=MzMgMzkgNjMgNjU