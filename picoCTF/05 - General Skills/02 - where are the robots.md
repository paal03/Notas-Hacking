## **Descripción**
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/56830/` ([link](https://jupiter.challenges.picoctf.org/problem/56830/)) or http://jupiter.challenges.picoctf.org:56830
## Hints
1. What part of the website could tell you where the creator doesn't want you to look?
## **Solución** 
Para este reto haremos lo siguiente:
- Empezamos a inspeccionar la pagina pero no miramos nada sospechoso
- Un archivo robots.txt contiene instrucciones que indican a los bots a qué páginas web pueden y no pueden acceder.
- Podemos acceder el robots.txt, escribiendo esta cadena en el URL.
- Esto nos mostrará lo siguiente User-agent: *
						 Disallow: /1bb4c.html
- Ahora solo queda buscar esa ruta y obtenemos la bandera.

```

picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}

```

## **Notas adicionales**
Un archivo robots.txt es un conjunto de instrucciones para [bots](https://www.cloudflare.com/learning/bots/what-is-a-bot/). Este archivo está incluido en los archivos fuente de la mayoría de los sitios web. Los archivos robots.txt están diseñados principalmente para gestionar las actividades de los bots beneficiosos, como los [rastreadores web](https://www.cloudflare.com/learning/bots/what-is-a-web-crawler/), ya que es poco probable que los bots perjudiciales sigan las instrucciones.

## **Referencias**
https://www.cloudflare.com/es-es/learning/bots/what-is-robots-txt/