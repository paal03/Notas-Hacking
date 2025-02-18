## **Descripción**
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el file que nos dan con `wget`.
- Dado que es un archivo .zip usamos `unzip` para descomprimirlo
- Dado que hay carpetas dentro de otras recursivamente, podemos usar solamente la tecla `tab`, colocamos el comando `cd` y después damos múltiples `tab`.
- Cuando llegamos a la carpeta final, nos encontramos con un ejecutable, el cual ejecutamos y nos la la bandera.

```
┌──(kali㉿kali)-[~/Documents/General Skills/tab tab]
└─$ ls
Addadshashanammu  Addadshashanammu.zip

┌──(kali㉿kali)-[~/Documents/General Skills/tab tab]
└─$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku              

┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}


				picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}

```

## **Notas adicionales**
En Linux, la tecla de tabulación (Tab) se utiliza para completar automáticamente comandos y rutas de archivos. También se puede usar para navegar entre opciones..
## **Referencias**
https://openwebinars.net/blog/15-atajos-teclado-mas-utilizados-shell-linux/