## **Descripción**
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 7449`, but it doesn't speak English...
## **Solución** 
Para este reto haremos uso del comando nc(netcat).
- Nos conectaremos al puerto 25103 del servidor jupiter.challenges.picoctf.org
- Usamos el comando nc para conectarnos de manera remota de la siguiente manera: 
`nc [-options] hostname port[s] [ports]` |` nc mercury.picoctf.net 7449 `
- El puerto nos manda la siguiente bandera, la cual son numeros en ascii y necesitamos convertirlos a texto, para ello hacemos uso de una pagina web:

```
112 105 99  111  67  84  70  123  103  48  48  100  95  107  49  116  116  121  33 95  110  49 99  51  95  107  49  116  116  121  33  95  102  50  100  55  99  97  102  97  125  1

picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}
```

## **Referencias**
- https://es.rakko.tools/tools/76/