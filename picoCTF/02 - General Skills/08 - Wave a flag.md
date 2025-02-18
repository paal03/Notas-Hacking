## **Descripción**
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el programa que nos dan con `wget`.
- Usamos un `file` para saber de que archivo se trata.
- Dado que es un ejecutable le damos permiso se ejecución con `chmod`.
- Lo ejecutamos y nos pide que le agregamos un -`h`, al realizar esto nos da la bandera.

```
──(kali㉿kali)-[~/Documents/General Skills/Wave a flag]
└─$ file warm 
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3181a501366281ab5eba1c41e54a1f40800e3966, with debug_info, not stripped

┌──(kali㉿kali)-[~/Documents/General Skills/Wave a flag]
└─$ chmod +x warm

┌──(kali㉿kali)-[~/Documents/General Skills/Wave a flag]
└─$ ./warm   
Hello user! Pass me a -h to learn what I can do!

┌──(kali㉿kali)-[~/Documents/General Skills/Wave a flag]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

```

## **Notas adicionales**

## **Referencias**
https://openwebinars.net/blog/15-atajos-teclado-mas-utilizados-shell-linux/