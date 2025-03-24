## **Descripción**
Jacky is not very knowledgable about the best security passwords and used a simple password to encrypt their BitLocker drive. See if you can break through the encryption!Download the disk image [here](https://challenge-files.picoctf.net/c_verbal_sleep/9e934e4d78276b12e27224dac16e50e6bbeae810367732eee4d5e38e6b2bb868/bitlocker-1.dd) 
## Hints
1. Hash cracking
## **Solución** 
Para este reto haremos lo siguiente:
- Descargamos la imagen del disco, este tiene por nombre bitlocker-1.dd.
- Teniendo la imgaen prodemos a realizar  procedemos a utilizar binwalk y mmls pero estos no son utiiles ya que el disco esta protegido por bitlock.
  1.- Vamos a Extraer el hash de BitLocker usando bitlocker2john
		`bitlocker2john /ruta/a/la/imagen_bitlocker.img > bitlockerhash.txt`
  2.- Usamos ```bitlocker -i bitlockerhash.txt
	- Para obtener el hash que romperemos, este lo tenemos que guardar en un nuevo archivo  *hash.txt* lo podremos distinguir ya que inicia por  $ bitlocker $ 
  3.-Enseguido usamos hashcat para romper el hash y obtener la contraseña:
	- `hashcat` -m 22100 -a 0 hash.txt  /ruta/a/rockyou.txt
	- `-m 22100`: Modo de hash (en este caso, para BitLocker).
	- `-a 0`: Modo de ataque diccionario.
	- `/ruta/a/rockyou.txt`: Especifica el archivo de diccionario.
	- Después de un momento se encuentra con la contraseña " **jacqueline** "
   4.  Ahora solo queda usar dislocker para acceder al disco cifrado utilizando la contraseña que obtuvimos, el disco lo montamos en la carpeta mnt (esta pueda ser la que ustedes quieran)
   5. Por ultimo me muevo a la carpeta donde esta el disco montado, en esto caso yo utilice un simple ***strings*** con un ***grep*** para buscar la bandera 


```
---------------------------------- 1 -------------------------------
┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE/Bitlocker-1]
└─$ hashcat -m 22100 -a 0 HASH.txt /usr/share/wordlists/rockyou.txt

hashcat (v6.2.6) starting

OpenCL API (OpenCL 3.0 PoCL 6.0+debian  Linux, None+Asserts, RELOC, LLVM 17.0.6, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
============================================================================================================================================
* Device #1: cpu-penryn-12th Gen Intel(R) Core(TM) i5-12450H, 2917/5898 MB (1024 MB allocatable), 8MCU

Minimum password length supported by kernel: 4
Maximum password length supported by kernel: 256

INFO: All hashes found as potfile and/or empty entries! Use --show to display them.

Started: Sun Mar  9 17:25:54 2025
Stopped: Sun Mar  9 17:25:56 2025

--------------------------------- 2 -----------------------------------------

┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE/Bitlocker-1]
└─$ hashcat -m 22100 -a 0 HASH.txt --show                          
$bitlocker$0$16$cb4809fe9628471a411f8380e0f668db$1048576$12$d04d9c58eed6da010a000000$60$68156e51e53f0a01c076a32ba2b2999afffce8530fbe5d84b4c19ac71f6c79375b87d40c2d871ed2b7b5559d71ba31b6779c6f41412fd6869442d66d:jacqueline

--------------------------------- 3 ---------------------------------------------

┌──(kali㉿kali)-[~/Documents/COMPETICION PICOCTF/FORENCE/Bitlocker-1]
└─$ sudo dislocker -u bitlocker-1.dd -- /mnt          

Enter the user password: jacqueline

┌──(kali㉿kali)-[/]
└─$ sudo su       
┌──(root㉿kali)-[/]
└─# cd mnt 

┌──(root㉿kali)-[/mnt]
└─# ls
dislocker-file
------------------------------- 4 -----------------------------------------
┌──(root㉿kali)-[/mnt]
└─# strings dislocker-file | grep 'pico'
picoCTF{us3_b3tt3r_p4ssw0rd5_pl5!_3242adb1}

```


## **Notas adicionales**

## **Referencias**
- https://www.networkdatapedia.com/post/decrypting-bitlocker-with-hashcat-a-beginner-friendly-guide-casey-mullis
- https://www.kali.org/tools/wordlists/
- 