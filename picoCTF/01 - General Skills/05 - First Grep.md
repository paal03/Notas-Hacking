## **Descripción**
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## **Solución** 
Para este reto haremos uso del comando grep
- Primero descargamos el archivo que nos dan con wget.
- Podemos usar file para darnos cuenta de que tipo de archivo se trata.
- Usamos el comando grep de la siguiente manera: 
- `grep [opciones] pattern [ARCHIVO]`                   `grep pico file`

```
picoCTF{grep_is_good_to_find_things_dba08a45}
```

## **Notas adicionales**
- El comando grep nos permite buscar cadenas de texto y palabras dentro de un fichero de texto. 
- grep se utiliza muy a menudo como "filtro" con otros comandos.
## **Referencias**
- https://ryanstutorials.net/linuxtutorial/grep.php