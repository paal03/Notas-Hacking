## **Descripción**
How about trying to match a regular expression

Additional details will be available after launching your challenge instance.
## Hints
1. Access the webpage and try to match the regular expression associated with the text field
## **Solución** 
Para este reto haremos lo siguiente:
- Iniciamos la instancia que nos dan, y nos vamos al link que genera, al parecer es una pagina web
- Empezamos a inspeccionar la pagina, este contiene un recuadro, al parecer valida las entrada que coloquemos en el recuadro, cuando ingresamos algún texto nos dice lo siguiente:
	- `wrong match! Try again!`
-  Pasamos a inspeccionar el código fuente de la pagina, al mirar el código nos damos cuenta de que hay una pequeña función que es el siguiente:
- 
`function send_request() {`
	`let val = document.getElementById("name").value;`
	`// ^p.....F!?`
	`fetch(/flag?input=${val})`
	`.then(res => res.text())`
	`.then(res => {`
	`const res_json = JSON.parse(res);`
	`alert(res_json.flag)`
	`return false;`
	`})`
`return false;`
`}`
- Este código es una función JavaScript llamada `send_request()` que realiza una solicitud HTTP a un servidor y procesa la respuesta para mostrar un valor específico (en este caso, el valor de un campo denominado `flag`).
- Como sugiere el título, la entrada debe coincidir con una expresión regular particular para que aparezca la bandera.
- Este si presentamos atención al código podemos ver que hay un comentario con lo que parece ser una expresión `// ^p.....F!?`
- Entonces la expresion que estamos buscando obligatoriamente necesita empezar por ***p*** y terminar con ***F***, ademas de tener una longitud de 7 caracteres.
- Procedemos a colocar en la caja texto cualquier cosa con esta característica por ejemplo (pqwertF, p12345F o picoCTF) y nos da la bandera.
 ![[Pasted image 20250403215453.png]]

```
picoCTF{succ3ssfully_matchtheregex_9080e406}

```

## **Notas adicionales**

## **Referencias**
https://regexr.com/
