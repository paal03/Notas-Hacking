## **Descripción**
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)
## Hints
- `git branch -a` will let you see available branches
- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
## **Solución** 
Para este reto haremos lo siguiente:
- Primero descargamos el archivo con el enlace que nos dan con wget.
- Lo descomprimimos con unzip, aqui vamos a encontrar un archivo el cual al aparecer no tiene nada, para este reto al parecer haremos uso del control de versiones de git.
- Al parecer la bandera esta dividida en 3 partes asi que:
- Primero vamos hacer uso de git log feature/part-'1,2,3' para conocer el [id] de cada parte.
- Despues hacemos git diff [id] -- flag.py
- Esto lo replicamos para las 3 partes y obtenemos la bandera.

```
┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ ls
flag.py

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git log feature/part-1                                      
commit 300cff1bf1f64637dd9ff603d90176e8e8bdeb01 (feature/part-1)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    add part 1

commit 5e4b2dae1868abb644627483c78a683286dfe67c (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    init flag printer

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git diff 300cff1bf1f64637dd9ff603d90176e8e8bdeb01 -- flag.py
diff --git a/flag.py b/flag.py
index 6e17fb3..77d6cec 100644
--- a/flag.py
+++ b/flag.py
@@ -1,2 +1 @@
 print("Printing the flag...")
-print("picoCTF{t3@mw0rk_", end='')
\ No newline at end of file

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git log feature/part-2                                      
commit 74989a4f650d024929388b6788d2b4c214a07e49 (feature/part-2)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    add part 2

commit 5e4b2dae1868abb644627483c78a683286dfe67c (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    init flag printer

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git diff 74989a4f650d024929388b6788d2b4c214a07e49 -- flag.py
diff --git a/flag.py b/flag.py
index 7ab4e25..77d6cec 100644
--- a/flag.py
+++ b/flag.py
@@ -1,3 +1 @@
 print("Printing the flag...")
-
-print("m@k3s_th3_dr3@m_", end='')
\ No newline at end of file

┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git log feature/part-3                                      
commit 12c2ae89d8035b7a5aa7cd169dc9e93cc68201be (feature/part-3)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    add part 3

commit 5e4b2dae1868abb644627483c78a683286dfe67c (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:57 2024 +0000

    init flag printer
    
┌──(kali㉿kali)-[~/…/COMPETICION PICOCTF/GENERAL SKILLS/Collaborative Development/drop-in]
└─$ git diff 12c2ae89d8035b7a5aa7cd169dc9e93cc68201be -- flag.py
diff --git a/flag.py b/flag.py
index c312152..77d6cec 100644
--- a/flag.py
+++ b/flag.py
@@ -1,3 +1 @@
 print("Printing the flag...")
-
-print("w0rk_798f9981}")


					picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}

```

## **Notas adicionales**


## **Referencias**
https://primer.picoctf.org/#_git_version_control