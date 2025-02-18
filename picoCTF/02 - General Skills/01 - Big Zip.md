## **Descripción**
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.

## **Hints**
Can grep be instructed to look at every file in a directory and its subdirectories.
## **Solución** 
Para este reto haremos uso del comando grep
- Primero descargamos el archivo que nos dan con wget.
- Este nos descarga un archivo zip, el cual descomprimo.
- Nos damos cuenta de que se encuentran muchos archivos, carpetas y subcarpetas.
- Para filtrar el contenido, haremos uso del comando grep de la siguiente manera: 
- `grep -r pattern [ARCHIVO]`                   `grep -r pico `

```
└─$ grep -r pico
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

picoCTF{gr3p_15_m4g1c_ef8790dc}

```

## **Notas adicionales**
El comando `grep -r` en Linux o sistemas Unix se utiliza para buscar recursivamente en los archivos dentro de un directorio. La opción `-r` (o `--recursive`) hace que `grep` busque no solo en el directorio especificado, sino también en todos sus subdirectorios.
## **Referencias**
- https://ryanstutorials.net/linuxtutorial/grep.php