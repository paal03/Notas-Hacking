## **Descripción**
Jacky has learnt about the importance of strong passwords and made sure to encrypt the BitLocker drive with a very long and complex password. We managed to capture the RAM while this drive was opened however. See if you can break through the encryption!Download the disk image [here](https://challenge-files.picoctf.net/c_verbal_sleep/b22e1ca13c0b82bb85afe5ae162f6ecbdf5b651e364e6a2b57c9ad44ae0b3bfd/bitlocker-2.dd) and the RAM dump [here](https://challenge-files.picoctf.net/c_verbal_sleep/b22e1ca13c0b82bb85afe5ae162f6ecbdf5b651e364e6a2b57c9ad44ae0b3bfd/memdump.mem.gz)
#### **Hints**
1.Try using a volatility plugin
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos la imagen del disco, este tiene por nombre bitlocker-1.dd y el volcado de memoria que tiene por nombre memdump.mem.
- El reto nos menciona que este puede ser resuelto utilizando volatility, pero antes de usarlo quise hacer uso de algo mas como lo es strings y grep.
- Haciendo uso de estos comando en el volcado de memoria obtenemos la bandera sin hacer otra cosa, aunque al parce hay otra forma de resolverlo con volatility.


```

┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE/Bitlocker-2]
└─$ strings memdump.mem | grep -i "picoCTF"            
picoCTF{B1tl0ck3r_dr1v3_d3crypt3d_9029ae5b}
picoCTF{B1tl0ck3r_dr1v3_d3crypt3d_9029ae5b}
picoCTF{B1tl0ck3r_dr1v3_d3crypt3d_9029ae5b}


```


## **Notas adicionales**

## **Referencias**


