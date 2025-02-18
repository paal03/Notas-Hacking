## **Descripción**
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static)? This [BASH script](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh) might help!
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el script y el bash que nos dan con wget.
- Debemos ejecutar el bash y pasarle el script, esto nos devuelve dos archivos
- Hacemos uso del comando grep y obtenemos la bandera.

```
┌──(kali㉿kali)-[~/Documents/General Skills/Static ain't always noise]
└─$ ./ltdis.sh static   
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset

┌──(kali㉿kali)-[~/Documents/General Skills/Static ain't always noise]
└─$ ls
ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt

┌──(kali㉿kali)-[~/Documents/General Skills/Static ain't always noise]
└─$ grep pico static.ltdis.strings.txt 
   1020 picoCTF{d15a5m_t34s3r_ccb2b43e}

					picoCTF{d15a5m_t34s3r_ccb2b43e}

```

## **Notas adicionales**
También podemos resolverlo utilizando el comando grep desde el inicio.
## **Referencias**
ninguna