## **Descripción**
If you want to hash with the best, beat this test!
Additional details will be available after launching your challenge instance.
## Hints
1. You can use a commandline tool or web app to hash text
2. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## **Solución** 
Para este reto haremos lo siguiente:
- Nos conectaremos a vía netcat al servidor que nos dan.
- Esta nos despliega unas preguntas las cuales consisten en convertir las cadenas que nos dan a  md5 hash .
- Entonces para la resolución de los retos solo basta con ir generando los hash correspondientes a cada cadena y irlas ingresando.
- Al final nos darán la bandera.

```
Shadow75-picoctf@webshell:~$ nc saturn.picoctf.net 52368
Please md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Answer: 
2f7cfa603df2a25fce27ad69cd4be673
2f7cfa603df2a25fce27ad69cd4be673
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Adam Sandler'
Answer: 
dfaa815a18f38cd5737f9fd73b907d6e
dfaa815a18f38cd5737f9fd73b907d6e
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'choir boys'
Answer: 
ce6b6964402e279f878ce9cf5e19d14b
ce6b6964402e279f878ce9cf5e19d14b
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}
```

## **Notas adicionales**

## **Referencias**