# Bandit Level 22 → Level 23

## Objetivo
Un programa se ejecuta automáticamente a intervalos regulares desde **cron**, el programador de trabajos basado en el tiempo. Busque en /**etc/cron.d/** la configuración y ver qué comando se está ejecutando.

## Datos de acceso al nivel
* Servidor: ssh bandit22@bandit.labs.overthewire.org
* Usuario: bandit22
* Contraseña: WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

## Solución
``` bash
bandit22@bandit:~$ ls /etc/cron.d
cronjob_bandit15_root  cronjob_bandit23       e2scrub_all
cronjob_bandit17_root  cronjob_bandit24       otw-tmp-dir
cronjob_bandit22       cronjob_bandit25_root  sysstat
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash
myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ /usr/bin/cronjob_bandit23.sh
Copying passwordfile /etc/bandit_pass/bandit22 to /tmp/8169b67bd894ddbb4412f91573b38db3
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $bandit23
bandit22@bandit:~$ echo $(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
'QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G'
bandit22@bandit:~$
```

## Notas Adicionales
* *md5sum:*  Verifica la integridad de los datos. Es un hash criptográfico de 128 bits y se puede usar para verificar la autenticidad e integridad de un archivo.
* *echo:* Muestra la línea de texto/cadena que se pasa como un argumento. 

## Referencias
* [md5sum](https://www.geeksforgeeks.org/md5sum-linux-command/)
* [echo](https://www.geeksforgeeks.org/echo-command-in-linux-with-examples/)

Fecha: 28/02/2023.