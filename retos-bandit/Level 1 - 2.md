# Bandit Level 1 → Level 2

## Objetivo
La contraseña para el siguiente nivel se almacena en un archivo llamado **-** ubicado en el directorio de inicio.

## Datos de acceso al nivel
* Servidor: ssh bandit1@bandit.labs.overthewire.org
* Usuario: bandit1
* Contraseña: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solución
``` bash
C:\Users\vikyg>ssh bandit1@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit1@bandit.labs.overthewire.org's password:
```
``` bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ cat /home/bandit/-
cat: /home/bandit/-: No such file or directory
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas Adicionales

|Comando | Descripcion |
|-----|-------|
| cat | muestra el contenido de un archivo.


## Referencias
- [archivos con guion](https://tldp.org/LDP/abs/html/special-chars.html)

Fecha: 16/02/2023.