# Bandit Level 17 → Level 18

## Objetivo
Hay 2 archivos en el directorio de inicio: **passwords.old y passwords.new**. La contraseña para el siguiente nivel está en passwords.new y es la única línea que se ha cambiado entre **passwords.old y passwords.new**.

## Datos de acceso al nivel
* Servidor: ssh bandit17@bandit.labs.overthewire.org
* Usuario: bandit17
* Contraseña: VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## Solución
``` bash 
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$
```

## Notas Adicionales
|Comando | Descripcion |
|-----|-------|
| diff | Muestra las diferencias en los archivos comparándolos línea por línea. |

## Referencias
* [diff]([comando diff en Linux con ejemplos - GeeksforGeeks](https://www.geeksforgeeks.org/diff-command-linux-examples/))

Fecha: 23/02/2023.