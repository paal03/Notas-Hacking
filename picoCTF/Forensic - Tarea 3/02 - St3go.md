## **Descripción**
Download this image and find the flag.
- [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)
## Hints
1. We know the end sequence of the message will be `$t3g0`.
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos el archivo que nos brindan con wget.
- Una ves que lo descargamos nos damos cuenta de que se trata de una imagen, al abrirla solo muestra una simple imagen pero nada interesante.
- Ahora nos guiamos un poco con el nombre del reto y la pista.
- Al parecer tiene que ver con la esteganografía.
- Para realizar una inspección a png que nos da, haremos uso de zsteg.
- Al ejecutar este comando junto con un grep podremos encontrar la cadena oculta que estamos buscando.
- Después de realizar analizar el png nos muestra la cadena que estamos buscando, en este caso la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/St3g0]
└─$ zsteg -a pico.flag.png | grep pico 
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a1062667}$t3g0"
/var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s': stack level too deep (SystemStackError)
from /var/lib/gems/3.1.0/gems/iostruct-0.4.0/lib/iostruct.rb:175:in `inspect'
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
from /var/lib/gems/3.1.0/gems/iostruct-0.4.0/lib/iostruct.rb:175:in `inspect'
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
from /var/lib/gems/3.1.0/gems/iostruct-0.4.0/lib/iostruct.rb:175:in `inspect'
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
from /var/lib/gems/3.1.0/gems/iostruct-0.4.0/lib/iostruct.rb:175:in `inspect'
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
 ... 10066 levels...
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
from /usr/local/bin/zsteg:25:in `load'
from /usr/local/bin/zsteg:25:in `<main>'

picoCTF{7h3r3_15_n0_5p00n_a1062667}

```

## **Notas adicionales**

## **Referencias**