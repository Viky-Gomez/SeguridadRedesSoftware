# Bandit Level 2 → Level 3

## Objetivo
La contraseña para el siguiente nivel se almacena en un archivo llamado **espacios**. En este nombre de archivo ubicado en el directorio principal.

## Datos de acceso al nivel
* Servidor: ssh bandit2@bandit.labs.overthewire.org
* Usuario: bandit2
* Contraseña: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Solución
``` bash
C:\Users\vikyg>ssh bandit2@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit2@bandit.labs.overthewire.org's password:
```
``` bash
bandit2@bandit:~$ whoami
bandit2
bandit2@bandit:~$ pwd
/home/bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spacs\ in\ this\ filename
cat: 'spacs in this filename': No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Notas Adicionales
- Cuando hay espacios en el nombre, hay que delimitarlo.

## Referencias
* [Espacios en blanco en filename]([Cómo hacer referencia al nombre de archivo con espacios en Linux (linuxhint.com)](https://linuxhint.com/reference-filename-with-spaces-linux/))

Fecha: 16/02/2023.