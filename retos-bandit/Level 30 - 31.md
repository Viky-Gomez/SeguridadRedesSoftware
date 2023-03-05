# Bandit Level 30 → Level 31

## Objetivo
Hay un repositorio git. La contraseña para el usuario es la misma que para el usuario: ssh://bandit30-git@localhost/home/bandit30-git/repobandit30-gitbandit30.

Clone el repositorio y encuentre la contraseña para el siguiente nivel.

## Datos de acceso al nivel
* Servidor: ssh bandit30@bandit.labs.overthewire.org
* Usuario: bandit30
* Contraseña: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

## Solución
``` bash 
bandit30@bandit:~$ mktemp -d
/tmp/tmp.0U6FaRM8Bl
bandit30@bandit:~$ cd /tmp/tmp.0U6FaRM8Bl
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
bandit30-git@localhosts password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), 299 bytes | 299.00 KiB/s, done.
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl$ ls -la
total 124
drwx------   3 bandit30 bandit30   4096 Mar  4 02:12 .
drwxrwx-wt 424 root     root     114688 Mar  4 02:12 ..
drwxrwxr-x   3 bandit30 bandit30   4096 Mar  4 02:12 repo
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl$ cd repo
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ git show-ref
cf552c166d78421e64ddf52f850e680075d216e1 refs/heads/master
cf552c166d78421e64ddf52f850e680075d216e1 refs/remotes/origin/HEAD
cf552c166d78421e64ddf52f850e680075d216e1 refs/remotes/origin/master
831aac2e2341f009e40e46392a4f5dd318483019 refs/tags/secret
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ git show cf552c166d78421e64ddf52f850e680075d216e1
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..029ba42
--- /dev/null
+++ b/README.md
@@ -0,0 +1 @@
+just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.0U6FaRM8Bl/repo$ git show 831aac2e2341f009e40e46392a4f5dd318483019
'OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt'
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| git branch | Lista, crea o elimina ramas. |
| -a | Enumera todas las ramas remotas. |
| git show -ref | Lista de referencias en un repositorio local. |

## Referencias
* [git branch](https://www.atlassian.com/git/tutorials/using-branches#:~:text=The%20git%20branch%20command%20lets%20you%20create%2C%20list%2C,repository.%20This%20is%20synonymous%20with%20git%20branch%20--list.)
*  [git show-ref](https://git-scm.com/docs/git-show-ref)

Fecha: 03/03/2023.