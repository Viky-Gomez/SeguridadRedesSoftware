# Bandit Level 29 → Level 30

## Objetivo
Hay un repositorio git. La contraseña para el usuario es la misma que para el usuario: `ssh://bandit29-git@localhost/home/bandit29-git/repobandit29-gitbandit29`.
Clone el repositorio y encuentre la contraseña para el siguiente nivel.

## Datos de acceso al nivel
* Servidor: ssh bandit29@bandit.labs.overthewire.org
* Usuario: bandit29
* Contraseña: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

## Solución
``` bash 
bandit29@bandit:~$
bandit29@bandit:~$ mktemp -d
/tmp/tmp.VVqA1rAJvy
bandit29@bandit:~$ cd /tmp/tmp.VVqA1rAJvy
bandit29@bandit:/tmp/tmp.VVqA1rAJvy$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
bandit29-git@localhosts password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/tmp.VVqA1rAJvy$ ls -la
total 124
drwx------   3 bandit29 bandit29   4096 Mar  4 01:49 .
drwxrwx-wt 412 root     root     114688 Mar  4 01:49 ..
drwxrwxr-x   3 bandit29 bandit29   4096 Mar  4 01:49 repo
bandit29@bandit:/tmp/tmp.VVqA1rAJvy$ cd repo/
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials
- username: bandit30
- password: <no passwords in production!>
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git diff 0afe3501277395fbfa017480925edee3df6e8bb5 c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
diff --git a/README.md b/README.md
index 1af21d3..2da2f39 100644
--- a/README.md
+++ b/README.md
@@ -3,6 +3,6 @@ Some notes for bandit30 of bandit.

 ## credentials
-- username: bandit30
+- username: bandit29
 - password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git branch
* (HEAD detached at 0afe350)
  master
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git branch -a
* (HEAD detached at 0afe350)
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git checkout remotes/origin/dev
Previous HEAD position was 0afe350 fix username
HEAD is now at fbbce0e add data needed for development
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git branch
* (HEAD detached at origin/dev)
  master
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git log
commit fbbce0ec6c80acb0fdc00ebb4b5228dd868fd799 (HEAD, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    add data needed for development

commit 925c929e0527f14c189b3d617d2bcc60f019f567
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    add gif2ascii

commit 0afe3501277395fbfa017480925edee3df6e8bb5 (origin/master, origin/HEAD, master)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$ git show fbbce0ec6c80acb0fdc00ebb4b5228dd868fd799
commit fbbce0ec6c80acb0fdc00ebb4b5228dd868fd799 (HEAD, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    add data needed for development

diff --git a/README.md b/README.md
index 1af21d3..a4b1cf1 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
 ## credentials

 - username: bandit30
-- password: <no passwords in production!>
+- password: 'xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS'

bandit29@bandit:/tmp/tmp.VVqA1rAJvy/repo$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| git diff | Muestra todos los cambios realizados en el archivo después de hacer una confirmación. |
| git show | Se utiliza para ver detalles ampliados en objetos Git como blobs, árboles, etiquetas y confirmaciones. tiene un comportamiento específico por tipo de objeto. |

## Referencias
* [git diff](https://www.geeksforgeeks.org/git-diff/)
* [git show]() 

Fecha: 03/03/2023.