## **Descripción**
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo que nos dan con wget.
- Este nos descarga un file, el cual contiene unos caracteres.
- Observando un poco nos podemos dar cuenta de que se trata de texto en base 64.
- Usamos cyberchef para esto, al parecer esta convertido a base 64 varias veces (6) despues nos arroja la bandera

```
┌──(kali㉿kali)-[~/Documents/General Skills/repetitions]
└─$ cat enc_flag                                                                        
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFpSV0VKWVZGVmtNRTVHV2tWU2JYUlVDbUpXV25sVWJGcHZWbGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}


```

## **Notas adicionales**
También podemos resolverlo utilizando base -d en la terminal de linux.
## **Referencias**
https://es.wikipedia.org/wiki/Base64
https://gchq.github.io/CyberChef/