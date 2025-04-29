## **Descripción**
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Hints
1. Try fixing the file header
## **Solución** 
Para este reto haremos lo siguiente:
- Para este reto tenemos que editar el encabezado del archivo en este caso nos damos cuenta de que se trata de un PNG. Verificamos el encabezado de los png y editamos nuestro archivo:
- En general un png esta compuesto por 4 chunks (HDR, PLTE, IDAT, END)
- NOTA: Nos podemos apoyar de pngcheck.

![[03 - c0rrupt.png]]

```
picoCTF{C0rrupt10n_1847995}
```

## **Notas adicionales**
PNG es la abreviatura de _Portable Network Graphics_ y es un archivo de imagen
## **Referencias**
https://medium.com/@0xwan/png-structure-for-beginner-8363ce2a9f73