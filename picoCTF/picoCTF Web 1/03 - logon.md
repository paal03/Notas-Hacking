## **Descripción**
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796
## Hints
1. Mmm, ¿no parece comprobar la contraseña de nadie, excepto la de Joe?
## **Solución** 
Para este reto haremos lo siguiente:
- Vamos a inspeccionar la pagina al parecer, no hay nada sospecho entonces tratamos de iniciar sesión y inspeccionamos la pagina con las herramientas de desarrollador en el apartado de red.
 ![[Pasted image 20250325173838.png]]

- Ahora para resolver este rato vamos a tener que editar las cookies de la pagina
![[Pasted image 20250325173926.png]]

Con ello obtenemos la bandera:

![[Pasted image 20250325173533.png]]

```
picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}

```

## **Notas adicionales**
**Las cookies** (a menudo conocidas como cookies de Internet) son archivos de texto con pequeños datos, como un nombre de usuario y contraseña, que se utilizan para identificar tu ordenador cuando utilizas una red. Se utilizan cookies específicas para identificar a usuarios concretos y mejorar su experiencia de navegación por la web.

## **Referencias**
- https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Cookies