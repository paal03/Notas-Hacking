## **Descripción**
Our flag printing service has started glitching!
Additional details will be available after launching your challenge instance.
## **Solución** 
Para este reto haremos uso del comando nc(netcat).
- Nos conectaremos al puerto 64598 del servidor jupiter.challenges.picoctf.org
- Usamos el comando nc para conectarnos de manera remota de la siguiente manera: 
  `nc [-options] hostname port[s] [ports]` |` nc jupiter.challenges.picoctf.org 64598 `
- El puerto nos manda la siguiente cadena la cual contiene unos strings que estan en hexadecimal
- Para esto usamos la pagina de cyberchef para convertir de hexadecimal a ascii.

```
└─$ nc saturn.picoctf.net 64598
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

picoCTF{gl17ch_m3_n07_a4392d2e}
```

## **Referencias**
- https://gchq.github.io/CyberChef/#input=MHgzRCA