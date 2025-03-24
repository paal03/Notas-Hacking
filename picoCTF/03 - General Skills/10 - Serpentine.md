## **Descripción**
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python.
- Usamos el comando python y le anexamos el nombre del programa para correrlo.
- Este al ejecutar el script nos abre un menú con diferentes opciones al parecer hay algo mal en el código ya que una de las opciones nos debería la bandera.
- Hacemos un cat al código y podemos observar que hace falta una llamada a la función que contiene la bandera, agregamos la función en la opción de mostrar la bandera.
- Volvemos a correr el programa modificado y nos da la bandera

```
┌──(kali㉿kali)-[~/Documents/General Skills/serpentine]
└─$ python serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}

```

## **Notas adicionales**
También podemos hacer un cat el archivo python y ver el código que contiene, en este nos podemos dar cuenta de que tiene una cadena con strings que al parecer son hexadecimales, , podemos solo extraer la cadena y hacer la conversión de hexa a texto

## **Referencias**
https://gchq.github.io/CyberChef/