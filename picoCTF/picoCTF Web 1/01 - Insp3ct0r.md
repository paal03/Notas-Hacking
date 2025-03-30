## **Descripción**
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/44924/` ([link](https://jupiter.challenges.picoctf.org/problem/44924/)) or http://jupiter.challenges.picoctf.org:44924
## Hints
1. How do you inspect web code on a browser?
2. There's 3 parts
## **Solución** 
Para este reto haremos lo siguiente:
- Sabemos que la bandera esta dividida en 3 partes así que:
- Primero primero vemos el código fuente de la pagina.
- Segundo pasamos a inspeccionar la pagina web, lo común seria irnos a los recursos y checar el javascript y el CSS. 
- Con esto obtenemos la siguiente bandera
```
|<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->|
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?f10be399} */

```

## **Notas adicionales**


## **Referencias**
