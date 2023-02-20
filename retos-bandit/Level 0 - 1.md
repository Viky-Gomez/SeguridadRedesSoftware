# Bandit Level 0 → Level 1

## Objetivo
La contraseña para el siguiente nivel se almacena en un archivo llamado **léame** ubicado en el directorio de inicio. Usar esta contraseña para iniciar sesión en bandit1 usando SSH. Siempre que encuentres una contraseña para un nivel, usa SSH (en el puerto 2220) para iniciar sesión en ese nivel y continuar el juego.

## Datos de acceso al nivel
* Servidor: ssh bandit0@bandit.labs.overthewire.org
* Usuario: bandit0
* Contraseña: bandit0

## Solución
``` bash
C:\Users\vikyg>ssh bandit0@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:
```
``` bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$
```


## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| cat | muestra el contenido de un archivo.
| ls | lista de archivos. |

## Referencias
* [OverTheWire: Nivel Objetivo: Bandido Nivel 0 → Nivel 1](https://overthewire.org/wargames/bandit/bandit1.html)*

Fecha: 16/02/2023