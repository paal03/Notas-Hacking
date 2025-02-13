## **Descripción**
Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `25103` to get the flag?
## **Solución** 
Para este reto haremos uso del comando nc(netcat).
- Nos conectaremos al puerto 25103 del servidor jupiter.challenges.picoctf.org
- Usamos el comando nc para conectarnos de manera remota de la siguiente manera: 
`nc [-options] hostname port[s] [ports]` |` nc jupiter.challenges.picoctf.org 25103 `
- El puerto nos manda la siguiente bandera:

```
picoCTF{nEtCat_Mast3ry_d0c64587}
```

## **Notas adicionales**
- Netcat es la navaja suiza de las herramientas de red. Puede leer y escribir datos en la red mediante TCP y UDP.
## **Referencias**
- https://www.ionos.mx/digitalguide/servidores/herramientas/netcat/