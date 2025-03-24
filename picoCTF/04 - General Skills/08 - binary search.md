## **Descripción**
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/19/challenge.zip)

Additional details will be available after launching your challenge instance.
## Hints
- Have you ever played hot or cold? Binary search is a bit like that.
- You have a very limited number of guesses. Try larger jumps between numbers!
- The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Este se trata de un script hecho en python el cual genera un numero aleatorio y debemos de adivinarlo, tenemos 10 intentos para ello.
- Ahora nos conectamos al servidor que nos dan con ssh y al parecer se esta ejecutando el script que vimos anteriormente.
- Ahora solo queda adivinar el numero, lo que hice fue tomar los números que quedan en medio por ejemplo la mitad de 1000 es 500 y de ahí partí. 

```
┌──(kali㉿kali)-[~/…/Binary Search/home/ctf-player/drop-in]
└─$ ssh -p 58706 ctf-player@atlas.picoctf.net

The authenticity of host '[atlas.picoctf.net]:58706 ([18.217.83.136]:58706)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:58706' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 700
Higher! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 725
Higher! Try again.
Enter your guess: 740
Lower! Try again.
Enter your guess: 735
Lower! Try again.
Enter your guess: 733
Congratulations! You guessed the correct number: 733
Here's your flag: picoCTF{g00d_gu355_1597707f}
Connection to atlas.picoctf.net closed.


```

## **Notas adicionales**

## **Referencias**
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)