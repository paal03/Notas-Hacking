## **Descripción**
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 60638`
## **Solución** 
Para este reto haremos lo siguiente:
- Nos conectamos a un servidor el cual esta corriendo un script el cual al parecer esta pidiendo el resultado de 6 diferentes operaciones.
- Solo debemos ir haciendo las operaciones que nos dicen con los 2 números que nos dan en binario.
- Al final de responder las 6 preguntas nos dan la bandera.

```
┌──(kali㉿kali)-[~/…/Binary Search/home/ctf-player/drop-in]
└─$ nc titan.picoctf.net 60638

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10101111
Binary Number 2: 10011000


Question 1/6:
Operation 1: '*'
Perform the operation on Binary Number 1&2. 
Enter the binary result: 0110011111101000
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 101011110
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01001100
Correct!

Question 4/6:
Operation 4: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10001000
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 000101000111
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10111111 
Correct!

Enter the results of the last operation in hexadecimal: BF

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6862762d}

```

## **Notas adicionales**


## **Referencias**
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)