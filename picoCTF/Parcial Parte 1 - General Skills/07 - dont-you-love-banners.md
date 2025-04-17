## **Descripción**
Can you abuse the banner?
Additional details will be available after launching your challenge instance.
## Hints
1. Do you know about symlinks?
2. Maybe some small password cracking or guessing
## **Solución** 
Para este reto haremos lo siguiente:
-  Para este reto nos dan un servidor y 2 puertos distintos.
-  Al conectarnos al primer puerto este nos brinda una contraseña la cual nos sirve
	para conectarnos al segundo puerto.
- Despues de conectarnos nos salta un banner y nos realizan 3 preguntas al contestarlas nos logeamos en la shell.
- Para este reto hicimos uso de los symlinks, apuntamos el nombre de la bandera flag.txt endonde se encontraba el banner y eliminamos el banner que ya habia.
- Entonces cuando se fuera a ejecutar el banner nuevamente este ahora iba a leer la flag ya que apuntamos a esta haciendo uso del nombre del banner

```
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_1226c9b0}
```

## **Notas adicionales**

## **Referencias**
