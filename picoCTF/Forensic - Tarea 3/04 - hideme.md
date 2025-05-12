## **Descripción**
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/260/flag.png).
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de una imagen, al abrirla solo muestra una simple imagen pero nada interesante.
- Ahora nos ayudaremos un poco con el titulo del reto, así que usaremos el comando binwalk para ver que no haya archivos ocultos.
- Al parecer si hay archivos dentro de la imagen así que procedemos a extraerlos usando el mismo comando binwalk -e
- Ahora nos extrae una carpeta, dentro de esta se encontrara otra imagen, pero al abrir esta nos dará la imagen.


```

```

## **Notas adicionales**

## **Referencias**