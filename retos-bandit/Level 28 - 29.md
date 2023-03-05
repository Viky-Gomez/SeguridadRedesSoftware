# Bandit Level 28 → Level 29

## Objetivo
Hay un repositorio git. La contraseña para el usuario es la misma que para el usuario : `ssh://bandit28-git@localhost/home/bandit28-git/repobandit28-gitbandit28`.
Clone el repositorio y encuentre la contraseña para el siguiente nivel.

## Datos de acceso al nivel
* Servidor: ssh bandit28@bandit.labs.overthewire.org
* Usuario: bandit28
* Contraseña: AVanL161y9rsbcJIsFHuw35rjaOM19nR

## Solución
``` bash 
bandit28@bandit:~$ mktemp -d
/tmp/tmp.UmUvp0nTge
bandit28@bandit:~$ cd /tmp/tmp.UmUvp0nTge
bandit28@bandit:/tmp/tmp.UmUvp0nTge$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory home/bandit28/.ssh (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhosts password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/tmp.UmUvp0nTge$ ls -la
total 124
drwx------   3 bandit28 bandit28   4096 Mar  4 01:30 .
drwxrwx-wt 402 root     root     114688 Mar  4 01:30 ..
drwxrwxr-x   3 bandit28 bandit28   4096 Mar  4 01:30 repo
bandit28@bandit:/tmp/tmp.UmUvp0nTge$ cd repo
bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ ls
README.md
bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials
- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md

bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ git checkout cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Previous HEAD position was 104db85 fix info leak
HEAD is now at cd3b97e initial commit of README.md
bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials
- username: bandit29
- password: <TBD>

bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ git checkout 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Previous HEAD position was 104db85 fix info leak
HEAD is now at 6c3c5e4 add missing data
bandit28@bandit:/tmp/tmp.UmUvp0nTge/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials
- username: bandit29
- password: 'tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S'
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| mktemp | Toma la plantilla de nombre de archivo dada y sobrescribe una parte de ella para crear un nombre de archivo único.|
| git log | Muestra las instancias confirmadas. Se utiliza para enumerar y filtrar el historial del proyecto, y poder buscar cambios particulares.|
| git checkout | Cambia ramas y restaura archivos del árbol de trabajo. |

## Referencias
* [mktemp]([mktemp - Unix, Comando Linux (tutorialspoint.com)]https://www.tutorialspoint.com/unix_commands/mktemp.htm)
* [git log](https://www.w3docs.com/learn-git/git-log.html#:~:text=The%20git%20log%20command%20shows%20committed%20snapshots.%20It,controlling%20the%20working%20directory%20and%20the%20staging%20area.)
* [git checkout](https://git-scm.com/docs/git-checkout)

Fecha: 03/03/2023.