## **Descripción**
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.
## Hints
1. In the country that doesn't exist, the flag persists
## **Solución** 
Para este reto haremos lo siguiente:
- Primero debemos de iniciar una instancia que aloja un servidor el cual tiene una pagina web, esta tiene muchas banderas en formato png de diferentes países.
-  La pista nos dice que hay un país que no existe pero se encuentra ahí.
- Después de buscar dentro de todas las pagina, se encontró uno con el siguiente nombre(Upanzi, Republic The) con su respectiva bandera, lo googleamos y nos damos cuenta que efectivamente no se trata de un país.
- Siguiendo la pista que nos dan procedemos a descargar el png de la bandera .
- Analizamos los metadatos y al parecer el png es demasiado grande entonces probablemente hay datos o archivos ocultos dentro del png.
- Primero usamos binwalk pero no hay nada extraño.
- Después podemos usar zsteg pero les puede dar algun error ya que es damasiado grande, entonces hacemos uso de stepic 
- Usando el comando stepic nos arroja la bandera.
```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE]
└─$ stepic -i upz.png -d
/usr/lib/python3/dist-packages/PIL/Image.py:3368: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(
picoCTF{fl4g_h45_fl4ga664459a} 
```

## **Notas adicionales**
Si ponemos atención al nombre del reto nos podemos dar cuenta que hacen referencia a la herramienta utilizada para resolver el reto. 

stepic: Esteganografía de imágenes en Python

## **Referencias**
https://code.tools/man/1/stepic/
