## **Descripción**
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `ee388b88`
Additional details will be available after launching your challenge instance.
## **Solución** 
Para este reto haremos nos conectamos a un servidor vía SSH 
- Al ingresar al servidor nos damos cuenta que la bandera esta dividida en 3 partes, en el directorio actual que existen 2 archivos uno que nos menciona una parte de la bandera y otra las instrucciones que debe ir siguiendo para encontrar las bandera.
- Solo es ir haciendo `cat` a los archivos y cambiando de directorios.

```
picoCTF{xxsh_0ut_0f_\/\/4t3r_3ca613a1}
```

## **Notas adicionales**
NO HAY
## **Referencias**
NO HAY