	## **Descripción**
	Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)
	## **Solución** 
	Para este reto haremos lo siguiente:
	- Primero descargamos el archivo con el enlace que nos dan con wget.
	- Este se trata de un script hecho en python.
	- Usamos el comando python y le anexamos el nombre del programa para correrlo.
	- Este al ejecutar el script nos pregunta por la conversion de un numero decimal a binario al ingresar la respuesta nos da la bandera.
	
	```
	┌──(kali㉿kali)-[~/Documents/General Skills/converme.py]
	└─$ python convertme.py 
	If 31 is in decimal base, what is it in binary base?
	Answer: 11111
	That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}
	
	```
	
	## **Notas adicionales**
	También podemos hacer un cat el archivo python y ver el código que contiene, en este nos podemos dar cuenta de que tiene una cadena con strings que al parecer son hexadecimales, , podemos solo extraer la cadena y hacer la conversión de hexa a texto
	
	## **Referencias**
	- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
	- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)