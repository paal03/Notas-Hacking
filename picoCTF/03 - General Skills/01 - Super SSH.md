## **Descripción**
Using a Secure Shell (SSH) is going to be pretty important.
Additional details will be available after launching your challenge instance.

Using a Secure Shell (SSH) is going to be pretty important.Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `61738` to get the flag?You'll also need the password `84b12bae`. If asked, accept the fingerprint with `yes`.
## **Solución** 
Para este reto solo nos conectaremos a un servidor con `ssh` usando los datos que nos dan.
Se realiza la conexión brevemente con el servidor y nos arroja la bandera, por ultimo la conexión se cierra automáticamente.

```
┌──(kali㉿kali)-[~/Documents/General Skills]
└─$ ssh ctf-player@titan.picoctf.net -p 61738    
The authenticity of host '[titan.picoctf.net]:61738 ([3.139.174.234]:61738)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:4: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[titan.picoctf.net]:61738' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_07a987ac}
Connection to titan.picoctf.net closed.

				picoCTF{s3cur3_c0nn3ct10n_07a987ac}

```

## **Notas adicionales**
`ssh remote_username@remote_host`
## **Referencias**
[https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
https://webshell.picoctf.org/
