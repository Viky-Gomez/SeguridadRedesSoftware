# Bandit Level 4 → Level 5

## Objetivo
La contraseña para el siguiente nivel se almacena en el único legible por humanos en el directorio **inhere**. Consejo: si tu terminal está desordenado, intente el comando "Restablecer".

## Datos de acceso al nivel
* Servidor: ssh bandit4@bandit.labs.overthewire.org
* User: bandit4
* Contraseña: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## Solución
``` bash 
C:\Users\vikyg>ssh bandit4@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit4@bandit.labs.overthewire.org's password:
```
``` bash 
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| file  | Indica el tipo de archivo que contiene un directorio.|
| * | Comodín que indica "todos", Ejemplo: file./*, aplica file a todos los archivos.*|

## Referencias
* [Ninguna]

Fecha: 16/02/2023.












