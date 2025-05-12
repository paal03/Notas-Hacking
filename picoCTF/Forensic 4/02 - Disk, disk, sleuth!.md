## **Descripción**
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)
## Hints
1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!
## **Solución** 
Para este reto haremos lo siguiente:
- Descargaremos la imagen con la liga que nos dan.
- Ahora descomprimimos el archivo.
- Primero usamos mmls para ver la estructura.
- Como se menciona en la descripción de la pregunta, usaremos srch_strings, junto con grep para filtrar de mejor manera la salida de los datos.
- Con esto nos dará la bandera

```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/Disk, disk, sleuth]
└─$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}

```

## **Notas adicionales**

## **Referencias**