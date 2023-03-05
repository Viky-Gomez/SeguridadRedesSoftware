# Bandit Level 27 → Level 28

## Objetivo
Hay un repositorio git en . La contraseña para el usuario es la misma que para el usuario: ssh://bandit27-git@localhost/home/bandit27-git/repo``bandit27-git``bandit27.

Clone el repositorio y encuentre la contraseña para el siguiente nivel.
## Datos de acceso al nivel
* Servidor: ssh bandit27@bandit.labs.overthewire.org
* Usuario: bandit27
* Contraseña: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS

## Solución
``` bash
bandit27@bandit:/$ mktemp -d
/tmp/tmp.4SY07NDSFG
bandit27@bandit:/$ cd /tmp/tmp.4SY07NDSFG
bandit27@bandit:/tmp/tmp.4SY07NDSFG$ git clone ssh://bandit27-git@localhost/home/bandit27-git/repobandit27-gitbandit27
Cloning into repobandit27-gitbandit27...
The authenticity of host localhost (127.0.0.1) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).

                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

!!! You are trying to log into this SSH server on port 22, which is not intended.

bandit27-git@localhost: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
bandit27@bandit:/tmp/tmp.4SY07NDSFG$
bandit27@bandit:/tmp/tmp.4SY07NDSFG$ git glone ssh://bandit27-
git@localhost:2220/home/bandit27-git/repo
git: 'glone' is not a git command. See 'git --help'.

The most similar command is
        clone
-bash: git@localhost:2220/home/bandit27-git/repo: No such file or directory
bandit27@bandit:/tmp/tmp.4SY07NDSFG$ git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit27/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit27-git@localhosts password: 'YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS'
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.4SY07NDSFG$ ls -la
total 124
drwx------   3 bandit27 bandit27   4096 Mar  4 00:21 .
drwxrwx-wt 364 root     root     114688 Mar  4 00:21 ..
drwxrwxr-x   3 bandit27 bandit27   4096 Mar  4 00:21 repo
bandit27@bandit:/tmp/tmp.4SY07NDSFG$ cd repo/
bandit27@bandit:/tmp/tmp.4SY07NDSFG/repo$ ls
README
bandit27@bandit:/tmp/tmp.4SY07NDSFG/repo$ cat README
The password to the next level is: 'AVanL161y9rsbcJIsFHuw35rjaOM19nR'
bandit27@bandit:/tmp/tmp.4SY07NDSFG/repo$
```

## Notas Adicionales
* *git clone:* Es una utilidad de línea de comandos de Git que se utiliza para fijar como objetivo un repositorio existente con el fin de clonarlo o copiarlo.

## Referencias
* [git clone](https://www.atlassian.com/es/git/tutorials/setting-up-a-repository/git-clone)

Fecha: 28/02/2023.