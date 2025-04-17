## **Descripción**
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py) using [this password](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/pw.txt) to get [the flag](https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/flag.txt.en)?
## Hints
1. Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/8e33ede04d02f3765b8c6a6e24d72733/ende.py`
2. `$ man python`

## **Solución** 
Para este reto haremos lo siguiente:
- Primero, necesitamos descargar los archivos del desafío que contendrán un script de Python, un archivo de texto codificado que contiene la bandera y un archivo de contraseña, para ello usaremos el comando wget.
- Los dos archivos de texto son la bandera codificada y la contraseña, veamos el script de Python usándolo `cat`para leer su contenido.
- Este script, vemos que está diseñado para interactuar con un archivo llamado "pole.txt" y que admite dos argumentos (-e/-d).
- Utilizamos el `cp`comando para copiar el archivo “flag.txt.en” y cambiarle el nombre a “pole.txt”.
-  Ejecutamos `python3 ende.py -d pole.txt`para volcar la bandera. 

```
picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
```

## **Notas adicionales**

## **Referencias**