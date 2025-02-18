## **Descripción**
Unzip this archive and find the file named 'uber-secret.txt'
## **Solución** 
Para este reto haremos uso del comando grep
- Primero descargamos el archivo que nos dan con wget.
- Este nos descarga un archivo zip, el cual descomprimo.
- Nos damos cuenta de que se encuentran muchos archivos, carpetas y subcarpetas.
- Para filtrar el contenido, haremos uso del comando grep de la siguiente manera: 
- `find -name [ARCHIVO]`                   `find -name uber-secret.txt  `

```
┌──(kali㉿kali)-[~/Documents/General Skills/First Find/files]
└─$ find -name uber-secret.txt                                                     
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

┌──(kali㉿kali)-[~/Documents/General Skills/First Find/files]
└─$ cat adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

picoCTF{f1nd_15_f457_ab443fd1}
```

## **Notas adicionales**
El comando `grep -r` en Linux o sistemas Unix se utiliza para buscar recursivamente en los archivos dentro de un directorio. La opción `-r` (o `--recursive`) hace que `grep` busque no solo en el directorio especificado, sino también en todos sus subdirectorios.
## **Referencias**
- https://ryanstutorials.net/linuxtutorial/grep.php