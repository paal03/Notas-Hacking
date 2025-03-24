## **Descripción**
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:
## Hint
- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
- You can 'checkout' commits to see the files inside them
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Lo descomprimimos con unzip, aqui vamos a encontrar un archivo el cual al aparecer no tiene nada, para este reto al paracer haremos uso del control de versiones de git.
- Asi que hacemos uso de un git log para ver las confirmaciones previas, y una de ellas tiene una nota que dice "create flag" con su ID.
- Por ultimo hacemos un git checkout ID, y ahora un cat message.txt, con esto tendremos la bandera.

```
┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Commitment Issues/drop-in]
└─$ git log     
commit 8dc51806c760dfdbb34b33a2008926d3d8e8ad49 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    remove sensitive info

commit 87b85d7dfb839b077678611280fa023d76e017b8
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    create flag

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Commitment Issues/drop-in]
└─$ git checkout 87b85d7 
Note: switching to '87b85d7'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 87b85d7 create flag


┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Commitment Issues/drop-in]
└─$ cat message.txt 
picoCTF{s@n1t1z3_ea83ff2a}


```

## **Notas adicionales**


## **Referencias**
https://primer.picoctf.org/#_git_version_control
