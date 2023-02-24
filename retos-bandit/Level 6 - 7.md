# Bandit Level 6 → Level 7

## Objetivo
La contraseña para el siguiente nivel se almacena **en algún lugar del y** tiene todas las propiedades siguientes:
-   Propiedad del usuario Bandit7.
-   Propiedad de Group Bandit6.
-   33 Bytes de tamaño.

## Datos de acceso al nivel
* Servidor: ssh bandit6@bandit.labs.overthewire.org
* Usuario: bandit6
* Contraseña: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solución
``` bash 
C:\Users\vikyg>ssh bandit6@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit6@bandit.labs.overthewire.org's password:
```
``` bash 
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Jan 11 19:18 .
drwxr-xr-x 70 root root 4096 Jan 11 19:19 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| -user | Especificar un usuario.|
| -group | Especificar un grupo. |
| 2 > | Redirigir a otro destino. |

## Referencias
* [Ninguna]

Fecha: 16/02/2023.