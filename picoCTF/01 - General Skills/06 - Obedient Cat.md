## **Descripción**
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag).
## **Solución** 
Para este reto haremos uso del comando cat.
- Primero descargamos el archivo que nos dan con wget.
- Podemos usar file para darnos cuenta de que tipo de archivo se trata.
- Usamos el comando cat para leer el contenido del archivo de la siguiente manera: 
	`cat [OPTION] [FILE]`                   `cat flag`
- Con esto obtenemos la bandera:

```
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
```

## **Notas adicionales**
- El comando cat se utiliza para mostrar, concatenar y crear archivos de texto.
## **Referencias**
- https://www.hostinger.mx/tutoriales/comando-cat-linux