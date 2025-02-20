## **Descripción**
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
- Al parecer hay algo mal en el código y no lo corre.
- Después de analizar el código nos damos cuenta de que solamente hay una mala identacion.
- Al corregir el error, podemos ejecutarlo y nos da la bandera.

```
┌──(kali㉿kali)-[~/Documents/General Skills/fixme1.py]
└─$ python fixme1.py 
That is correct! Here is  your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}

```

## **Notas adicionales**
También podemos hacer un cat el archivo python y ver el código que contiene, en este nos podemos dar cuenta de que tiene una cadena con strings que al parecer son hexadecimales, , podemos solo extraer la cadena y hacer la conversión de hexa a texto

## **Referencias**
