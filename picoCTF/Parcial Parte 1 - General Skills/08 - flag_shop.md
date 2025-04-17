## **Descripción**
There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/253c4651d852ac6342752ff222cf2a83/store.c). Connect with `nc jupiter.challenges.picoctf.org 9745`.
## Hints
1. Two's compliment can do some weird things when numbers get really big
## **Solución** 
Para este reto haremos lo siguiente:
- Usamos netcat para comunicarnos con un programa en C, cuyo código fuente nos fue proporcionado.
- El problema es que la bandera que hay que comprar cuesta 100.000, cuando empezamos con solo 1100.
- Para este reto haremos desbordamiento de la variable int que es entero, para invertir el signo y hacer que el coste sea negativo. El número máximo que se puede contener con int es **2147483647;** dividido entre 900 (el coste de la bandera), obtenemos **2386092** , que es el máximo teórico que podía introducir. 
- Simplemente ingresmos el valor de 240000, y podremos comprar la bandera y leerla.

```
1. Check Account Balance 
2. Buy Flags
3. Exit
    
Enter a menu selection 2 Currently for sale

1. Defintely not the flag Flag
2. 1337 Flag 1 These knockoff Flags cost 900 each, enter desired quantity 2400000
The final cost is: -2134967296
Your current balance after transaction: 2134968396
Welcome to the flag exchange We sell flags

3. Check Account Balance
4. Buy Flags
5. Exit
Enter a menu selection 2 Currently for sale

6. Defintely not the flag Flag
7. 1337 Flag 2 1337 flags cost 100000 dollars, and we only have 1 in stock Enter 1 to buy one1 YOUR FLAG IS: picoCTF{m0n3y_bag5_68d16363} Welcome to the flag exchange We sell flags picoCTF{m0n3y_bag5_68d16363
```

## **Notas adicionales**

## **Referencias**