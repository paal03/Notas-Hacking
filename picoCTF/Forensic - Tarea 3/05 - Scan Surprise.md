## **Descripción**
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/16/challenge.zip)
Additional details will be available after launching your challenge instance.
## Hints
1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de un archivo .zip, lo descomprimimos y nos devuelve unas carpetas anidadas.
- Al ingresar a cada carpeta, llegamos al final, y encontramos un imagen, la abrimos y se trata de un código qr.
- Solo basta con escanear el código y nos dará la respuesta.


```

```

## **Notas adicionales**

## **Referencias**