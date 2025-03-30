## **Descripción**
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/28921/` ([link](https://jupiter.challenges.picoctf.org/problem/28921/)) or http://jupiter.challenges.picoctf.org:28921
## Hints
1. You don't need to download a new web browser
## **Solución** 
Para este reto haremos lo siguiente:
-  Nos vamos al link que nos dan el cual nos lleva a un sitio web.
- Este sitio web tiene un botón que puedes presionar para obtener la bandera. Sin embargo, si lo presionas en tu navegador, te mostrará un error que dice "¡No eres Picobrowser!" y mostrará una cadena de texto.
![[Pasted image 20250330133112.png]]
- Esa cadena de texto se conoce como Agente de Usuario y le dice al servidor qué navegador estás usando.
- Para convencerlos de que estás usando el navegador Pico, simplemente cambia la cadena de agente de usuario, en este caso copiamos la bandera en formato 'curl bash'
- Este lo pegamos en una terminal linux y cambiamos el agente de usuario.
- Con esto obtenemos la siguiente bandera:

```
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/GENERAL SKILLS]
└─$ curl 'https://jupiter.challenges.picoctf.org/problem/28921/flag' \
  -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7' \
  -H 'Accept-Language: es-US,es-419;q=0.9,es;q=0.8,en;q=0.7' \
  -H 'Connection: keep-alive' \
  -b 'cf_clearance=EmLoICdkWeGrDd_Jch7UPWW4aws42yNtj2HDYknkURI-1742916792-1.2.1.1-cj_aXXqcvOpfPtW.132LprgC9zI8uj99FQaozE61AbcJ9fsdmqMOS5Q7mdK0HpPJBzzlSJFW4NYP0eRx8GosN4xPLQuUvhpfeBoRWplzZYwjWpGAvO8xHKTcURAG4MP.nRoPQqABNpLHEjs8Rf1uEH88BRoc13Yshj4ks.muKw2rsCkNccai9Wj1TbEaerXuVpXo7lvbXAJ.kDo3QJwq3Dn1X0HLt.LgnYqF_KuQOdNgNrf2ecRjhU_zUvgCxuOuI580G6lhnZKW26xPVsd7I7FnATgxgrjQlxeBq1eOxZdmHwYRfrKfmWPbr8MI1nhdGTsCrUcQR73KWG9WdQ9jkBYX1g4B.W1tSV70KBYhHKU; _ga_BSZFGM3NWK=GS1.1.1743359980.15.0.1743359984.56.0.1130321326; _ga=GA1.2.267300810.1741481023; _gid=GA1.2.1647580164.1743359985; _ga_L6FT52K063=GS1.2.1743359985.42.1.1743360821.36.0.1002072067' \
  -H 'Referer: https://jupiter.challenges.picoctf.org/problem/28921/flag' \
  -H 'Sec-Fetch-Dest: document' \
  -H 'Sec-Fetch-Mode: navigate' \   
  -H 'Sec-Fetch-Site: same-origin' \
  -H 'Sec-Fetch-User: ?1' \
  -H 'Upgrade-Insecure-Requests: 1' \       
  -H 'User-Agent: picobrowser' \                                                                                                    
  -H 'sec-ch-ua: "Chromium";v="134", "Not:A-Brand";v="24", "Google Chrome";v="134"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-platform: "Windows"' | grep pico   
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  2115  100  2115    0     0   5963      0 --:--:-- --:--:-- --:--:--  5974
 <!-- <strong>Title</strong> --> picobrowser!
 <p style="text-align:center; font-size:30px;"><b>Flag</b>:   <code>picoCTF{p1c0_s3cr3t_ag3nt_84f9c865}</code></p>

picoCTF{p1c0_s3cr3t_ag3nt_84f9c865}

```

## **Notas adicionales**
El comando `curl` ==es una herramienta de línea de comandos que permite transferir datos a través de diferentes protocolos de red==. Es de código abierto y se usa para interactuar con API, descargar archivos y probar las respuestas del servidor.
## **Referencias**
- https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers/User-Agent