# Bandit Level 18 → Level 19

## Objetivo
La contraseña para el siguiente nivel se almacena en un **archivo léame** en el directorio principal. Desafortunadamente, alguien ha modificado .**bashrc** para cerrar sesión cuando inicia sesión con SSH.

## Datos de acceso al nivel
* Servidor: ssh bandit18@bandit.labs.overthewire.org
* Usuario: bandit18
* Contraseña: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Solución
*- Forma 1:*
``` bash 
C:\Users\vikyg>ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC 
```
*- Forma 2:*
``` bash 
C:\Users\vikyg>ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
id
uid=11018(bandit18) gid=11018(bandit18) groups=11018(bandit18)
ls
readme
cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
exit
```

## Notas Adicionales
* Ninguna.

## Referencias
* [Ninguna]

Fecha: 23/02/2023.