## **Descripción**
Run the Python script `code.py` in the same directory as `codebook.txt`.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python y den un txt que al paracer su contenido esta encriptado o codificado.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
- Este al ejecutar el script abre el archivo .txt y nos da la bandera.

```
┌──(kali㉿kali)-[~/Documents/General Skills/Codebook]
└─$ ls
codebook.txt  code.py  random

┌──(kali㉿kali)-[~/Documents/General Skills/Codebook]
└─$ python code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}

```

## **Notas adicionales**
También podemos hacer un cat el archivo python y ver el código que contiene, en este nos podemos dar cuenta de que tiene una cadena con strings que al parecer son hexadecimales, , podemos solo extraer la cadena y hacer la conversión de hexa a texto

## **Referencias**
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)