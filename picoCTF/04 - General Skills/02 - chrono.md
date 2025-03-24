## **Descripción**
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.
```
Server: saturn.picoctf.net
Port: 49526
Username: picoplayer 
Password: ENAFb6zfzn
```
## **Solución** 
Para este reto haremos lo siguiente:
- Primero nos conectamos al servidor con ssh.
- Nos cambias a la ruta principal y ingresamos en la carpeta etc.
- En la carpeta etc se suelen almacenar, las tareas de crontab.
- Una vez en la carpeta etc, buscamos la tarea de crontab y leemos el contenido.
- Al parecer con solo hacer un cat nos muestra la bandera.

```
picoplayer@challenge:~$ cd /
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ cd etc
picoplayer@challenge:/etc$ ls
adduser.conf            cloud         debconf.conf    fstab      hostname     kernel         logrotate.d    mke2fs.conf          pam.conf   rc0.d  resolv.conf  ssh        sysctl.conf  update-motd.d
alternatives            cron.d        debian_version  gai.conf   hosts        ld.so.cache    lsb-release    modules-load.d       pam.d      rc1.d  rmt          ssl        sysctl.d     wgetrc
apt                     cron.daily    default         group      hosts.allow  ld.so.conf     machine-id     mtab                 passwd     rc2.d  security     subgid     systemd      xattr.conf
bash.bashrc             cron.hourly   deluser.conf    group-     hosts.deny   ld.so.conf.d   magic          networkd-dispatcher  passwd-    rc3.d  selinux      subgid-    terminfo     xdg
bindresvport.blacklist  cron.monthly  dhcp            gshadow    init.d       legal          magic.mime     networks             profile    rc4.d  shadow       subuid     timezone
binfmt.d                cron.weekly   dpkg            gshadow-   inputrc      libaudit.conf  mailcap        nsswitch.conf        profile.d  rc5.d  shadow-      subuid-    tmpfiles.d
ca-certificates         crontab       e2scrub.conf    gss        issue        localtime      mailcap.order  opt                  python3    rc6.d  shells       sudoers    ucf.conf
ca-certificates.conf    dbus-1        environment     host.conf  issue.net    login.defs     mime.types     os-release           python3.8  rcS.d  skel         sudoers.d  ufw
picoplayer@challenge:/etc$ cat crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}

```

## **Notas adicionales**
Los crontabs de todo el sistema se almacenan en el archivo `/etc/crontab` o en archivos individuales dentro del directorio `/etc/cron.d/`

## **Referencias**
- 