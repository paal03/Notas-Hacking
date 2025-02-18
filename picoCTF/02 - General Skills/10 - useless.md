## **Descripción**
There's an interesting script in the user's home directoryThe work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     60986
Username: picoplayer
Password: password
```
## **Solución** 
Para este reto haremos nos conectaremos a un servidor con `ssh`.
- Al ingresar nos damos cuenta de que hay un script.
- Lo ejecutamos y nos pide que leamos el código primero
- Leemos el manual del script y nos damos cuenta de que ahí esta la bandera.

```
picoplayer@challenge:~$ ./useless 
Read the code first
picoplayer@challenge:~$ man useless 

useless
     useless, — This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_8504}

```

## **Notas adicionales**

## **Referencias**
