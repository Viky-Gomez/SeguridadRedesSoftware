# Bandit Level 9 → Level 10

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo**.txt** en una de las pocas cadenas legibles por humanos, precedida por varios '=' Caracteres.

## Datos de acceso al nivel
* Servidor: ssh bandit9@bandit.labs.overthewire.org
* Usuario: bandit9
* Contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solución
``` bash
C:\Users\vikyg>ssh bandit9@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit9@bandit.labs.overthewire.org's password:
````
``` bash
bandit9@bandit:~$ ls data.txt 
bandit9@bandit:~$ file data.txt data.txt: data 
bandit9@bandit:~$ strings data.txt | grep == 
c========== the 
h;========== password 
========== isT 
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s 
bandit9@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| strings | Proporciona el nombre del archivo que se desea buscar en la línea de comandos..

## Referencias
* [strings](https://www.howtogeek.com/427805/how-to-use-the-strings-command-on-linux/)

Fecha: 16/02/2023.