## **Descripción**
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
-  Al parecer hay algo mal en el código y no lo corre.
- Después de analizar el código nos damos cuenta de que solamente esta mal la condicion del if, al parecer le hace falta un = en la condicion, esta tiene = y debe ser == doble.
- Al corregir el error, podemos ejecutarlo y nos da la bandera.


```
┌──(kali㉿kali)-[~/Documents/General Skills/fixme1.py]
└─$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

					picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## **Notas adicionales**
También podemos hacer un cat el archivo python y ver el código que contiene, en este nos podemos dar cuenta de que tiene una cadena con strings que al parecer son hexadecimales, , podemos solo extraer la cadena y hacer la conversión de hexa a texto

## **Referencias**