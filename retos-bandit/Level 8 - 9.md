# Bandit Level 8 → Level 9

## Objetivo
La contraseña para el siguiente nivel se almacena en los datos del archivo**.txt** y es la única línea de texto que aparece solo una vez.

## Datos de acceso al nivel
* Servidor: ssh bandit8@bandit.labs.overthewire.org
* Usuario: bandit8
* Contraseña: TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solución
``` bash 
C:\Users\vikyg>ssh bandit8@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit8@bandit.labs.overthewire.org's password:
```
``` bash
bandit8@bandit:~$ ls data.txt 
bandit8@bandit:~$ wc data.txt 
1001 1001 33033 data.txt 
bandit8@bandit:~$ cat data.txt | sort | uniq -u 
EN632PlfYiZbn3PhVK3XOGSlNInNE00t 
bandit8@bandit:~$
```

## Notas Adicionales

|Comando | Descripcion |
|-----|-------|
| grep | Filtra las líneas repetidas en un archivo.

## Referencias
* [grep]([uniq Command en LINUX con ejemplos - GeeksforGeeks](https://www.geeksforgeeks.org/uniq-command-in-linux-with-examples/))

Fecha: 16/02/2023.