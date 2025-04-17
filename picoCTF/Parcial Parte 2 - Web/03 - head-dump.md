## **Descripción**
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.
Additional details will be available after launching your challenge instance.
## Hints
1. Explore backend development with us
2. The head was dumped.
## **Solución** 
Para este reto haremos lo siguiente:
- Nos vamos al link que nos dan, lo primero que hacemos es inspeccionar la pagina en busca de alguna pista.
- La pagina parece ser de noticias, en la pagina hay algunos posts los cuales contienen hashtags, después de buscar un rato nos damos cuenta que hay uno que nos redirecciona a otra pagina, http://verbal-sleep.picoctf.net:49609/api-docs
- En esta pagina se nos muestran la documentación de una API, en esta caso la de la actual pagina.
- En esta misma pagina hay un apartado llamada Diagnosing el cual contiene información acerca de el heapump.
- Usando la pista que nos brindan nos damos cuenta de que ocupamos hacer un volcado del heapdump de la pagina.
- Entonces hacemos un heapdump de la pagina de picoCTF News, con el comando curl, además le agregamos un grep y este nos da la bandera

```
curl -X 'GET' \
  'http://verbal-sleep.picoctf.net:49609/heapdump' \
  -H 'accept: */*' | grep pico
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  4 8723k    4  407k    0     0   145k      0  0:01:00  0:00:02  0:00:58  145kpicoCTF{Pat!3nt_15_Th3_K3y_388d10f7}
100 8723k  100 8723k    0     0  2313k      0  0:00:03  0:00:03 --:--:-- 2313k



picoCTF{Pat!3nt_15_Th3_K3y_388d10f7}


```

## **Notas adicionales**
Una API, o interfaz de programación de aplicaciones, es un conjunto de reglas o protocolos que permiten que las aplicaciones de software se comuniquen entre sí para intercambiar datos, características y funcionalidades.
## **Referencias**
1. 