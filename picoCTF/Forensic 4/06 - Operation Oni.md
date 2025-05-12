## **Descripción**
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
Additional details will be available after launching your challenge instance.
## Hints
1. 
## **Solución** 
Para este reto haremos lo siguiente:
- 


```
┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationoni]
└─$ gzip -d disk.img.gz                           

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationoni]
└─$ icat disk.img -o 206848 2345 > key_file            

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationoni]
└─$ chmod 600 key_file 

┌──(kali㉿kali)-[~/Documents/PicoCTF/Forensics/operationoni]
└─$ ssh -i key_file -p 56426 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:56426 ([13.59.203.175]:56426)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:56426' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_b5066e83}ctf-player@challenge:~$ 

```

## **Notas adicionales**

## **Referencias**