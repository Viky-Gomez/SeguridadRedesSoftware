# Bandit Level 5 → Level 6

## Objetivo
La contraseña para el siguiente nivel se almacena en un archivo en algún lugar bajo el directorio **inhere**, y tiene todas las propiedades siguientes:
-   Legible por humanos.
-   1033 Bytes de tamaño.
-   No ejecutable.

## Datos de acceso al nivel
* Servidor: ssh bandit5@bandit.labs.overthewire.org
* Usuario: bandit5
* Contraseña: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Solución
```bash 
C:\Users\vikyg>ssh bandit5@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames
```
``` bash 
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| -readable | Mostrar código legible en ASCII.|
| find | Permite encontrar archivos en el sistema. |
| -size | Especifica el tamaño. |
| -size XXc| Especifica la cantidad de caracteres.|
| -type | Especificar el tipo. |

## Referencias
* [Ninguna]

Fecha: 16/02/2023.