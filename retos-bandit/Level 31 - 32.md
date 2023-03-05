# Bandit Level 31 → Level 32

## Objetivo
Hay un repositorio git. La contraseña para el usuario es la misma que para el usuario: `ssh://bandit31-git@localhost/home/bandit31-git/repobandit31-gitbandit31`.
Clone el repositorio y encuentre la contraseña para el siguiente nivel.

## Datos de acceso al nivel
* Servidor: ssh bandit31@bandit.labs.overthewire.org
* Usuario: bandit31
* Contraseña: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt

## Solución
``` bash 
bandit31@bandit:~$ mktemp -d
/tmp/tmp.kuQ2Ys0W4x
bandit31@bandit:~$ cd /tmp/tmp.kuQ2Ys0W4x
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
Cloning into 'repo'...
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhosts password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x$ ls -la
total 124
drwx------   3 bandit31 bandit31   4096 Mar  5 15:42 .
drwxrwx-wt 786 root     root     114688 Mar  5 15:42 ..
drwxrwxr-x   3 bandit31 bandit31   4096 Mar  5 15:42 repo
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x$ cd repo
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ ls
README.md
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ git branch
* master
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ touch key.txt
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ echo "May I come in?" > key.
txt
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ cat .gitignore
*.txt
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ git add -f key.txt
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ git commit -m "update key.tx
t file"
[master 4bd1294] update key.txt file
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$ git push
The authenticity of host [localhost]:2220 ([127.0.0.1]:2220) cant be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhosts password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 330 bytes | 110.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: 'rmCBvG56y58BXzv98yZGdO7ATVL5dW8y'
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to ssh://localhost:2220/home/bandit31-git/repo
bandit31@bandit:/tmp/tmp.kuQ2Ys0W4x/repo$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| touch | Crea un archivo sin ningún contenido. |
| git add | Agrega contenido de archivo al índice del repositorio. | 
| git commit | Registra los cambios realizados en el repositorio. |
| git push | Actualiza referencias remotas junto con objetos asociados. | 

## Referencias
* [touch](https://www.geeksforgeeks.org/touch-command-in-linux-with-examples/)
* [git add](https://git-scm.com/docs/git-add)
* [git commit](https://git-scm.com/docs/git-commit)
* [git push](https://git-scm.com/docs/git-push)

Fecha: 04/03/2023.