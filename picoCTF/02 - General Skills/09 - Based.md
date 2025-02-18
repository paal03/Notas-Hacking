## **Descripción**
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.
## **Solución** 
Para este reto haremos nos conectaremos a un servidor con netcat.
- Al parecer esta corriendo un script en el puerto
- Nos dan 3 tipos de datos(binario, octal y hexa), estos los debemos de convertir a palabras, y ingresarlos conforme los pide.
- Podemos hacer uso de cyberchef para hacer las conversiones rapidamente.

```
┌──(kali㉿kali)-[~/Documents/General Skills]
└─$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
colorado
Please give the 01100011 01101111 01101100 01101111 01110010 01100001 01100100 01101111 as a word.
...
you have 45 seconds.....

Input:
colorado
Please give me the  156 165 162 163 145 as a word.
Input:
nurse
Please give me the 74657374 as a word.
Input:
test
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}

```

## **Notas adicionales**

## **Referencias**
- https://gchq.github.io/CyberChef/