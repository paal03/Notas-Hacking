## **Descripción**

## Hints
1. Look at the problem category
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos a la liga que nos dan, este nos manda a un pagina web
- Inspeccionamos la pagina en busca de algo, pero solo vemos lo que parece ser una imagen.
- Descargamos dicha imagen.
- Ahora parece que hay datos ocultos dentro de la imagen así que para ello usaremos la herramienta de zsteg.
- Al usar zsteg -a analizaremos el archivo y nos devolverá los datos ocultos.
- Para mayor rapidez le agregamos un grep con una indicio de lo que estamos buscando.
- Esto nos devolver a la bandera.


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/MilkSlap]
└─$ zsteg -a concat_v.png | grep pico 
/var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:303:in `upto': stack level too deep (SystemStackError)
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:303:in `decoded_bytes'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:319:in `block in decoded_bytes'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `upto'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:318:in `decoded_bytes'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line/mixins.rb:17:in `prev_scanline_byte'
        from /var/lib/gems/3.1.0/gems/zpng-0.4.5/lib/zpng/scan_line.rb:377:in `prev_scanline_byte'
         ... 9483 levels...
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/MilkSlap]
└─$ export RUBY_THREAD_VM_STACK_SIZE=5000000000       

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/MilkSlap]
└─$ zsteg -a concat_v.png | grep pico          
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"
zsh: killed     zsteg -a concat_v.png | 
zsh: done       grep --color=auto pico
```

## **Notas adicionales**

## **Referencias**