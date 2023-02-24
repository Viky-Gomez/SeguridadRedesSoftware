# Bandit Level 3 → Level 4

## Objetivo
La contraseña para el siguiente nivel se almacena en un archivo oculto en el directorio **inhere**.

## Datos de acceso al nivel
* Servidor:  ssh bandit3@bandit.labs.overthewire.org
* Usuario: bandit3
* Contraseña: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## Solución
``` bash
C:\Users\vikyg>ssh bandit3@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit3@bandit.labs.overthewire.org's password:
```
``` bash 
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jan 11 19:19 .
drwxr-xr-x 3 root    root    4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3   33 Jan 11 19:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| ls -la | Mostrar listado de archivos ocultos de un directorio.

## Referencias
* [ninguna]

Fecha: 16/02/2023.